# Iteration 1: Establishing an Overall System Structure

![step 1](https://user-images.githubusercontent.com/31861025/49497174-b77a4980-f835-11e8-914b-75f297dad584.PNG)

---

### Step 2: Establish Iteration Goal by Selecting Drivers
The architect must be particularly mindful of the following:
* QA-1: Availability
* QA-2: Performance
* QA-3: Accessibility
* CON-1: The system must be able to support a minimum of 50 users at any time.
* CON-3: The system must be accessed through a major web browser (Chrome, Firefox, IE8+, Safari) in different Operating Systems: Windows, OSX, and Linux.
* CON-4: UI must be consistent on all browsers and Operating Systems.
* CON-5: Network connection should still be reliable even if the user has low bandwidth.
* CRN-2: Maintaining a consistent UI throughout the entire system
* CRN-3: Leverage team’s knowledge using JavaScript for web-based development

---

### Step 3: Choose One or More Elements of the System to Refine

The entire CMS system will be refined due to the fact that this is a greenfield development effort. As a result, refinement is performed through decomposition. 
![i1 step3 context diagram](https://user-images.githubusercontent.com/31861025/49493693-02429400-f82b-11e8-9b05-1022e73a34e7.PNG)
*Context diagram for Course Management System (CMS) Fig 1.1*

---

### Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers

| Design Decisions and Location | Rationale and Assumptions |
| --- | --- |
| Build the user interface and web application to structure the system for the client | The web application initiated from a web browser that communicates with a server (CRN-1). The presentation layer contains modules that are responsible for managing user interaction. The data layer contains modules that manage the data stored either locally or remotely. The four-level each responsible for the system and it will support. |
| Four-tier deployment pattern | It allows performance, usability, availability, and security by creating different tiers. This separation is done to improve security as the web server resides in a publicly accessible network. Doing this will assist in achieving our QA’s as well as CON-3. |
| Rich Client application | It runs on the user’s machine and it will provide high performance and interactive (QA-2). The modules are structured in three or more layers. |
| User Interface is built using React which is a Javascript framework and Bootstrap 4 is used from overall styling | This is one of the best current JavaScript frameworks and will allow for aspects of the website to be its own component (All UC’s can be made its own component). Also, the good thing about doing this is that it allows for a consistent design no matter what browser or OS the user accesses from CON-3, CON-4, CRN-2. This approach also for development teams to evenly distribute the workload as everyone can individually work on a portion without affecting someone else’s work CRN-3, CRN-5. Lastly, it will be styled using Bootstrap 4 as a means of keeping the entire system consistent (CON-4, CRN-2). |
| Deploy Javascript web application through notable hosting service | The application will be hosted through “Bluehost” which has a 99.99% (1st in uptime) and is proven to be reliable is handling sites with high traffic (QA-1, QA-2, CON-1, CON-2). Also due to the nature of the React framework, Once a user launches the website, all the file needed will be stored in the memory of the user’s workstation. This ensures that the website will always be running smoothly as everything will already be loaded (QA-2, CON-5). |

---

### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decisions and Location   | Rationale          |
|:-------------:|-------------|
| Accessing the time server in the data layer |  The reference architecture is adapted to abstract the access to the time server (UC--7, CON-2, CON-7, CON-8, CON-9). |
|  Remove local data source in the rich client application  |  The network is reliable so no need to store data locally.   |

---

### Step 6: Sketch Views and Record Design Decisions

![modules obtained](https://user-images.githubusercontent.com/31861025/49501276-79ceee00-f840-11e8-9f6b-f9af3348243d.png)  
*Modules obtained from the selected reference architectures Fig 1.2*  

| Elements  | Responsibilities            |
|:-------------:|-------------|
| Presentation CS |  The reference architecture is adapted to abstract the access to the time server (UC--7, CON-2, CON-7, CON-8, CON-9). |
| UI Module  |  Receive user input  |
| UI Process Module |  Use case flow    |
| Data CS  |  Modules that communicate with the server   |
| Communication Module  | Communication with the application serve     |
| Cross-Cutting CS   |  Connects with multi-layer modules   |
|  Services SS |  Modules that connects services to clients  |
| Data SS  | Modules that connects data and server communication    |
|  Database Access Module SS |  Connects to the main database  |
|  Secondary Service module SS  |  Data import and export for the secondary system  | 

![step6](https://user-images.githubusercontent.com/32312941/49492989-5e57e900-f828-11e8-9369-f7d13b0f31f1.PNG)  
*Initial deployment diagram for CMS Fig 1.3*


| Elements | Responsibilities |
|:-------------:|-------------|
|  User workstation | Hosts the client-side logic of the application |
|  Application Server | Hosts server-side logic of the application and also serves web pages |
|  Database Server | The server that hosts the legacy relational database |
|  Secondary system | Sets the external secondary servers |




| Relationship | Description |
|:-------------:|-------------|
|  Between app server and database server |  Communication with the database will be done using ODBC     |

---

### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
| Not Addressed | Partially Addressed |  Completely Addressed  |  Design Decisions Made During the Iteration  |
|:-------------:|:-------------:|:-------------:|-------------| 
|  |  UC-1  |  |  The reference architecture established modules to support this functionality  |  



