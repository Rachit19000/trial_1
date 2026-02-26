# Technical Specification

## 1. System Overview

**Project Name:** Smart Project Governance & Access Control System

**Description:** A centralized governance system that consolidates people, project, allocation, timesheets, and access data into a single system for improved visibility, control, and compliance.

**Architecture Pattern:** Microservices

### Key Design Decisions

- Use a microservices architecture to enable modular development and scalability.
- Implement RBAC for secure access control.
- Use a relational database for data storage.

## 2. Data Model

### Entity: Employee

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the employee. |
| name | String | Employee's full name. |
| email | String | Employee's email address. |
| role | String | Employee's role in the organization. |
| department | String | Employee's department. |
| manager_id | UUID | ID of the employee's manager. |
| status | String | Employee's current status (active, inactive, etc.). |

**Relationships:** manager_id

### Entity: Project

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the project. |
| name | String | Project name. |
| owner_id | UUID | ID of the project owner. |
| start_date | Date | Project start date. |
| end_date | Date | Project end date. |
| status | String | Project status (active, completed, etc.). |

**Relationships:** owner_id

### Entity: Allocation

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the allocation. |
| employee_id | UUID | ID of the allocated employee. |
| project_id | UUID | ID of the project the employee is allocated to. |
| percentage | Integer | Percentage of the employee's time allocated to the project. |

**Relationships:** employee_id, project_id

### Entity: Timesheet

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the timesheet entry. |
| employee_id | UUID | ID of the employee who logged the timesheet entry. |
| project_id | UUID | ID of the project the timesheet entry is for. |
| date | Date | Date of the timesheet entry. |
| hours | Float | Number of hours worked on the project. |
| is_billable | Boolean | Indicates if the hours are billable. |

**Relationships:** employee_id, project_id

### Entity: AccessRequest

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the access request. |
| employee_id | UUID | ID of the employee requesting access. |
| project_id | UUID | ID of the project the access is for. |
| status | String | Status of the access request (pending, approved, denied). |
| request_date | Date | Date the access request was made. |

**Relationships:** employee_id, project_id

## 3. API Design

| Method | Path | Description |
|--------|------|-------------|
| GET | `/employees` | Retrieve a list of all employees. |
| POST | `/employees` | Create a new employee. |
| GET | `/employees/{id}` | Retrieve an employee by ID. |
| PUT | `/employees/{id}` | Update an employee. |
| DELETE | `/employees/{id}` | Delete an employee. |
| GET | `/projects` | Retrieve a list of all projects. |
| POST | `/projects` | Create a new project. |
| GET | `/projects/{id}` | Retrieve a project by ID. |
| PUT | `/projects/{id}` | Update a project. |
| DELETE | `/projects/{id}` | Delete a project. |
| GET | `/allocations` | Retrieve a list of all allocations. |
| POST | `/allocations` | Create a new allocation. |
| GET | `/allocations/{id}` | Retrieve an allocation by ID. |
| PUT | `/allocations/{id}` | Update an allocation. |
| DELETE | `/allocations/{id}` | Delete an allocation. |
| GET | `/timesheets` | Retrieve a list of all timesheets. |
| POST | `/timesheets` | Create a new timesheet entry. |
| GET | `/timesheets/{id}` | Retrieve a timesheet entry by ID. |
| PUT | `/timesheets/{id}` | Update a timesheet entry. |
| DELETE | `/timesheets/{id}` | Delete a timesheet entry. |
| GET | `/accessrequests` | Retrieve a list of all access requests. |
| POST | `/accessrequests` | Create a new access request. |
| GET | `/accessrequests/{id}` | Retrieve an access request by ID. |
| PUT | `/accessrequests/{id}` | Update an access request. |
| DELETE | `/accessrequests/{id}` | Delete an access request. |

### GET `/employees`

Retrieve a list of all employees.

**Response Body:** List of Employee entities.

### POST `/employees`

Create a new employee.

**Request Body:** Employee entity with required fields.

**Response Body:** Created Employee entity.

### GET `/employees/{id}`

Retrieve an employee by ID.

**Response Body:** Employee entity.

### PUT `/employees/{id}`

Update an employee.

**Request Body:** Employee entity with updated fields.

**Response Body:** Updated Employee entity.

### DELETE `/employees/{id}`

Delete an employee.

**Response Body:** Confirmation message.

### GET `/projects`

Retrieve a list of all projects.

**Response Body:** List of Project entities.

