# Use Cases

---
# Quality Attributes
| ID   |    Quality Attribute       |  Scenario    |    Associated Use Case   |
|:-------------:|:-------------:|:-------------:|-------------|
| QA-1 |  Availability  | The system should be running all the time without interruption. | All |
| QA-2 |  Performance   | The system should accommodate the user’s needs without long wait times or server refresh. | All |
| QA-3 |  Accessibility | The system should be able to let users upload files, send messages to individuals, teams or all course participants at once.  | UC-2, UC-8, UC-10 |
| QA-4 |  Security  | The system allows only students to change study information of others, user login will determine its user privileges and should allow determined access.  | ALL |
| QA-5 | Interoperability | The system provides export to commonly used calendar formats and it should be interoperable with a secondary university system. | ALL |
| QA-6 | Maintainability |  The system should be easily maintainable. | ALL |
| QA-7 |  Testability | The system should be easily testable. | UC-6, UC7, UC12 | 

---
# Constraints
| ID   | Constraint          |
|:-------------:|-------------|
| CON-1 | The system must be able to support a minimum of 50 users at any time. |
| CON-2 | The server must prompt the user when and why the server will be down at minimum a day before going offline. |
| CON-3 | The system must be accessed through a major web browser (Chrome, Firefox, IE8+, Safari) in different Operating Systems: Windows, OSX, and Linux. |
| CON-4 | UI must be consistent on all browsers and Operating Systems. |
| CON-5 | Network connection should still be reliable even if the user has low bandwidth. |
| CON-6 | The system must prompt Users/Administrators to log-in before any other action can be made. |
| CON-7 | Must automatically log-out user’s that are inactive for 20 minutes. |
| CON-8 | Performance data must be collected every 5-minute interval. |
| CON-9 | A history of all events within a year time period must be stored. |
| CON-10 | Relational database must be used and hosted along with system files. |

---
# Architectural Concerns
| ID        | Constraint          |
|:-------------:|-------------|
|  |  |
