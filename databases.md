# Databases

[Home](index.md) | [Software Design and Engineering](software-design-and-engineering.md) | [Algorithms and Data Structures](algorithms-and-data-structures.md)

---

## Enhancement Overview

For the Databases enhancement, I improved the Event Tracker's database structure, password security, user-event relationships, and data access.

The enhancement replaces plaintext password storage with salted password hashes, connects events to individual user accounts, adds database constraints and indexes, and introduces migration logic that preserves existing data when the database is upgraded. Each authenticated user can now view and manage only their own events.

### Files Enhanced

- `DatabaseHelper.java`
- `MainActivity.java`
- `EventsActivity.java`

### New File

- `PasswordHasher.java`

### Artifact Files

[Download Original Event Tracker](artifacts/Original_EventTrackerMarcelo.zip)

[Download Database Enhancement](artifacts/EnhancementThree_EventTrackerMarcelo.zip)

---

## Narrative

The artifact I selected is my Event Tracker Android application from CS 360: Mobile Architecture and Programming. I originally created the app to allow users to create an account, log in, add events, view saved events, update events, delete events, and request SMS permission for reminders. After completing the software design and engineering and algorithms and data structures enhancements, the application had a cleaner structure, an easier event workflow, and features for searching, filtering, sorting, and conflict detection. For this third enhancement, I focused on improving the database structure, password security, user-event relationships, and data access.

I selected this artifact for my ePortfolio because it provides a practical way to demonstrate database skills within a working Android application. In the earlier version, passwords were stored as plaintext, events were not connected to individual users, and a database version change would delete the existing tables and recreate them. These issues limited the security and reliability of the application. I improved the users table so it stores a password hash and unique salt instead of the original password. I also added a user ID to each event and created a foreign-key relationship between the users and events tables. As a result, each account can now view and manage only its own events.

The database structure was also improved with required fields, a case-insensitive unique username constraint, foreign-key enforcement, and indexes that support user and event lookups. Login now returns the authenticated user's database ID, which is passed to the event screen and included in event queries, updates, and deletions. This prevents one user from viewing or changing another user's records. I also replaced the original destructive upgrade process with migration logic that converts existing plaintext passwords into salted hashes and preserves existing data when the database moves to the new version. Because the earlier schema did not record event ownership, older events are assigned to the earliest existing account during migration. This was a necessary trade-off that allowed the records to be preserved instead of deleted.

The files enhanced for this milestone were `DatabaseHelper.java`, `MainActivity.java`, and `EventsActivity.java`. I also added the new `PasswordHasher.java` helper class. `DatabaseHelper.java` now manages the improved schema, migration, constraints, indexes, authentication, and user-specific event operations. `MainActivity.java` authenticates the account and passes the user ID to the event screen. `EventsActivity.java` keeps the features from the previous enhancement while limiting every database operation to the authenticated user. No layout files were changed for this enhancement.

This enhancement supports the course outcomes I planned in Module One. It most directly supports the outcome related to using well-founded tools and techniques to implement a computing solution that delivers value. I used SQLite, Java, foreign keys, indexes, constraints, migration logic, and password hashing to improve the application. It also supports the security outcome because plaintext passwords are no longer stored, database operations are limited by user ID, and the schema reduces the risk of invalid or unauthorized data access. The enhancement also supports the outcome related to evaluating computing solutions because I had to consider the trade-off between preserving older events and the fact that the original database did not contain enough information to determine their owners. I did not need to change my planned outcome coverage because the completed work matches the user-event relationship, password handling, and database organization improvements identified in Module One.

While enhancing the artifact, I learned that changing a database affects more than the table definitions. The login process, screen navigation, queries, updates, and deletions all had to work together with the new user relationship. One challenge was creating a migration that improved the schema without simply deleting the existing database. Another challenge was making sure that all the features from the previous enhancement continued to work after events became user-specific. Testing with two separate accounts helped confirm that each user could see only their own events while searching, sorting, filtering, updating, and deleting still worked correctly. Overall, this enhancement helped me practice database design, schema migration, secure password storage, access control, and the integration of database changes into a working mobile application.

---

[Back to ePortfolio Home](index.md)
