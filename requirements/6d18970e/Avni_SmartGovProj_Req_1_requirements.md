# Requirements: Smart Project Governance & Access Control System

## Functional Requirements

### FR1: Establish a centralized, auditable employee master
Establish a centralized, auditable employee master that governs identity, hierarchy, and lifecycle across the organization.

### FR2: Enable structured project creation and controlled visibility
Enable structured project creation and controlled visibility to ensure clear ownership and governance throughout the project lifecycle.

### FR3: Optimize workforce utilization
Optimize workforce utilization by enforcing capacity limits and providing real-time visibility into employee workload.

### FR4: Ensure secure, project-bound, and time-bound access
Ensure secure, project-bound, and time-bound access through approval-driven workflows with full traceability.

### FR5: Capture accurate, compliant effort data
Capture accurate, compliant effort data through controlled time entry and approval processes.

### FR6: Deliver real-time, role-based insights
Deliver real-time, role-based insights to support operational oversight and informed decision-making.

### FR7: Project creation with auto-generated unique Project ID
Project creation with auto-generated unique Project ID (PID).

### FR8: Assignment of Project Owner
Assignment of Project Owner.

### FR9: Project metadata
Project metadata (duration, type, department).

### FR10: Controlled visibility for sensitive fields
Controlled visibility for sensitive fields (e.g., budget for leadership).

### FR11: Mid-project updates
Mid-project updates (dates, scope, allocations).

### FR12: Percentage-based allocation per project
Percentage-based allocation per project.

### FR13: Real-time utilization view per employee
Real-time utilization view per employee.

### FR14: Visual load indicators
Visual load indicators (flag extra efforts).

### FR15: Hard enforcement of 100% utilization cap
Hard enforcement of 100% utilization cap.

### FR16: Heatmap for manager-driven task assignment
Heatmap for manager-driven task assignment using filters.

### FR17: Foundation for future “Best Fit” algorithm
Foundation for future “Best Fit” algorithm.

### FR18: Access request initiation by employees
Access request initiation by employees.

### FR19: Approval workflows
Approval workflows (Employee → Manager → IT/Admin).

### FR20: Project-bound and role-bound access
Project-bound and role-bound access.

### FR21: Time-bound access with auto-expiry
Time-bound access with auto-expiry.

### FR22: Flag orphan access
Flag orphan access.

### FR23: Manual revocation by Manager/Admin
Manual revocation by Manager/Admin.

### FR24: Centralized Access Matrix
Centralized Access Matrix (who has what and why).

### FR25: Comprehensive audit trail for all access actions
Comprehensive audit trail for all access actions.

### FR26: Daily project-wise time entry by employees
Daily project-wise time entry by employees.

### FR27: Billable vs non-billable classification
Billable vs non-billable classification.

### FR28: Manager approval/rejection workflow
Manager approval/rejection workflow.

### FR29: Immutable records
Immutable records (no manager edits).

### FR30: Compliance tracking and reminders
Compliance tracking and reminders.

### FR31: Analytics for utilization and burnout detection
Analytics for utilization and burnout detection.

### FR32: Allocation summary
Allocation summary (who is working on what).

### FR33: Employee utilization views
Employee utilization views.

### FR34: Access matrix dashboard
Access matrix dashboard.

### FR35: Project-wise and employee-wise hours
Project-wise and employee-wise hours.

### FR36: Manager and leadership-level views
Manager and leadership-level views.

## Non-Functional Requirements

- **NFR1**: API response times to remain within acceptable limits for standard user actions.
- **NFR2**: Dashboard pages to load within reasonable time for expected data volumes.
- **NFR3**: Background jobs (allocation calculations, reports) to run without impacting user experience.

## Acceptance Criteria

### AC1 (References: )
- Employee data can be successfully imported and viewed in a People Master screen.

### AC2 (References: )
- Project allocations are system-driven and fully auditable, eliminating manual or meeting-based assignment decisions.

### AC3 (References: )
- Employee overload and underutilization are prevented through enforced percentage-based allocation limits.

### AC4 (References: )
- Clear ownership and accountability are ensured through immutable, approved timesheet records.

### AC5 (References: )
- All system access is project-bound, time-bound, fully audited, and automatically revoked when no longer required.

### AC6 (References: )
- Timesheet data (billable and non-billable) is visible at project and employee level.

### AC7 (References: )
- Reports accurately reflect allocations, access permissions, and project hours.

### AC8 (References: )
- The system is stable, usable, and demonstrable to stakeholders.
