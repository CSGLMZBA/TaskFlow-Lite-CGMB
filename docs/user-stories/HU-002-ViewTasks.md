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