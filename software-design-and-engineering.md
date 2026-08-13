# Software Design and Engineering

[Home](index.md) | [Algorithms and Data Structures](algorithms-and-data-structures.md) | [Databases](databases.md)

---

## Enhancement Overview

For the Software Design and Engineering enhancement, I improved the structure, maintainability, and usability of my Event Tracker Android application.

The original application worked, but some of the Activity classes contained too much logic, and users had to manually enter an internal event ID to update or delete an event. The enhancement reorganized this workflow so users can select an event directly from the list and separated validation logic from the Activity code.

### Files Enhanced

- `MainActivity.java`
- `EventsActivity.java`
- `activity_events.xml`

### New File

- `EventValidator.java`

### Artifact Files

[Download Original Event Tracker](artifacts/Original_EventTrackerMarcelo.zip)

[Download Software Design and Engineering Enhancement](artifacts/EnhancementOne_EventTrackerMarcelo.zip)

---

## Narrative

The artifact I selected is my Event Tracker Android application from CS 360: Mobile Architecture and Programming. I created this app as a mobile project that allows users to create an account, log in, add events, view saved events, update events, delete events, and request SMS permission for reminders. The original app worked, but the code review helped me see that the design could be improved, especially in the Activity classes and the event update/delete workflow.

I selected this artifact for my ePortfolio because it shows practical software development skills, including Java, Android Studio, user interface design, SQLite use, event management, validation, and permission handling. It is also a good artifact because I can improve it in stages across the capstone categories. For this first enhancement, I focused on software design and engineering by making the app easier to use and easier to maintain.

The main improvement was changing the event workflow so users can select an event from a list before updating or deleting it. In the original version, users had to manually type an internal event ID. That worked technically, but it was not very user-friendly and could lead to errors. I refactored parts of `MainActivity.java` and `EventsActivity.java` into smaller methods, updated `activity_events.xml` to support the new selection-based workflow, and added an `EventValidator` helper class so validation is separated from the Activity logic. These changes make the code cleaner, reduce repeated logic, and make the app feel closer to a real mobile application.

This enhancement supports the course outcomes I planned in Module One. It supports professional communication because the code comments and narrative explain the design changes clearly. It also supports the use of well-founded tools and techniques because I used Java, Android Studio, Android interface components, and software design practices to improve an existing application. It also begins to support a security mindset by reducing user input errors and improving validation, although the larger security work with password handling and database structure will come later.

While enhancing the artifact, I learned that improving software design does not always mean adding many new features. In this case, the better improvement was making the existing features more organized and easier for the user. One challenge was deciding how to improve the app without simply adding extra features. The original issue was more about design quality than missing functionality. By focusing on event selection, validation, and cleaner Activity logic, I was able to make the app easier to use and maintain while keeping the enhancement aligned with software design and engineering. Overall, this enhancement helped me practice refactoring, separating responsibilities, improving validation, and making an existing application more professional.

---

[Back to ePortfolio Home](index.md)
