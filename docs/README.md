Workspace Reservation Management (WRM) - Sprint 1
Project Overview
Workspace Reservation Management (WRM) is a custom ServiceNow application designed to streamline the process of reserving office workspaces, managing workspace inventory, and tracking maintenance activities.
The solution provides employees with a self-service experience for reserving desks, meeting rooms, and collaboration spaces while enabling facilities teams to efficiently manage reservations and workspace-related issues from a centralized platform.
This repository contains the Sprint 1 implementation of the project.
________________________________________
Sprint 1 Objectives
The primary objective of Sprint 1 was to establish the application foundation by building:
•	Core data model
•	Role-based access structure
•	Workspace inventory management
•	Reservation management
•	Maintenance tracking
•	Service Catalog request entry point
•	Agent workflow actions
•	Form automation and validation
________________________________________
Solution Architecture
Application Scope
Application Name: Workspace Reservation Management
Scope:
x_2057477_wrm
Roles
Role	Purpose
wrm_user	Submit workspace reservation requests
wrm_agent	Process reservations and maintenance activities
wrm_admin	Manage workspace inventory and administration
________________________________________
Data Model
Workspace Options
Stores all reservable workspaces.
Key Attributes
•	Workspace Name
•	Workspace Type
•	Location
•	Status
•	Maximum Occupancy
•	Description
•	Image
Supported Workspace Types
•	Hot Desk
•	Focus Room
•	Collaboration Space
•	Meeting Room
________________________________________
Reservation Tracker
Extends the ServiceNow Task table and serves as the operational reservation record.
Key Attributes
•	Request Number
•	Workspace
•	Reserved For
•	Reservation Status
•	Start Date/Time
•	End Date/Time
•	Purpose of Visit
•	Additional Notes
Reservation Lifecycle
Pending Check-In
      ↓
   Checked-In
      ↓
  Checked-Out
Alternative path:
Pending Check-In
      ↓
    No-Show
________________________________________
Workspace Maintenance
Tracks maintenance and corrective actions related to workspaces.
Key Attributes
•	Reservation
•	Workspace
•	Workspace Status
•	Ticket Status
•	Date Reported
•	Issue Description
•	Assignment Group
•	Assigned To
________________________________________
Features Implemented
Workspace Inventory Management
•	Workspace inventory table
•	Workspace categorization
•	Occupancy tracking
•	Location management
•	Workspace status management
•	Image support
Reservation Management
•	Reservation tracking
•	Task-based workflow design
•	Related list relationships
•	Agent processing views
•	Personal reservation queues
Maintenance Management
•	Maintenance ticket creation
•	Maintenance assignment process
•	Maintenance team routing
•	Workspace issue tracking
Form Automation
Implemented UI Policies to:
•	Make key reservation fields read-only
•	Dynamically show and hide fields
•	Improve data quality
•	Reduce accidental modifications
UI Actions
Custom server-side UI Actions were developed to support reservation processing:
Check-In
Updates reservation status to Checked-In.
Check-Out
Updates reservation status to Checked-Out and closes the reservation.
No-Show
Allows agents to close reservations that were never used.
Claim
Assigns reservations and maintenance tickets to the current user.
Needs Maintenance
Creates a Workspace Maintenance record directly from a completed reservation.
________________________________________
Service Catalog
A custom catalog item was developed to provide a self-service booking experience.
Workspace Reservation Request
Users can:
•	Select available workspaces
•	Choose reservation dates
•	Specify location
•	Provide purpose of visit
•	Submit workspace reservation requests
Validation
•	Required fields enforced
•	Available workspace filtering
•	User auto-population
________________________________________
Technical Skills Demonstrated
This sprint demonstrates practical experience with:
•	Scoped Application Development
•	Custom Table Design
•	Task Table Extension
•	Role-Based Security
•	Service Catalog Development
•	Reference Qualifiers
•	UI Policies
•	UI Actions
•	GlideRecord Scripting
•	Related Lists
•	Form Configuration
•	List Configuration
•	Data Import and Transformation
•	ServiceNow Application Navigation
________________________________________
Key Challenges and Lessons Learned
One of the most valuable learning experiences during this sprint involved troubleshooting server-side UI Actions responsible for creating Workspace Maintenance records.
The issue required:
•	GlideRecord debugging
•	System log analysis
•	Reference field validation
•	Choice value verification
•	End-to-end testing
This reinforced the importance of validating data relationships and testing business logic with realistic datasets.
________________________________________
Sprint 1 Deliverables
✅ Scoped Application
✅ Role Structure
✅ Workspace Options Table
✅ Reservation Tracker Table
✅ Workspace Maintenance Table
✅ Application Navigation
✅ Related Lists
✅ UI Policies
✅ UI Actions
✅ Service Catalog Item
✅ Workspace Inventory Data
________________________________________
Planned Sprint 2 Enhancements
•	Flow Designer automation
•	Reservation approval workflows
•	Workspace availability automation
•	Notification framework
•	Reporting and dashboards
•	Reservation lifecycle automation
•	Enhanced maintenance workflows
________________________________________
Author
Franklin Nana Yaw Smith
ServiceNow Certified System Administrator (CSA)
Workspace Reservation Management Project - Sprint 1


