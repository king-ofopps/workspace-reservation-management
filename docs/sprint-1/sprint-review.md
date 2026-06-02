# Sprint 1 Review

## Objectives

Build the foundational Workspace Reservation Management application.

## Completed Deliverables

- Scoped Application
- Custom Tables
- Navigation Modules
- Related Lists
- UI Policies
- UI Actions
- Service Catalog Item

## Challenges Encountered

### Needs Maintenance UI Action

Initially appeared not to create maintenance records.

Root cause:
Testing was performed against reservations without workspace references.

Resolution:
Used system logs, GlideRecord debugging, and record validation to identify the issue.

## Lessons Learned

- GlideRecord debugging
- Reference field validation
- Choice values versus labels
- Server-side UI Action troubleshooting
