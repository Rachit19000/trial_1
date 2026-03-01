# Technical Specification

## 1. System Overview

**Project Name:** Smart Project Governance & Access Control System

**Description:** A centralized governance system for managing employees, projects, allocations, timesheets, and access control with real-time visibility and controlled workflows.

**Architecture Pattern:** Microservices

### Key Design Decisions

- Use a microservices architecture to ensure modularity and scalability.
- Implement RBAC for secure access control.
- Utilize API-driven integrations for data consistency.

## 2. Data Model

### Entity: Employee

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the employee. |
| name | String | Employee's full name. |
| email | String | Employee's email address. |
| role | String | Employee's role within the organization. |
| department | String | Employee's department. |
| manager_id | UUID | Unique identifier for the employee's manager. |
| status | String | Employee's current status (active, inactive). |

**Relationships:** manager_id

### Entity: Project

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the project. |
| name | String | Name of the project. |
| owner_id | UUID | Unique identifier for the project owner. |
| start_date | Date | Start date of the project. |
| end_date | Date | End date of the project. |
| budget | Float | Budget allocated for the project. |

**Relationships:** owner_id

### Entity: Allocation

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the allocation. |
| employee_id | UUID | Unique identifier for the employee. |
| project_id | UUID | Unique identifier for the project. |
| percentage | Float | Percentage of employee's time allocated to the project. |

**Relationships:** employee_id, project_id

### Entity: Timesheet

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the timesheet. |
| employee_id | UUID | Unique identifier for the employee. |
| project_id | UUID | Unique identifier for the project. |
| date | Date | Date of the timesheet entry. |
| hours | Float | Number of hours worked on the project. |
| is_billable | Boolean | Indicates if the hours are billable. |

**Relationships:** employee_id, project_id

### Entity: AccessRequest

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the access request. |
| employee_id | UUID | Unique identifier for the employee. |
| project_id | UUID | Unique identifier for the project. |
| start_date | Date | Start date of the access request. |
| end_date | Date | End date of the access request. |
| status | String | Status of the access request (pending, approved, rejected). |

**Relationships:** employee_id, project_id

## 3. API Design

| Method | Path | Description |
|--------|------|-------------|
| GET | `/employees` | Retrieve a list of all employees. |
| POST | `/employees` | Create a new employee. |
| PUT | `/employees/{id}` | Update an existing employee. |
| DELETE | `/employees/{id}` | Delete an employee. |
| GET | `/projects` | Retrieve a list of all projects. |
| POST | `/projects` | Create a new project. |
| PUT | `/projects/{id}` | Update an existing project. |
| DELETE | `/projects/{id}` | Delete a project. |
| POST | `/allocations` | Create a new allocation. |
| PUT | `/allocations/{id}` | Update an existing allocation. |
| DELETE | `/allocations/{id}` | Delete an allocation. |
| POST | `/timesheets` | Create a new timesheet entry. |
| PUT | `/timesheets/{id}` | Update an existing timesheet entry. |
| DELETE | `/timesheets/{id}` | Delete a timesheet entry. |
| POST | `/accessrequests` | Create a new access request. |
| PUT | `/accessrequests/{id}` | Update an existing access request. |
| DELETE | `/accessrequests/{id}` | Delete an access request. |

### GET `/employees`

Retrieve a list of all employees.

**Response Body:** List of Employee entities.

### POST `/employees`

Create a new employee.

**Request Body:** Employee entity with required fields (name, email, role, department, manager_id, status).

**Response Body:** Created Employee entity.

### PUT `/employees/{id}`

Update an existing employee.

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

**Request Body:** Project entity with required fields (name, owner_id, start_date, end_date, budget).

**Response Body:** Created Project entity.

### PUT `/projects/{id}`

Update an existing project.

**Request Body:** Project entity with updated fields.

**Response Body:** Updated Project entity.

### DELETE `/projects/{id}`

Delete a project.

**Response Body:** Confirmation message.

### POST `/allocations`

Create a new allocation.

**Request Body:** Allocation entity with required fields (employee_id, project_id, percentage).

**Response Body:** Created Allocation entity.

### PUT `/allocations/{id}`

Update an existing allocation.

**Request Body:** Allocation entity with updated fields.

**Response Body:** Updated Allocation entity.

### DELETE `/allocations/{id}`

Delete an allocation.

**Response Body:** Confirmation message.

### POST `/timesheets`

Create a new timesheet entry.

**Request Body:** Timesheet entity with required fields (employee_id, project_id, date, hours, is_billable).

**Response Body:** Created Timesheet entity.

### PUT `/timesheets/{id}`

Update an existing timesheet entry.

**Request Body:** Timesheet entity with updated fields.

**Response Body:** Updated Timesheet entity.

### DELETE `/timesheets/{id}`

Delete a timesheet entry.

**Response Body:** Confirmation message.

### POST `/accessrequests`

Create a new access request.

**Request Body:** AccessRequest entity with required fields (employee_id, project_id, start_date, end_date).

**Response Body:** Created AccessRequest entity.

### PUT `/accessrequests/{id}`

Update an existing access request.

**Request Body:** AccessRequest entity with updated fields.

**Response Body:** Updated AccessRequest entity.

### DELETE `/accessrequests/{id}`

Delete an access request.

**Response Body:** Confirmation message.

## 4. Component Breakdown

### EmployeeService

**Responsibility:** Manages employee data and operations.

**Depends on:** Database

### ProjectService

**Responsibility:** Manages project data and operations.

**Depends on:** Database

### AllocationService

**Responsibility:** Manages allocation data and operations.

**Depends on:** Database

### TimesheetService

**Responsibility:** Manages timesheet data and operations.

**Depends on:** Database

### AccessRequestService

**Responsibility:** Manages access request data and operations.

**Depends on:** Database

### AuthenticationService

**Responsibility:** Handles user authentication and authorization.

**Depends on:** Database

### NotificationService

**Responsibility:** Sends notifications and alerts.

**Depends on:** EmailService, SMSService

### DashboardService

**Responsibility:** Provides real-time dashboards and reports.

**Depends on:** EmployeeService, ProjectService, AllocationService, TimesheetService, AccessRequestService

## 5. Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React |
| Backend | Spring Boot |
| Database | PostgreSQL |
| Infrastructure | Docker, Kubernetes |

## 6. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Unavailability or mismatch of HROne mock data | Medium | Use sample schemas aligned with expected HROne structure. |
| Jira timesheet data not available or incomplete | High | Use mocked Jira worklogs with realistic data patterns. |
| Dependency between modules causing delays | Medium | Follow dependency-aware delivery and phased development. |
| Scope creep during implementation | Medium | Provide a section after project creation to clearly inform about in-scope and out-of-scope deliverables and any extra cost attached to them. |
| Performance issues with reports | Low | Use indexing, caching, and background processing. |
| Security gaps in access control | High | Enforce RBAC, audit logs, and secure authentication. |

## 7. Open Questions

- What all access can be granted and what amount of data is available?
- How to include scope creep, reusable and non-reusable customization, flag extra efforts, calculation of estimated efforts?
- Gamifying Timesheet Entry – create a leaderboard
