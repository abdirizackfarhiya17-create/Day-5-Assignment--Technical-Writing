# DAY 5 ASSIGNMENT: SOFTWARE ENGINEERING ESSENTIALS

## MODULE: TECHNICAL WRITING FOR SOFTWARE DOCUMENTATION AND REPORTS

---

## Exercises

### A) User Manual Procedure: Setting Up a Python Virtual Environment

#### 📋 Prerequisites
* **Python Installation:** Python 3.13 installed on the local system paths.
* **Operating System:** Microsoft Windows 10 / Windows 11 platform environment.
* **Command Shell:** Standard Windows Command Prompt terminal (`cmd.exe`).

#### ⚙️ Step-by-Step Instructions

##### Step 1: Initialize the Local Terminal Window
* **Action:** Press the **Windows Key** on your hardware keyboard, input the search criteria string `cmd`, and press **Enter** to initialize a new window.
* **Expected Result:** A clean system terminal interface opens, defaulting focus path tracking inside your specific user profile directory: `C:\Users\MOHAMED>`.

##### Step 2: Generate the Isolated Virtual Environment Directory Folder
* **Action:** Input the formal environmental architecture execution script command string into the shell line path and press **Enter**:
  ```cmd
  python -m venv myenv
  ```
* **Expected Result:** The system cursor pauses on an empty line space for roughly 3 to 5 seconds while compiling dependency file systems locally. The base profile directory tracking string then reappears cleanly on the line directly below.

##### Step 3: Activation of the Virtual Environment Runtime Space
* **Action:** Execute the local path binary script initialization target directly by inputting this string and pressing **Enter**:
  ```cmd
  myenv\Scripts\activate
  ```
* **Expected Result:** The terminal baseline configuration string dynamically adapts, appending an explicit contextual tracking prefix indicator reading `(myenv)` on the far left-hand margin edge of your line.

##### Step 4: Install a Third-Party Dependency Module Package Using Pip
* **Action:** Connect to the remote package directory tracking repository system to pull down the requests module library by typing:
  ```cmd
  pip install requests
  ```
* **Expected Result:** The active console shell executes package retrieval actions for `requests` along with related functional dependencies. The logging process finishes with an explicit structural validation notification stream.
* **📸 Step Verification Screenshot:**
  
  ![Terminal Installation Output](screenshot.png)

##### Step 5: Deactivate and Terminate Isolated Runtime Memory Variables
* **Action:** Exit the runtime execution context environment safely by typing:
  ```cmd
  deactivate
  ```
* **Expected Result:** The prefix structural indicator variable label `(myenv)` immediately drops from the tracking margin line, returning full window operational parameters back to the system profile scope path line: `C:\Users\MOHAMED>`.

#### 🛠️ Troubleshooting Note
* **Common Error:** Running the activation script commands inside an active shell returns an error line string stating: *"Script execution is disabled on this system"*.
* **Root Cause & Resolution:** This error state occurs if a user opens a Microsoft PowerShell console window rather than a standard Command Prompt window, tripping built-in Windows execution security script policies. To resolve, close out the terminal window and explicitly open a standard Windows Command Prompt (`cmd`) workspace as described in Step 1.

---

### B) API Reference Entry: Task Creation Endpoint

#### 🧭 Endpoint Routing Profile
* **HTTP Protocol Method:** `POST`
* **Target Request URI Route Path:** `/api/v1/tasks`
* **Functional Description:** Builds and stores an individual task assignment item schema records within the target organizational database tracker application.

#### 🔑 Required Request Header Properties
* `Authorization`: `Bearer <token>` *(Required string. Validates access control credentials against authorization systems.)*
* `Content-Type`: `application/json` *(Required string. Sets parsing constraints to process the payload content body as JSON data structures.)*

#### 📥 JSON Request Body Schema Definitions

* **`title`** (String | Required)
  * A clear, plain-language short headline overview summary specifying the primary work assignment goal.
* **`description`** (String | Optional)
  * Extensive narrative text field detailing technical requirements, contextual documentation, or instructions.
* **`assignee_id`** (String | Required)
  * Unique system relational database identification alphanumeric string mapping the task ownership tracking records to a single user.
* **`due_date`** (String | Required)
  * Project completion milestone deadline constraints, explicitly structured as an ISO 8601 calendar date value metric format string (`YYYY-MM-DD`).
* **`priority`** (String | Required)
  * Operational classification configuration tier filtering variable. Must match exactly one of these lowercase validation options: `low`, `medium`, or `high`.

#### Valid Request Body Formatting Template Example:
```json
{
  "title": "Complete Technical Documentation Review",
  "description": "Read through the newly published API documentation entries to check formatting guidelines.",
  "assignee_id": "usr_78945x",
  "due_date": "2026-09-02",
  "priority": "high"
}
```

#### 📤 HTTP Response Lifecycle Status Codes
* **`201 Created`**: The network server parsed the payload correctly and constructed the backend record asset successfully.
* **`400 Bad Request`**: Validation checkpoint parsing fault error; occurs if required fields are missing, empty, or if strings violate formatting guidelines.
* **`401 Unauthorized`**: Client validation parsing checks failed due to a missing, expired, or structurally invalid security Bearer credential token payload string.

#### Successful Payload Processing Return Structure Example (201 Created):
```json
{
  "id": "task_abc123xyz",
  "title": "Complete Technical Documentation Review",
  "description": "Read through the newly published API documentation entries to check formatting guidelines.",
  "assignee_id": "usr_78945x",
  "due_date": "2026-09-02",
  "priority": "high",
  "status": "open",
  "created_at": "2026-08-28T16:23:00Z"
}
```
