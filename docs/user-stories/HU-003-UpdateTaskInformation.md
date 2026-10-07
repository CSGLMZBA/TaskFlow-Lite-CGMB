# HU - 003 – Update Task Information
## User history
As a member of the team, i want to update a task task with title or description, to document the work that i need to do.

# Acceptance Criteria

### CA-000 - Task exists
Given that the user desires to update a task
And the task doesn't exists
When they try to updated the task
Then the task must not be updated
And they must receive information that the task is not valid.

### CA-001 – Update
Given that the user provides a valid title
When requesting the task updating
Then the task must be updated

### CA-002 - Required title
Given that the user wants to update a task
And doesn't provide the title
When they try to update the task
Then the task must not be updated
And they must receive information indicating that the title is required.

### CA-003 - Minimum title length 
Given that the user desires update a task
And provides a title with less than 3 characters
When trying to update the Task
Then the task must not be updated
and they must be informed that the title does not fulfill the minimum length requirement

### CA-004 - Maximum title length
Given that the user desires to update a task
And provides a title with more than 80 characters
When they try to update the task
Then the task must not be updated
And they must be informed that the title does not fulfill the maximum length requirement

### CA-005 - Optional description
Given that user provides a valid title
And does not provide a description
When the task is updated
Then the task must be updated successfully

### CA-006 - Maximum description length
Given that the user provides a description longer than 300 characters
When trying to update the task
Then the task must not be updated
And they must be informed that the description does not fulfill the maximum length restriction

## Business rules
RN-001: All tasks must have a title
RN-002: The title must contain 3-80 characters
RN-003: The description is optional
RN-004: The description has a maximum of 300 characters
RN-006: Every task must be uniquely identifiable
RN-007: The las update time of the task must be accessible

## dependencies
This history depends on:
* Create Task HU 001

## Out of Scope 
* Update the status of the task
* Delete Tasks.
* Full task history.
* Check permissions.