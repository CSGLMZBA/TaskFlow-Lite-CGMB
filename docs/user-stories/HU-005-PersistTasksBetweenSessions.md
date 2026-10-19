# HU - 005 - Persist Tasks Between Sessions
## User history
As a user i want to be able to close the web page and open it again later with all of the same information available.

# Acceptance Criteria

### CA-001 - Start the storage
Given that the user wants to use the software
And there is data saved on the device
When the user starts the software
Then the data must be loaded into the current state
And we must start saving the data onto it

### CA-002 - No storage currently
Given that the user wants to use the software
And there is no local storage saved
When the user starts the software
Then the storage must be started on an empty format
And we must start saving the data onto it

### CA-003 - Invalid storage
Given that on trying to read or write to the local storage
And The program is unable to because the data is malformed
Then The user must be notified 
And a backup must be loaded if available
Otherwise we must save the corrupted data to the most recent backup
And then initialize a blank storage

### CA-004 - backups
Given that there is data on current local storage
And There has been a period longer than 30 minutes without backups
Then the system must create a backup with the data with its timestamp on it
And the system must check how many backups there are
If there are already 7 backups
Then the oldest backup must be deleted
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