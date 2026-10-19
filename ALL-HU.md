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
# HU - 002 – View Tasks
## User history
As a member of the team, i want to see the tasks registered by other members and myself.

# Acceptance Criteria
### CA-002 – Display details
Given that the user request to see the tasks
When displaying them
Then the tasks must show the title
And they must also display a brief part of the description Max 40 characters

### CA-002 - New tasks
Given that a new task was correctly added
And it's marked with a state 
When the task is displayed
Then the task must be on the section corresponding to its state
And displayed correctly

### CA-003 - Updated Tasks
Given that a user updates a task
And changes at least one of the attributes
When the editing is done
Then the task must be update visually in the display board
and they must be on the corresponding section to their state.


## Business rules
RN-001: All boards must have sections.
RN-002: The sections must correspond to all the possible states of a task.
RN-003: The boards must be up to date with the latest modifications.
RN-004: All tasks must belong to a board.
RN-005: A board can be empty.

## dependencies
This history depends on the user histories for creating tasks, updating tasks, and updating the states of such tasks. 
## Out of Scope 
* Limiting task visibility to members of a team.
* Limiting board visibility to members of a team.
* Interaction with the tasks.
* Drag and drop.
* Check visibility permissions.
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
# HU - 005 - Persist Tasks Between Sessions
## User history
As a user i want to be able to close the web page and open it again later with all of the same information available.

# Acceptance Criteria

### CA-001 - Start the storage
Given that the user wants to use the software
And there is data saved on the device
When the user starts the software
Then the data must be loaded into the current state
And we must start logging events onto it

### CA-002 - No storage currently
Given that the user wants to use the software
And there is no local storage saved
When the user starts the software
Then the storage must be started on an empty format
And we must start logging events onto it

## Business rules
RN-001: All updates must be saved
RN-002: The saved information must contain every required detail for the different components
RN-003: No changes get saved until they are successful.
RN-004: No new tasks get saved until they are with the right data.
RN-005: All tasks with invalid info do not get saved.

## dependencies
This history does not depends on:
* HU-001
* HU-002
* HU-003
* HU-004

## Out of Scope 
* Individual storage
* Save task drafts
* Save edit drafts
* Create multiple backups
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
# HU - 007 – Search and filter tasks
## User history
As a team member, i want to search and filter the task list so i can quickly find the tasks that are relevant to me.

# Acceptance Criteria

### CA-001 - Search by text
Given that the user wants to find a task in the list
And they type a keyword in the search field
When they apply the search
Then only the tasks whose title or description contain the entered text must be displayed
And the list must update immediately.

### CA-002 - Filter by status
Given that the user wants to view tasks according to their progress state
And they select a status filter
When they apply the filter
Then only the tasks that match that status must be shown
And the other tasks must remain hidden until the filter is cleared.

### CA-003 - Clear filters
Given that the user has applied a search or a status filter
When they clear the filters
Then the full list of tasks must be restored
And the search fields must return to their empty state.

## Business rules
RN-001: The search must compare the typed value against the task title and description.
RN-002: The status filter must only accept valid task states.
RN-003: Search and filter operations must not modify task data.
RN-004: If the search field is empty, the system must show all tasks.
RN-005: A task must remain visible if it matches the active filters.
RN-006: Search must be case insensitive.

## dependencies
This history depends on:
* HU-002
* HU-004

## Out of Scope 
* Saved searches
* Advanced  filters
* Regex search
* Select multiple results
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
