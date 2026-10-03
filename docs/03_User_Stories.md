# 3. User Stories and Acceptance Criteria

**US-01 (FR-01)** As a user, I want to log in with my role so that I only see features meant for me.
- Given valid credentials, when I log in, then I land on my role's home page.
- Given invalid credentials, when I log in, then I see an error and no access is granted.

**US-02 (FR-02)** As a student, I want to search and filter courses so that I can find the ones I need quickly.
- Given I enter a course code or name, when I search, then matching courses are listed.
- Given I apply a department filter, then only that department's courses appear.

**US-03 (FR-03)** As a student, I want to see course details so that I can decide before registering.
- When I open a course, then credits, schedule, faculty, seats left, and prerequisites are shown.

**US-04 (FR-04)** As a student, I want to register for a course so that it is added to my timetable.
- Given the window is open and all checks pass, when I register, then the course appears in my registered list and I get a confirmation.
- Given the window is closed, when I try to register, then I see a "registration closed" message.

**US-05 (FR-05)** As a student, I want to join a waitlist when a course is full so that I can get a seat if one opens.
- Given a course has no seats, when I register, then I am offered the waitlist.
- Given a seat opens, then the first waitlisted student is registered and notified.

**US-06 (FR-06)** As a student, I want clashes flagged so that I do not register for overlapping classes.
- Given a course overlaps one I already hold, when I register, then the system blocks it and names the clashing course.

**US-07 (FR-07)** As a student, I want prerequisites and credit limits checked so that my registration is valid.
- Given I lack a prerequisite, then registration is blocked and the missing course is named.
- Given registering would exceed my credit limit, then registration is blocked and the limit is shown.

**US-08 (FR-08)** As a student, I want to drop a course so that I can fix a mistake.
- Given the drop window is open, when I drop, then the seat is released and I get a confirmation.
- Given the drop window is closed, then the drop is not allowed.

**US-09 (FR-09)** As a faculty member, I want to see my class list so that I know who is enrolled.
- When I open my course, then I see the currently enrolled students only.

**US-10 (FR-10)** As an admin, I want to manage courses so that the catalog stays current.
- When I create or edit a course, then the change appears in the student catalog.
- When I close a course, then no new registrations are accepted.

**US-11 (FR-11)** As a student, I want notifications so that I know the result of my actions.
- When I register, drop, or am promoted from the waitlist, then I receive a notification.

**US-12 (FR-12)** As an admin, I want enrolment reports so that I can monitor demand.
- When I choose a course or department and export, then a report with enrolled and waitlisted counts is produced.
