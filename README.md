# Vacation Tracking System (VTS) 

*This project is based on an example from the book "Object-Oriented Analysis and Design with Applications, 3rd Edition", focusing on the business and system analysis aspects of the VTS.*

## 1. Vision 🌟
Our vision is to create a system that allows and empowers employees to effortlessly manage their vacation time without needing to master company policies. The system will automate the leave management process, ensuring efficiency, transparency, and ease of use for all stakeholders.

## 2. Functional Requirements 🛠️
### Employee Self-Management of Vacation Time
- Give individual employees the capability and responsibility to manage this particular aspect of their employment agreements with the company.

### Rules-Based Validation and Verification
- Implement a flexible rules-based system to validate and verify leave time requests.

### Historical and Future Requests
- Provide access to leave requests for the previous calendar year.
- Allow employees to submit leave requests up to a year and a half in the future.

### Manager Approval
- Approval by the immediate manager (some high-level employees may not require manager approval).

### Award Personal Leave Time
- The ability of managers to grant additional leave time (comp time) to employees directly, beyond their standard entitlements, within predefined limits set by the system.

### Email Notifications
- Send email notifications to request manager approval.
- Notify employees of changes to their request status.

### Activity Logs
- Maintain activity logs for all transactions.

### HR and System Administration Overrides
- Enable HR and system administration personnel to override restricted actions, with all overrides logged.

### HR Data Management
- HR personnel will be responsible for entering and updating employee vacation data in the system.

### Web Service Interface
- Provide a web service interface for internal systems to query an employee’s vacation request summary.

## 3. Non-Functional Requirements 📋
### Usability
- The system must be intuitive, intelligent, and easy to use for all user roles.

### Security
- Implement robust authentication and authorization mechanisms.

### Efficiency
- Aim to save time and reduce costs.

## 4. Constraints 🚧
### Technical Constraints
- Uses existing hardware and middleware.
- The system implemented as an extension to the existing intranet portal system, and uses the portal’s single-sign-on mechanisms for all authentication.

### Operational Constraints
- Keeps activity logs for all transactions.

## 5. Use Cases 

## 5.1 Use Case Diagram
![Use Case Diagram](DOCs/Use%20Case%20Diagram.png)

### Actors
- **Employee:** The main user of this system, managing their vacation time.
- **Manager:** An employee who has all the abilities and goals of a regular employee, but with the added responsibility of approving vacation requests for immediate subordinates. A manager may award subordinates comp time, subject to certain limits set in the system.
- **Clerk (HR Member):** A member of the HR department who has sufficient rights to view employees’ personal data and is responsible for ensuring that employees’ information in all HR systems is up to date and correct. An HR clerk can add or remove nearly any record in the system. In real life, HR clerks may or may not be employees; however, if they are employees, they use two separate login IDs to manage these two different roles.
- **System Admin:** Responsible for the smooth running of the system’s technical resources (e.g., Web server, database) and for collecting and archiving all log files.

## 5.2 Manage Time Use Case
### Preconditions:
The employee is authenticated by the portal framework and identified as an employee of the company with privileges to manage his or her 
own vacation time.
### Flow Chart
![Flow Chart](DOCs/Flow%20Chart%20-%20Manage%20Time.png)
### Sequence Diagram
![Sequence Diagram](DOCs/Sequence%20Diagram%20-%20Manage%20Time.png)

## 5.3 Alternate Use Cases
### 5.3.1 Withdraw Or edit Pending Request
###  Preconditions:
An employee has made a vacation time request, and that request has yet to be approved or denied by an authorized manager.
### Flow Chart & Sequence Diagram
![Flow Chart & Sequence Diagram](DOCs/Flow&Sequence%20Diagrams%20-%20Withraw&Edit%20Request.png)

### 5.3.2 Cancel Approved Request
###  Preconditions:
The employee has a vacation time request that has been approved and is scheduled for some time in the future or the recent past (previous 5 business days).
### Flow Chart & Sequence Diagram
![Flow Chart & Sequence Diagram](DOCs/Flow&Sequence%20Diagrams%20-%20Cancel%20Request.png)
## 6. Data Model (ERD)
![Data Model](DOCs/Data%20Model.png)


