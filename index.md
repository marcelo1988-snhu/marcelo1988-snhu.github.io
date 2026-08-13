# Marcelo Martinelli - CS 499 ePortfolio

Welcome to my CS 499 Computer Science Capstone ePortfolio.

This portfolio presents my growth throughout the Computer Science program through my professional self-assessment, code review, and enhancements to the Event Tracker Android application in software design and engineering, algorithms and data structures, and databases.

[Professional Self-Assessment](#professional-self-assessment) | [Code Review](#code-review) | [Software Design and Engineering](software-design-and-engineering.md) | [Algorithms and Data Structures](algorithms-and-data-structures.md) | [Databases](databases.md)

---

## Professional Self-Assessment

When I started the Computer Science program, I mainly thought about the technical side of the field: writing code, building applications, and learning how different technologies work. By the end of the program, my view of computer science had become broader. I now see software as part of a larger system that includes users, data, security, infrastructure, communication, and the decisions made by the people responsible for it. Developing this ePortfolio gave me an opportunity to bring those areas together and show not only what I can build, but also how I approach problems and improve existing systems.
One of the strengths I developed throughout the program is the ability to look at a problem from both a technical and practical perspective. I enjoy understanding how something works, finding where it can be improved, and turning that into a solution that makes sense for the people using it. That is one reason I am interested in areas such as software development, technical support, and systems analysis. These roles require technical knowledge, but they also require patience, troubleshooting, communication, and the ability to understand what the user or organization actually needs. My coursework helped me strengthen those skills and gave me a better foundation for moving into a more technical role.

My professional experience has also influenced the way I think about collaboration. In my current work, I often help coordinate technology-related tasks involving employees, management, local technicians, and outside IT teams. During server, firewall, and network projects, for example, there are usually several people responsible for different parts of the work. My role may involve confirming equipment status, communicating what has already been completed, helping identify a problem, or making sure the right information reaches the right person. These experiences have shown me that collaboration in computer science is not limited to developers working together on the same source code. A technical project can fail just as easily because of unclear communication or missing information as it can because of a programming error. Good collaboration means creating an environment where people with different responsibilities and levels of technical knowledge can contribute to the same goal.

Communication has been another important part of my development. Throughout the program, I had to explain technical ideas in different ways depending on the audience and assignment. In this capstone, the code review required me to walk through an existing application, identify weaknesses, and explain planned improvements in a way that another developer or manager could follow. The milestone narratives required a different approach because they focused more on the reasoning behind the changes and what I learned from them. GitHub, code comments, written assignments, and video presentations all required different forms of communication. My professional work reinforces the same lesson because a detailed technical explanation may be appropriate for an IT specialist but not for someone who simply needs to know what a problem means and what action is required.

The program also strengthened my understanding of data structures and algorithms. I learned that choosing how information is represented can affect everything that happens later in an application. In the Event Tracker, moving to an Event object and an ArrayList<Event> made it possible to keep each event's information together while supporting searching, filtering, sorting, and conflict detection. One of the more useful lessons from that work was that an algorithm cannot be considered separately from the rest of the application. Sorting a list correctly was only part of the problem. The application also had to preserve the connection between the item displayed to the user and the correct database record when that item was updated or deleted. That type of problem helped me understand the practical side of designing and evaluating computing solutions instead of thinking about algorithms only as classroom exercises.

Other coursework gave me experience beyond the artifact used in this portfolio. In CS 370, I worked with artificial intelligence concepts through neural network and reinforcement learning projects, including image classification and the Cartpole problem. These projects introduced me to a different type of computing problem, where the result may depend on training, data, and repeated feedback rather than only a fixed sequence of instructions. They also reinforced many of the same fundamentals I used elsewhere in the program: organizing data, selecting an approach, testing results, identifying limitations, and deciding whether the output actually solves the intended problem. Exposure to these areas increased my interest in how newer technologies such as artificial intelligence can be applied to practical systems without losing sight of reliability, security, or the user.

Software engineering and database development became especially important during the capstone because I was able to revisit an application I had already completed and look at it with more experience. Instead of starting over, I had to decide what was worth changing and what should remain intact. I improved the structure of the application, separated responsibilities, strengthened validation, and made the event workflow easier to use. Later, I redesigned important parts of the database so events belonged to individual users, database relationships were enforced, indexes and constraints were added, and upgrades could preserve existing information instead of simply deleting the old tables. This process taught me that improving an existing system can require more judgment than creating a first version because every change can affect functionality that already works.

Security became part of that same decision-making process. The original application stored passwords in plaintext and did not associate events with the account that created them. Those choices were acceptable for demonstrating basic functionality in an earlier course, but they became obvious weaknesses when I reviewed the application more critically. I replaced plaintext passwords with salted hashes, restricted event operations to the authenticated user, strengthened validation, and used database constraints to protect the consistency of stored information. The biggest lesson for me was that security is easier to manage when it is considered as part of the design. Authentication, data ownership, validation, permissions, and future database changes all influence each other, so security cannot be treated as one feature added at the end.

The artifacts in this portfolio show that progression. I used the same Event Tracker application for all three enhancement categories because I wanted the portfolio to show how one working application could evolve instead of presenting three unrelated projects. The Software Design and Engineering enhancement focuses on structure, maintainability, and usability. The Algorithms and Data Structures enhancement focuses on how event data is represented, searched, filtered, sorted, and compared. The Database enhancement focuses on data relationships, authentication, migration, access control, and security. The code review provides the starting point by showing the original application and the reasoning behind the planned improvements. The narratives that follow each enhancement explain what changed, the decisions involved, and what I learned during the process.

Completing the Computer Science program has given me a stronger technical foundation, but it has also made me more comfortable with the fact that technology constantly changes. I do not expect to enter the field knowing every programming language, framework, platform, or tool. What I can bring is the ability to learn a system, identify a problem, research possible solutions, make reasonable design decisions, test the result, communicate with the people involved, and continue improving the solution as requirements change. That combination of technical knowledge, communication, practical problem-solving, and willingness to keep learning is what I believe best represents my growth through the program and the work presented in this ePortfolio.


---

## Code Review

In this code review, I examine the original Event Tracker Android application, explain its existing functionality, identify areas for improvement, and describe the planned enhancements in software design and engineering, algorithms and data structures, and databases.

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe
    src="https://www.youtube.com/embed/SbgaynQ2524"
    title="CS 499 Event Tracker Code Review"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
</div>

[Watch the code review directly on YouTube](https://youtu.be/SbgaynQ2524)

---

## Selected Artifact

My selected artifact is the Event Tracker Android application from CS 360: Mobile Architecture and Programming. I used the same artifact for all three enhancement categories so the portfolio shows how one application improved throughout the capstone.

The original application allowed users to create an account, log in, and add, view, update, and delete events using a local SQLite database.

---

## Artifact Enhancements

### Software Design and Engineering

This enhancement focused on improving the structure, maintainability, and usability of the Event Tracker application.

[View Software Design and Engineering Enhancement](software-design-and-engineering.md)

### Algorithms and Data Structures

This enhancement focused on improving how event data is represented, searched, filtered, sorted, and compared.

[View Algorithms and Data Structures Enhancement](algorithms-and-data-structures.md)

### Databases

This enhancement focused on improving database structure, user-specific data access, password security, and database migration.

[View Database Enhancement](databases.md)

---

## Source Code

The complete Event Tracker project and its development history are available in the source-code repository.

[View the CS 499 Event Tracker Repository](https://github.com/marcelo1988-snhu/CS499-EventTracker)
