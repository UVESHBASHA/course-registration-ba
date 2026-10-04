# 7. UAT Test Cases

Also available as a spreadsheet: [test-cases/UAT_Test_Cases.csv](../test-cases/UAT_Test_Cases.csv)

Status is filled in during a walkthrough of the wireframes ([08_Wireframes.md](08_Wireframes.md)).

| ID | Requirement | Scenario | Steps | Expected result |
|---|---|---|---|---|
| TC-01 | FR-01 | Valid and invalid login | 1. Enter valid credentials. 2. Log out. 3. Enter a wrong password. | Valid: role home page shown. Invalid: error shown, no access. |
| TC-02 | FR-02 | Search by course code | 1. Open the catalog. 2. Enter a course code. 3. Click Search. | Matching course is listed. |
| TC-03 | FR-03 | View course details | 1. Open the catalog. 2. Click a course. | Credits, schedule, faculty, seats left, and prerequisites are shown. |
| TC-04 | FR-04 | Register within the window | 1. Log in as student. 2. Select an open course. 3. Click Register. | Course is added to my list and a confirmation is shown. |
| TC-05 | FR-05 | Register for a full course | 1. Select a course with no seats. 2. Click Register. 3. Accept the waitlist. | Waitlist is offered; waitlist position is shown after joining. |
| TC-06 | FR-06 | Timetable clash | 1. Hold a course. 2. Register for another with an overlapping time. | Registration blocked; clashing course is named. |
| TC-07 | FR-07 | Missing prerequisite and credit limit | 1. Register for a course without its prerequisite. 2. Register for a course that exceeds the credit limit. | Both blocked with the specific reason shown. |
| TC-08 | FR-08 | Drop within the window | 1. Open my registered courses. 2. Click Drop on one. | Course removed, seat released, confirmation shown. |
| TC-09 | FR-09 | Faculty class list | 1. Log in as faculty. 2. Open own course. | Only enrolled students are listed. |
| TC-10 | FR-10 | Admin manages a course | 1. Log in as admin. 2. Create a course. 3. Edit its seat limit. 4. Close it. | Changes appear in the catalog; closed course rejects registration. |
| TC-11 | FR-11 | Notification | 1. Register for a course. 2. Drop it. | A notification is received for each action. |
| TC-12 | FR-12 | Enrolment report | 1. Log in as admin. 2. Choose a department. 3. Export the report. | Report shows enrolled and waitlisted counts. |

## Findings

UAT was performed as a walkthrough of the low-fidelity wireframes in 08_Wireframes.md on 04-Oct-2026. Result: 5 Pass, 4 Fail, 3 Not covered.

| Test Case | Status | Gap found |
|---|---|---|
| TC-01 | Not covered | No login screen is drawn |
| TC-07 | Fail | No message for exceeding the semester credit limit |
| TC-08 | Fail | No drop confirmation message |
| TC-09 | Not covered | No faculty class list screen |
| TC-10 | Fail | No create/edit course form and no "course closed" message on the student side |
| TC-11 | Not covered | No notification screen or message |
| TC-12 | Fail | No enrolment report layout |

### Recommended changes
- Add a login wireframe with an error state for invalid credentials (TC-01).
- Add a "Credit limit exceeded: you can register up to X credits" message to screen 8.2 (TC-07).
- Add a "Course dropped successfully" confirmation to screen 8.3 (TC-08).
- Add a faculty screen listing enrolled students for a course (TC-09).
- Add create/edit course forms to the admin screen and a "Registration closed for this course" message on the student side (TC-10).
- Add notification messages for both registration and drop actions (TC-11).
- Add an enrolment report layout showing enrolled and waitlisted counts (TC-12).
