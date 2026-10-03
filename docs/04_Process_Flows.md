# 4. Process Flows

Diagrams are written in Mermaid and render automatically on GitHub.

## 4.1 As-Is (manual process)
```mermaid
flowchart TD
    A([Start]) --> B[Student collects paper registration form]
    B --> C[Student checks timetable and prerequisites by hand]
    C --> D[Faculty advisor signs the form]
    D --> E[Admin office enters data into a spreadsheet]
    E --> F{Seat available and no clash?}
    F -- No --> G[Admin contacts student by phone or email]
    G --> H[Student corrects the form]
    H --> D
    F -- Yes --> I[Admin sends class list to faculty by email]
    I --> J([End])
```

## 4.2 To-Be (proposed system)
```mermaid
flowchart TD
    A([Start]) --> B[Student logs in]
    B --> C[Search course catalog]
    C --> D[Select course and click Register]
    D --> E{Registration window open?}
    E -- No --> X1[Show registration closed message]
    E -- Yes --> F{Seat available?}
    F -- No --> W[Offer waitlist]
    W --> N
    F -- Yes --> G{Timetable clash?}
    G -- Yes --> X2[Block and name the clashing course]
    G -- No --> H{Prerequisites met and credit limit OK?}
    H -- No --> X3[Block and show the reason]
    H -- Yes --> I[Confirm registration and update seat count]
    I --> N[Send notification to student]
    N --> J[Faculty and admin see updated lists and reports]
    X1 --> K([End])
    X2 --> K
    X3 --> K
    J --> K
```

## 4.3 Key differences
| Step | As-is | To-be |
|---|---|---|
| Checks | Done by hand, found late | Automatic at submission |
| Communication | Phone and email | Instant notification |
| Class lists | Emailed by admin | Real-time faculty view |
| Record keeping | Spreadsheet | Central audit log |
