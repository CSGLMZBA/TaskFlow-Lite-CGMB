# HU - 001 – Create a task
## User history
As a member of the team, i wan to register a new task with title and description, to document the work that i need to do.

# Acceptance Criteria
### CA-001 – Create Correctly
Given that the user provides a valid title
When requesting the task creation
Then the task must be added
And it must start with Pending status

### CA-002 - Required title
Given that the user wants to create a new task
And doesn't provide the title
When they try to register the task
Then the task must not be created
And they must recieve information indicating that the title is required.

### CA-003 - Minimum title length 
Given that the user desires to create a task
And provides a title with less than 3 characters
When trying to register the Task
Then the task must not be created
and they must be informed that the title does not fulfill the minimum length requirement

### CA-004 - Maximum title length
Given that the user desires to create a task
And provides a title with more than 80 characters
When they try to register the task
Then the task must not be created
And they must be informed that the title does not fulfill the maximum length requirement

### CA-005 - Optional description
Given that user provides a valid title
And does not provide a description
When the task is created
Then the task must be created successfully

### CA-006 - Maximum description length
Given that the user provides a description longer than 300 characters
When trying to create the task
Then the task must not be registered
And they must be informed that the description does not fulfill the maximum length restriction

## Business rules
RN-001: All tasks must have a title
RN-002: The title must contain 3-80 characters
RN-003: The description is optional
RN-004: The description has a maximum of 300 characters
RN-005: All new tasks start as pending.
RN-006: Every task must be uniquely identifiable
RN007: The creation time of the task must be accessible

## dependencies
This history does not depends on another HU.

## Out of Scope 
* Assign tasks to people
* Due date
* Priority
* Categories
* Attached Files
* Sub tasks 
* Notifications