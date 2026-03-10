# Technical Specification

## 1. System Overview

**Project Name:** SDLC Artifact Automation Platform

**Description:** An AI-driven platform to automate the creation of structured SDLC artifacts from raw requirements (PDF/DOCX/Text).

**Architecture Pattern:** Microservices

### Key Design Decisions

- Use a microservices architecture to ensure scalability and maintainability.
- Implement human validation checkpoints for all generated artifacts.
- Integrate GitHub for version-controlled artifact storage.

## 2. Data Model

### Entity: Requirement

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the requirement. |
| content | TEXT | The raw content of the requirement. |
| file_path | TEXT | The path to the file where the requirement is stored. |
| repo_name | TEXT | The name of the repository where the requirement is associated. |

**Relationships:** User, UserStory, TechSpec

### Entity: UserStory

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the user story. |
| content | TEXT | The content of the user story. |
| requirement_id | UUID | The ID of the requirement this user story is associated with. |

**Relationships:** Requirement

### Entity: TechSpec

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the tech spec. |
| content | TEXT | The content of the tech spec. |
| user_story_id | UUID | The ID of the user story this tech spec is associated with. |

**Relationships:** UserStory

## 3. API Design

| Method | Path | Description |
|--------|------|-------------|
| POST | `/api/requirements/upload` | Upload raw requirements (PDF/DOCX/Text) for processing. |
| GET | `/api/github/repos` | Fetch the list of repositories associated with the authenticated user. |
| POST | `/auth/github` | Initiate GitHub OAuth authentication. |
| GET | `/auth/github/callback` | Handle GitHub OAuth callback. |

### POST `/api/requirements/upload`

Upload raw requirements (PDF/DOCX/Text) for processing.

**Request Body:** repo: TEXT, requirements: TEXT

**Response Body:** id: UUID, status: TEXT

### GET `/api/github/repos`

Fetch the list of repositories associated with the authenticated user.

**Response Body:** [{name: TEXT, id: UUID}, ...]

### POST `/auth/github`

Initiate GitHub OAuth authentication.

**Response Body:** redirect_url: TEXT

### GET `/auth/github/callback`

Handle GitHub OAuth callback.

**Response Body:** token: TEXT, user_data: OBJECT

## 4. Component Breakdown

### Frontend

**Responsibility:** Provides a React web interface for uploads, review, and approvals.

### Backend

**Responsibility:** Orchestrates and processes raw requirements, integrates with GitHub, and manages human validation checkpoints.

**Depends on:** Frontend

### AI Agent

**Responsibility:** Generates structured SDLC artifacts using Python and LangGraph + HuggingFace models.

**Depends on:** Backend

### GitHub Integration

**Responsibility:** Handles version-controlled artifact storage and retrieval.

**Depends on:** Backend

## 5. Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React |
| Backend | Java/Spring Boot |
| Database | PostgreSQL |
| Infrastructure | AWS |

## 6. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Security vulnerabilities in OAuth flow | Unauthorized access to user data | Implement CSRF protection, validate state, and use HTTPS. |
| AI agent failure | Inconsistent or incorrect artifact generation | Implement retry logic and human validation checkpoints. |

## 7. Open Questions

- What is the expected format of the raw requirements (PDF/DOCX/Text)?
- How will the AI agent handle different types of raw requirements (e.g., tables, images)?
- What is the process for human validation of generated artifacts?
