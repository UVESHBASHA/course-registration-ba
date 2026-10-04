# Online Course Registration System: Requirements & Process Analysis

A Business Analysis project that documents the requirements and process redesign for moving a university's manual course registration to an online system. This is a documentation-only project (no code): it shows the BA deliverables from business need to UAT.

**Author:** Uvesh Basha | B.Tech CSE, SRM Institute of Science and Technology

## Problem
Course registration relies on paper forms, spreadsheets, and email. Students cannot see live seat availability, clashes and prerequisite errors are found late, and the admin office spends time on manual checks and corrections.

## What this repo contains
| # | Deliverable | File |
|---|---|---|
| 1 | Business Requirements Document (BRD) | [docs/01_BRD.md](docs/01_BRD.md) |
| 2 | Functional Requirements Document (FRD) | [docs/02_FRD.md](docs/02_FRD.md) |
| 3 | User stories with acceptance criteria | [docs/03_User_Stories.md](docs/03_User_Stories.md) |
| 4 | As-is and to-be process flows | [docs/04_Process_Flows.md](docs/04_Process_Flows.md) |
| 5 | Gap analysis | [docs/05_Gap_Analysis.md](docs/05_Gap_Analysis.md) |
| 6 | Requirement traceability matrix | [docs/06_RTM.md](docs/06_RTM.md), [traceability/RTM.csv](traceability/RTM.csv) |
| 7 | UAT test cases | [docs/07_UAT_Test_Cases.md](docs/07_UAT_Test_Cases.md), [test-cases/UAT_Test_Cases.csv](test-cases/UAT_Test_Cases.csv) |
| 8 | Wireframes (low fidelity) | [docs/08_Wireframes.md](docs/08_Wireframes.md) |
| 9 | Jira backlog import file | [jira/jira_import.csv](jira/jira_import.csv) |

## Summary
- 12 functional requirements (MoSCoW prioritized) plus 4 non-functional requirements
- 12 user stories with Given/When/Then acceptance criteria
- 12 UAT test cases, each traced to a requirement and a user story
- 3 planned sprints

## Approach
1. Define the business problem, objectives, scope, and stakeholders (BRD).
2. Translate objectives into functional requirements (FRD) and prioritize with MoSCoW.
3. Write user stories with acceptance criteria.
4. Model the current (as-is) and proposed (to-be) processes and run a gap analysis.
5. Link every requirement to a user story and a test case (RTM).
6. Define UAT test cases for business users to verify the solution.

## Tools
Markdown, Graphviz diagrams, Excel/CSV for matrices, Jira for the backlog.
