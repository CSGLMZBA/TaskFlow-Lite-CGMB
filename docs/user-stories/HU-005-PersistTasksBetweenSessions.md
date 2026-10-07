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