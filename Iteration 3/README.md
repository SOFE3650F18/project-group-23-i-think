# Iteration 3: Addressing Quality Attribute Scenario Driver

### Step 2: Establish Iteration Goal by Selecting Drivers

This iteration focuses on QA-3 quality attribute scenario: The system should be able to let users upload files, send messages to individuals, teams or all course participants at once.

---

### Step 3: Choose One or More Elements of the System to Refine

The elements that will be refined are the 3 physical nodes from iteration 1:
* User Workstation (Client-Side Application)
* Application Server (Server-Side Application)
* Database Server

---

### Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers

| Design Decisions and Location | Rationale and Assumptions |
| --- | --- |
| Build components to for communication between users   |  This component will allow users to send messages, which is then temporarily stored in the database and then to be displayed in the display component of the receiving users.  |
|  Establish component for uploading files  |  It will have an upload field so that users can browse their device for a file and then upload it. This sends the file to be stored in the database and updates the user's history with the submission information along with a link to download it from the database   |

---

### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces
| Design Decisions and Location | Rationale |
| --- | --- |
| Utility component for users allowing for quick access to common features | Makes it very easy for the user to accomplish any task since everything they need is grouped together in a quick access section for their convenience. Doing this also creates a cleanly organized structure.  |
| All items (messages or file) sent to the database with details | Due to the nature of our database being a relational database, every sent item will be stored with information about the sender, target, timestamp, file size, etc... |

---

### Step 6: Sketch Views and Record Design Decisions
![i3 step6 sequence diagram green](https://user-images.githubusercontent.com/31861025/49495154-14730100-f830-11e8-85b9-1c25dd76c27e.PNG)  
*Sequence diagram for quality attribute QA-3 Fig 3.1*

| Element | Responsibility |
| --- | --- |
| User | The person using the system |
| Workstation | The user’s device |
| CMS Home Page | The UI that the user interacts with. After login, they are presented with the components that allows them to upload file and send messages |
| Database | A relational database that stores all data |
| User Event History | A file that store a history of all events made by the user |
| Messenger | The messaging component |

---

### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
|:---:|:---:|:---:| --- |
|  |  | QA-3 | Established and explained the sequence that occurs when either files are upload or a message is sent.  |
|  | CON-2 |  | No relevant decisions made. |
|  |  | CON-7 | Through use of the Activity function in iteration 2, the functionality of the inactivity logout feature has been established. |
|  |  | CON-9 | Established how event history will be updated. |
|  | CRN-3 |  | Technologies consider thus far takes into account the developer’s knowledge. Since there could still be more added throughout the system’s life cycle, it has been marked as “partially addressed”. |
