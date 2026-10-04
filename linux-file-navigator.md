# Lab: Exploring Linux Navigation and File Management

## 📌 Project Overview
In this lab, I acted as a security analyst navigating a Linux filesystem using the Bash shell. The goal was to audit user directory structures, investigate system access lists, and inspect server logs to identify potential operational anomalies and verify authorization controls.

## 🛠️ Skills & Commands Demonstrated
* **System Mapping:** Navigated nested directory architectures using `pwd`, `ls`, and `cd`.
* **Data Inspection:** Read targeted configuration files and isolated system user groups using `cat`.
* **Log Analysis:** Efficiently audited the initial states of log repositories using the `head` filter to avoid system resource overload.

| Command | Security Application / Use Case |
| :--- | :--- |
| `pwd` | Verifies the current active directory path during an investigation. |
| `ls` | Lists files, scripts, and logs available within an active folder. |
| `cd` | Transitions between administrative, user, and log directories. |
| `cat` | Outputs full contents of text assets, such as employee registry updates. |
| `head` | Restricts data output to the top 10 lines of large files like `server_logs.txt`. |

## 🔍 Step-by-Step Investigation & Results

### Step 1: Directory Navigation & Discovery
* Transitioned from the base user space to the targeted reporting subdirectory:
  ```bash
  cd /home/analyst/reports
  ls
  ```
* **Finding:** Discovered the `users` subdirectory, which houses organizational asset data.

### Step 2: Access & Department Auditing
* Navigated into the audited directory and inspected employee records:
  ```bash
  cd /home/analyst/reports/users
  cat Q1_added_users.txt
  ```
* **Finding:** Identified personnel records mapping specific system identifiers to active departments. For example, verified that user `aezra` belongs to the **Human Resources** department, ensuring baseline directory synchronization.

### Step 3: Log Analysis
* Moved to the system logs repository to perform an initial review of the application state:
  ```bash
  cd /home/analyst/logs
  head server_logs.txt
  ```
* **Finding:** Successfully filtered the initial lines of the log file. Discovered exactly **three** `WARNING` flags raised in the top 10 lines of the server runtime output, pinpointing initial areas for deeper security troubleshooting.

## 💡 Key Takeaways
* **Syntax Precision:** Linux systems are highly case-sensitive and literal; explicit formatting is required to prevent terminal truncation or file-not-found errors.
* **Process Management:** Developed hands-on familiarity with process interruption signals (`Ctrl + C`) to effectively clear hanging terminal tasks during an active investigation window.
