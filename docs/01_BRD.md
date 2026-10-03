# 1. Business Requirements Document (BRD)

## 1.1 Background
A university registers students for semester courses using paper forms, spreadsheets, and email. Students cannot see live seat availability, timetable clashes are found late, and the admin office spends significant time on manual checks and corrections.

## 1.2 Problem Statement
The manual registration process is slow, error-prone, and opaque. Students register for full or clashing courses, faculty receive incorrect class lists, and admins re-enter data across multiple files.

## 1.3 Business Objectives
| ID | Objective |
|---|---|
| BO-1 | Let students register and drop courses online within the allowed window |
| BO-2 | Prevent invalid registrations automatically (full course, timetable clash, missing prerequisite, credit limit) |
| BO-3 | Give faculty and admins an accurate, real-time enrolment view |
| BO-4 | Reduce manual data entry and correction work for the admin office |
| BO-5 | Keep a reliable record of every registration change for audit |

## 1.4 Scope
**In scope:** login, course catalog, registration, drop, waitlist, clash and prerequisite validation, faculty class lists, admin course management, notifications, enrolment reports.

**Out of scope:** fee payment, grading, attendance, exam scheduling, mobile app.

## 1.5 Stakeholders
| Stakeholder | Interest |
|---|---|
| Students | Easy, correct registration |
| Faculty | Accurate class lists |
| Admin / Registrar office | Control over courses, fewer manual errors |
| IT department | Maintainable, secure system |
| Department heads | Enrolment visibility |

## 1.6 Assumptions
- Student, faculty, and course master data already exist in the university database.
- Students authenticate with existing university credentials.
- A fixed registration window is defined each semester.

## 1.7 Constraints
- Must work in standard web browsers.
- Must follow university credit-limit and prerequisite rules.

## 1.8 Risks
| Risk | Impact | Mitigation |
|---|---|---|
| Peak load when the window opens | Slow or failed registration | Load testing; staggered slots per batch |
| Incorrect master data | Wrong validations | Validate data before go-live |
| Low user adoption | Manual process continues | Short training and a user guide |

## 1.9 Success Criteria
- Students can complete registration and drop without admin help.
- No registration is accepted that breaks seat, clash, prerequisite, or credit rules.
- Admin can produce an enrolment report on demand.
