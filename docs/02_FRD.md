# 2. Functional Requirements Document (FRD)

## 2.1 Functional Requirements
| ID | Requirement | MoSCoW | Objective |
|---|---|---|---|
| FR-01 | Role-based login for student, faculty, and admin | Must | BO-3 |
| FR-02 | Search and filter the course catalog by code, name, department, faculty, and semester | Must | BO-1 |
| FR-03 | Show course details: credits, schedule, faculty, seats left, prerequisites | Must | BO-1 |
| FR-04 | Allow a student to register for a course during the registration window | Must | BO-1 |
| FR-05 | Check seat availability and add the student to a waitlist if the course is full | Should | BO-2 |
| FR-06 | Detect timetable clashes and block the registration with a clear message | Must | BO-2 |
| FR-07 | Validate prerequisites and the semester credit limit before confirming | Must | BO-2 |
| FR-08 | Allow a student to drop a course within the drop window | Must | BO-1 |
| FR-09 | Allow faculty to view the list of students enrolled in their courses | Should | BO-3 |
| FR-10 | Allow admin to create, edit, and close courses and set seat limits | Must | BO-3, BO-4 |
| FR-11 | Send in-app or email notification on registration, drop, and waitlist promotion | Should | BO-4 |
| FR-12 | Allow admin to generate and export enrolment reports | Could | BO-3, BO-5 |

## 2.2 Business Rules
- BR-1: Registration is allowed only inside the registration window.
- BR-2: A student cannot exceed the semester credit limit.
- BR-3: A student must have completed all listed prerequisites.
- BR-4: A student cannot hold two courses with overlapping schedules.
- BR-5: Seats cannot exceed the limit set by the admin; extra students go to the waitlist.
- BR-6: Drops are allowed only inside the drop window, and the seat is released immediately.

## 2.3 Non-Functional Requirements
| ID | Requirement |
|---|---|
| NFR-1 | Performance: pages respond promptly under peak registration load |
| NFR-2 | Security: role-based access; students can act only on their own registrations |
| NFR-3 | Auditability: every registration, drop, and override is logged with user and time |
| NFR-4 | Usability: a student can register in a few steps without training |

## 2.4 Roles
| Role | Main actions |
|---|---|
| Student | Search, register, drop, join waitlist, view own timetable |
| Faculty | View class lists for own courses |
| Admin | Manage courses and seat limits, generate reports, handle exceptions |
