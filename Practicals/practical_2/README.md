Practical 2 Report: UML Use Case & Interaction Overview Diagrams
Module: SDA202 – Software Design and System Architecture
Practical Date: 24/03/2026
Submission Date: [Insert Date Before Next Practical]
Student Name: [Your Name]
Student ID: [Your ID]

1. Introduction
This report is a record of completion of Practical 2, which entails modeling the functional and interaction requirements of a proposed Automated Programming Assignment Grading System for a university’s software engineering course. The practical involved creating two different UML diagrams based on the requirements analysis of the system:

Interaction Overview Diagram (IoD) - from actor-to-actor viewpoint, modeling how these actors interact to achieve a business goal.

Use Case Diagram (UCD) - from a functional viewpoint, modeling how the system’s boundaries, actors, and use cases facilitate interactions.

These diagrams have been completed as per requirements and are referred to in this report. This report is written in accordance with the set format and includes requirements analysis, architectural design decisions, quality attribute analysis, self-reflection, and clarity of presentation.

2. Requirements Analysis
The problem analysis has presented a university setting with more than 300 students enrolled in a software engineering course every year. The current process is GitHub-based for assignment submission and completely manual in grading assignments by cloning repositories and inspecting code manually. The proposed system is expected to automate grading while considering various functional and non-functional requirements.

2.1 Functional Requirements (Use Case derived)
ID	Requirement
FR1	Students upload source code to be executed and graded.
FR2	Grades and execution logs must be persistent and auditable.
FR3	Plagiarism detection: internally and via TurnItIn web service.
FR4	Integration with the existing mainframe-based LMS.
FR5	Professor defines the due date and time. Any assignments turned in after this time will be rejected.
FR6	Students have multiple chances to turn in assignments to increase their grade.
FR7	Professor defines the grading criteria, either through metrics or test cases.
2.2 Key Actors
Actor	Description
Student	Students who will be submitting assignments and viewing their grades.
Professor	Professor who will be assigning deadlines and creating grading criteria.
LMS (External)	Mainframe-based system that holds final grades.
TurnItIn API	External web service used to perform plagiarism detection.
Admin	System administrator who will be maintaining the system.
2.3 Business Outcome
The business outcome for this project is to provide a system that will allow us to continue to have one of the top SWE programs in the country, even with a tight IT budget.



