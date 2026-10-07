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
