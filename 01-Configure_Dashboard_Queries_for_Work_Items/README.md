# Task 1 : Configure Dashboard and Queries for Work Items

## Objective:
### To create custom queries in Azure DevOps to filter work items assigned to the user and visualize them on a shared team dashboard using widgets like Query Tile.

## Steps:
### 1: Create a Custom Query
- Navigated to Boards → Queries

- Clicked New Query

- Configured the following filters in the Editor tab:

  - `Work Item Type` = `Task`

  - `Assigned To` = `@Me`

  - `State` = `To Do` 

- Saved the query as "My Active Tasks" under Shared Queries

### 📸 Query Editor setup
<img width="1919" height="678" alt="Image" src="https://github.com/user-attachments/assets/2d6e3a91-c68b-4386-8b9e-209b8d987ad4" />



### 2: Create and Assign a Task
- Went to Boards → Work Items

- Created a new task:

  - Title: `My Sample Task`

  - Assigned To: Self (Alina Khan)

  - State: `To Do` (default Agile state)

-  Saved the task

### 📸 Task detail view showing title, assigned to, and state
<img width="1593" height="467" alt="Image" src="https://github.com/user-attachments/assets/d9f5cb47-631d-4c8d-9b61-6dbcc037c59e" />


### 3: Run Query and Verify Result
- Ran the saved query: "My Active Tasks"

- The created task appeared in the result

### 📸 Query result showing the matching work item
<img width="1294" height="312" alt="Image" src="https://github.com/user-attachments/assets/b09093e3-4615-4581-9c64-9329b87417cd" />

### Step 4: Create and Configure Dashboard
- Navigated to Dashboards → New Dashboard

  - Name: `Work Item Overview`

  - Team: Week8_Assignment Team

- Added Query Tile widget to the dashboard

### 📸 Dashboard showing widget added
<img width="1598" height="424" alt="Image" src="https://github.com/user-attachments/assets/4a419090-0cb9-488a-b951-938336989c87" />


### Step 5: Configure Query Tile Widget
- Opened widget settings

  - Selected the query: My Active Tasks

  - Display: Count

  - Saved the widget configuration


## Summary:
- Successfully created a filtered query to track user tasks

- Visualized the result dynamically on a shared team dashboard

- Demonstrated end-to-end use of Azure Boards and Dashboards


