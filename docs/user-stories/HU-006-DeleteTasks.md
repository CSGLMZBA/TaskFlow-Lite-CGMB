# HU - 006 – Create a task
## User history
As a member of the team, i want to be able to delete a task.

# Acceptance Criteria

### CA-000 - Task exists
Given that the user desires to delete a task
And the task doesn't exist
When they try to delete the task
Then the task must not be deleted
And they must receive information that the task is not valid.

### CA-001 – Delete
Given that the user desires to delete a task
And the task is valid
When they try to delete the task
Then the task must be deleted
And they must receive information that the task was deleted.

## Business rules
RN-001: Task must exist before being deleted
RN-002: The user must be notified when the task i deleted
RN-003: Deleted tasks cannot be currently recovered

## dependencies
This history depends on:
* HU-001

## Out of Scope 
* Task trash container
* undo deletions
* log who deleted the task
* check for permissions to delete tasks