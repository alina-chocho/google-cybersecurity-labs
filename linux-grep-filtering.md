# Lab: Filtering Text and Logs Using Grep

## 📌 Project Overview
In this lab, I acted as a security analyst to investigate user records and system logs. Using the Linux command-line utility `grep`, I filtered large datasets to locate specific usernames and audit department access lists for security verification.

## 🛠️ Skills & Commands Demonstrated
* **Pattern Matching:** Isolated targeted text strings within flat files using exact matches.
* **String Interpretation:** Handled multi-word query arguments containing spaces by encapsulating strings in quotes.
* **Data Auditing:** Counted specific log outcomes to verify user counts within distinct organizational departments.

## 💻 Commands Applied & Use Cases

| Command | Security Application / Use Case |
| :--- | :--- |
| `grep "jhill" Q2_deleted_users.txt` | Searched the Quarter 2 deleted users log to verify if user account `jhill` was successfully removed. |
| `grep "Human Resources" Q4_added_users.txt` | Searched the Quarter 4 onboarding logs to identify all new user provisions under the HR department. |

---

## 🔍 Step-by-Step Investigation & Results

### Step 1: Locating Deleted User Accounts
To confirm whether the user **jhill** was present in the system's deletion logs, I executed a case-sensitive search against the Quarter 2 records. 

* **Command Executed:**
  ```bash
  grep "jhill" Q2_deleted_users.txt
  ```
* **Result:** The system returned the explicit match log `1025 jhill`, successfully confirming the user's presence in the deleted database.

### Step 2: Auditing Departmental Onboarding Records
To track personnel additions within the **Human Resources** team during the final quarter, I queried the onboarding log file. Because the search term contained multiple words, quotation marks were applied to ensure accurate string interpretation.

* **Command Executed:**
  ```bash
  grep "Human Resources" Q4_added_users.txt
  ```
* **Result:** The terminal generated two distinct entries representing newly added personnel (`sshah` and `msosa`), verifying that **two users** were added to the HR department during this period.
