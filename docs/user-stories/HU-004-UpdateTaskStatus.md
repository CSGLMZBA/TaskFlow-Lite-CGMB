# HU - 004 – Update Task Status
## User history
As a member of the team, update the status of a task to communicate progress on the project.

# Acceptance Criteria

### CA-000 - Task exists
Given that the user desires to update a task status
And the task doesn't exists
When they try to update the task status
Then the task status must not be updated
And they must receive information that the task is not valid.

### CA-001 – Update
Given that the user wants to update a task status
And selects a valid status
When requesting the task status updating
Then the task status must be updated

### CA-002 - Invalid status
Given that the user wants to update a task status
And somehow selects an invalid status
When requesting the task status updating
Then the task status must not be updated
And they must receive information indicating that the status is not valid.

### CA-003 - Out of date
Given that the user desires to update a task status
And selects a valid status
When the task/task status has been updated
Then the task status must not be updated
and they must be informed that the task is out of date before refreshing

## Business rules
RN-001: All tasks must have a status
RN-002: The tasks statuses are limited to : "Pending, Working, Overdue, Frozen, Completed"
RN-003: The status can only be updated via selector.
RN-004: Tasks can't be updated to invalid statuses.
RN-007: The las update time of the task status must be available.

## dependencies
This history depends on:
* Create Task HU 001

## Out of Scope 
* Update task details.
* Delete Tasks.
* Full task history.
* Check permissions.