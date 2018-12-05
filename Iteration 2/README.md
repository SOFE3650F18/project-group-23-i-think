## Iteration 2: Identifying Structures to Support Primary Functionality
------

### Step 2: Establish Iteration Goal by Selecting Drivers 

The architect must address the general architectural concerns of identifying structures to support primary functionality.  
By doing this, we will also accomplish:  
* CRN-4: Evenly distribute workload between members of the development team

The architect must also consider the system’s primary use cases:  
UC-1, UC-2, UC-5, UC-6, UC-7, UC-10

---
### Step 3: Choose One or More Elements of the System to Refine

The elements located throughout the layers of the reference architecture from the previous iteration will be refined in this iteration.

### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decisions and Location   | Rationale          |
|:-------------:|-------------|
|Implementation of initial domain models |  A functional decomposition is required to create an initial domain model for the system, identifying the major entities in the domain with their relationships. It should be created in a suboptimal fashion. (Fig 2.1)   |
|  Identify Domain objects that map to functional requirements,   |  Each distinct use case functional element of the application is encapsulated in a self-contained building blocks-- domain objects (UC-1,UC-2, UC5, UC6, UC-7, UC8, UC-10, UC-11) Fig 2.2    |
|  Build layer diagram to decompose the domain objects  |  This technique ensures that modules that support all the functionalities are identified. Client side and service side of the application with sub layers. Fig 2.3 |

### Step 6: Sketch Views and Record Design Decisions

![step6 11](https://user-images.githubusercontent.com/32312941/49493714-1e463580-f82b-11e8-98f0-8e1b493e8593.PNG)

Initial domain model Fig 2.1

|  Element  | Responsibility          |
|:-------------:|-------------|
|  User interface  |  Allows user input   |
|  Web client  |  Allows user to display information about courses, event history, search or add/delete courses.   | 
|  Web server  |  Collect data and process the request from web client  |  
|  Secondary system  |  Connects to web server   |
|  Database   |  Contains logic to perform data collection and storage.  |

![step66](https://user-images.githubusercontent.com/32312941/49493741-3b7b0400-f82b-11e8-990f-22e740bec1aa.PNG)
Domain object associate with the use case model Fig 2.2

![step6 3](https://user-images.githubusercontent.com/32312941/49493941-00c59b80-f82c-11e8-9672-f5fb4a1453d0.PNG)
Modules that supports the primary use cases Fig 2.3

|  Element  | Responsibility          |
|:-------------:|-------------|
|  RequestManager  |  Responsible for communication with the server-side logic   |
|  RequestService  |  Provides a facade that receives requests from the client.   | 
|  Data Collection Controller  |  Contains logic to perform data collection and storage.  |  
|  Process request business layer  |  Responsible for processing request.    |
|  Get request   |  Responsible for getting request from the client.  |
|  Process request data layer  |  Responsible for processing request. |
|  EventData Mapper  |  Responsible for persistence operations related to t
he event.   |
|  Secondary System  |  Responsible for persistence operation related to the secondary university system.  |

![sqdia](https://user-images.githubusercontent.com/32312941/49494166-ab3dbe80-f82c-11e8-8df1-b5be9deb5a09.PNG)
Sequence diagram for use case UC-1 Fig 2.4 






