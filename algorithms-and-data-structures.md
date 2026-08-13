# Algorithms and Data Structures

[Home](index.md) | [Software Design and Engineering](software-design-and-engineering.md) | [Databases](databases.md)

---

## Enhancement Overview

For the Algorithms and Data Structures enhancement, I improved how the Event Tracker organizes, searches, filters, sorts, and compares event data.

The enhancement introduced an object-based structure for events and separated the algorithms from the Activity logic. Users can now search events by title, filter them by date, sort them chronologically, and receive a warning when another event is already scheduled at the same date and time.

### Files Enhanced

- `EventsActivity.java`
- `EventValidator.java`
- `activity_events.xml`

### New Files

- `Event.java`
- `EventAlgorithms.java`

### Artifact Files

[Download Original Event Tracker](artifacts/Original_EventTrackerMarcelo.zip)

[Download Algorithms and Data Structures Enhancement](artifacts/EnhancementTwo_EventTrackerMarcelo.zip)

---

## Narrative

The artifact I selected is my Event Tracker Android application from CS 360: Mobile Architecture and Programming. I originally created the app to allow users to create an account, log in, add events, view saved events, update events, delete events, and request SMS permission for reminders. After completing the software design and engineering enhancement, the app had a cleaner structure and an easier event-selection workflow. For this second enhancement, I focused on improving how the application organizes, searches, filters, sorts, and compares event data.

I selected this artifact for my ePortfolio because it gives me a practical way to demonstrate algorithms and data structures in a working Android application. The original version displayed events using separate lists and provided limited control over how the records were organized. I added an `Event` model so the ID, title, date, and time for each event are stored together in an `ArrayList<Event>`. This is more reliable than maintaining separate lists because each object represents one complete event and the related values remain connected.

I also added an `EventAlgorithms` helper class to separate the algorithms from the screen logic. The enhancement includes a case-insensitive title search, filters for all, upcoming, and past events, and sorting by soonest or latest date and time. I also added conflict detection that checks whether another event already exists at the same date and time before a new event is added or an existing event is updated. The event list now continues to use the correct event object even when the visible results have been searched, filtered, or sorted. I updated `EventsActivity.java` and `activity_events.xml` to support these features, and I strengthened `EventValidator.java` so invalid dates and times, such as February 30 or 25:00, are rejected.

This enhancement supports the course outcomes I planned in Module One. It most directly supports the outcome related to designing and evaluating computing solutions using algorithmic principles and data structures. The application now uses an object-based data structure and algorithms for linear searching, filtering, sorting, and conflict detection. It also supports the use of well-founded tools and techniques because I used Java collections, comparator-based sorting, Android interface components, and date-and-time classes to add useful functionality. Professional communication is also supported through code comments and this narrative, which explain the purpose of the algorithms and the decisions behind the enhancement. I did not need to change my planned outcome coverage because the completed work matches the sorting, searching, filtering, and conflict-detection improvements identified in Module One.

While enhancing the artifact, I learned that adding algorithms to an application also requires careful coordination with the user interface. It was not enough to sort or filter the displayed text because update and delete actions still needed to use the correct database record. Using an `ArrayList<Event>` for the displayed results helped keep each list position connected to the correct event ID. Another challenge was comparing dates that were originally stored as text. Converting the date and time into `LocalDateTime` values made chronological sorting, filtering, and conflict detection more reliable. Overall, this enhancement helped me practice selecting appropriate data structures, separating algorithms from Activity logic, evaluating how different operations affect application behavior, and applying algorithmic concepts to improve a working mobile application.

---

[Back to ePortfolio Home](index.md)
