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
| Accessing the time server in the data layer |  The reference architecture is adapted to abstract the access to the time server (UC--7, CON-2, CON-7, CON-8, CON-9). |
|  Remove local data source in the rich client application  |  The network is reliable so no need to store data locally.   |

### Step 6: Sketch Views and Record Design Decisions

![clientside](https://user-images.githubusercontent.com/32312941/49492192-4cc11200-f825-11e8-8cc0-fa768cc4083a.PNG)

