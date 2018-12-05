# Iteration 1: Establishing an Overall System Structure
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
* CRN-3: Leverage team’s knowledge using JavaScript for web-based developmen


### Step 3: Choose One or More Elements of the System to Refine

The entire CMS system will be refined due to the fact that this is a greenfield development effort. As a result, refinement is performed through decomposition. 
![i1 step3 context diagram](https://user-images.githubusercontent.com/31861025/49493693-02429400-f82b-11e8-9b05-1022e73a34e7.PNG)
*Context diagram for Course Management System (CMS) Fig 1.1*

### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decisions and Location   | Rationale          |
|:-------------:|-------------|
| Accessing the time server in the data layer |  The reference architecture is adapted to abstract the access to the time server (UC--7, CON-2, CON-7, CON-8, CON-9). |
|  Remove local data source in the rich client application  |  The network is reliable so no need to store data locally.   |

### Step 6: Sketch Views and Record Design Decisions

![clientside](https://user-images.githubusercontent.com/32312941/49492192-4cc11200-f825-11e8-8cc0-fa768cc4083a.PNG)
![serverside](https://user-images.githubusercontent.com/32312941/49492241-7ed27400-f825-11e8-994b-debf753b1a92.PNG)
Fig 1.1


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
Initial deployment diagram for CMS Fig 1.3


| Elements  | Responsibilities            |
|:-------------:|-------------|
|  User workstation |  Hosts the client-side logic of the application     |
|  Application Server  |  Hosts server-side logic of the application and also serves web pages   |
|  Database Server |  The server that hosts the legacy relational database    |
|  Secondary system  |  Sets the external secondary servers    |


|  Relationship   |  Description            |
|:-------------:|-------------|
|  Between app server and database server |  Communication with the database will be done using ODBC     |