### POST `/projects`

Create a new project.

**Request Body:** Project entity with required fields.

**Response Body:** Created Project entity.

### GET `/projects/{id}`

Retrieve a project by ID.

**Response Body:** Project entity.

### PUT `/projects/{id}`

Update a project.

**Request Body:** Project entity with updated fields.

**Response Body:** Updated Project entity.

### DELETE `/projects/{id}`

Delete a project.

**Response Body:** Confirmation message.

### GET `/allocations`

Retrieve a list of all allocations.

**Response Body:** List of Allocation entities.

### POST `/allocations`

Create a new allocation.

**Request Body:** Allocation entity with required fields.

**Response Body:** Created Allocation entity.

### GET `/allocations/{id}`

Retrieve an allocation by ID.

**Response Body:** Allocation entity.

### PUT `/allocations/{id}`

Update an allocation.

**Request Body:** Allocation entity with updated fields.

**Response Body:** Updated Allocation entity.

### DELETE `/allocations/{id}`

Delete an allocation.

**Response Body:** Confirmation message.

### GET `/timesheets`

Retrieve a list of all timesheets.

**Response Body:** List of Timesheet entities.

### POST `/timesheets`

Create a new timesheet entry.

**Request Body:** Timesheet entity with required fields.

**Response Body:** Created Timesheet entity.

### GET `/timesheets/{id}`

Retrieve a timesheet entry by ID.

**Response Body:** Timesheet entity.

### PUT `/timesheets/{id}`

Update a timesheet entry.

**Request Body:** Timesheet entity with updated fields.

**Response Body:** Updated Timesheet entity.

### DELETE `/timesheets/{id}`

Delete a timesheet entry.

**Response Body:** Confirmation message.

### GET `/accessrequests`

Retrieve a list of all access requests.

**Response Body:** List of AccessRequest entities.

### POST `/accessrequests`

Create a new access request.

**Request Body:** AccessRequest entity with required fields.

**Response Body:** Created AccessRequest entity.

### GET `/accessrequests/{id}`

Retrieve an access request by ID.

**Response Body:** AccessRequest entity.

### PUT `/accessrequests/{id}`

Update an access request.

**Request Body:** AccessRequest entity with updated fields.

**Response Body:** Updated AccessRequest entity.

### DELETE `/accessrequests/{id}`

Delete an access request.

**Response Body:** Confirmation message.

## 4. Component Breakdown

### EmployeeService

**Responsibility:** Handles CRUD operations for employees, including validation and audit logging.

**Depends on:** Database

### ProjectService

**Responsibility:** Handles CRUD operations for projects, including validation and audit logging.

**Depends on:** Database

### AllocationService

**Responsibility:** Handles CRUD operations for allocations, including validation and audit logging.

**Depends on:** Database

### TimesheetService

**Responsibility:** Handles CRUD operations for timesheets, including validation and audit logging.

**Depends on:** Database

### AccessRequestService

**Responsibility:** Handles CRUD operations for access requests, including validation and audit logging.

**Depends on:** Database

### AuthenticationService

**Responsibility:** Manages user authentication and authorization, including JWT token generation and validation.

**Depends on:** Database

### DashboardService

**Responsibility:** Provides real-time dashboards and reports for project and employee data.

**Depends on:** EmployeeService, ProjectService, AllocationService, TimesheetService, AccessRequestService

## 5. Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React |
| Backend | Node.js with Express |
| Database | PostgreSQL |
| Infrastructure | AWS |

## 6. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Unavailability or mismatch of HROne mock data | Medium | Use sample schemas aligned with expected HROne structure. |
| Jira timesheet data not available or incomplete | High | Use mocked Jira worklogs with realistic data patterns. |
| Dependency between modules causing delays | Medium | Follow dependency-aware delivery and phased development. |
| Scope creep during implementation | Medium | Provide a section after project creation to clearly inform about in-scope and out-of-scope deliverables and any extra cost attached to them. |
| Performance issues with reports | Low | Use indexing, caching, and background processing. |
| Security gaps in access control | High | Enforce RBAC, audit logs, and secure authentication. |
| Limited/delayed access to MS Entra ID APIs | Medium | Fall-back to HR One based mapping. |

## 7. Open Questions

- What all access can be granted and what amount of data is available?
- How to include scope creep, reusable and non-reusable customization, flag extra efforts, calculation of estimated efforts?
- Gamifying Timesheet Entry – create a leaderboard
