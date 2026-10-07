# HU - 008 – Assign tasks to team members
## User history
As a member of the team, i want to assign each task to a responsible team member so that the workflow is clear.

# Acceptance Criteria

### CA-001 - Assign a task
Given that the user wants to assign responsibility for a task
And the task exists
And the selected team member exists
When they assign the task to that member
Then the task must show that team member as its owner
And the assignment must be stored correctly

### CA-002 - Update assignment
Given that a task already has an assigned member
And the user changes the assignment to another valid team member
When the assignment is saved
Then the task must display the new assigned member
And the previous assignment must no longer be assigned to it

### CA-003 - Remove assignment
Given that a task has an assigned member
When the user removes the assignment
Then the task must become unassigned
And the system must show that no team member is currently responsible for it.

### CA-004 - Invalid assignment
Given that the user attempts to assign a task to an invalid member
When they save the assignment
Then the task must not be assigned
And the user must receive a message indicating that the assignment isn't valid

## Business rules
RN-001: Each task may only have one assigned team member or none
RN-002: Assignment values must be validated before being saved
RN-003: Changes to assignment must be persistent across the current session and saved state.
RN-004: Tasks without a valid assigned member are still valid
RN-005: The assignment must be visible in the task details

## dependencies
This history depends on:
* HU-001
* HU-002
* HU-003

## Out of Scope 
* Team creation and deletion
* User permissions and roles
* Notifications sent to assigned members
* Assignment History
* Assignment to many members
