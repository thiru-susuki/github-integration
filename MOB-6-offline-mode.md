# MOB-6 Offline Mode

## Overview
Enable the mobile app to function without an active internet 
connection by caching critical data locally on the device.

## Technical Approach
- Use SQLite / Room database for local data persistence
- Implement sync queue for actions taken while offline
- Show clear offline indicator in the app UI
- Auto-sync when connectivity is restored

## Acceptance Criteria
- [ ] User can view last synced data without internet
- [ ] Actions taken offline are queued and synced on reconnect
- [ ] Conflict resolution handled when same record edited online and offline
- [ ] Offline banner shown at top of screen when no connection

## Notes
- Priority data to cache: tasks, user profile, recent activity
- Max local storage usage should not exceed 50MB
