**Architecture **
Client Layer (Browser)

Users (students or admins) interact via web browser.
Accesses UI built with HTML, CSS (Bootstrap), and JavaScript.
Uses forms and AJAX calls for interactive operations without page reloads.

Presentation Layer (PHP UI and Handlers)
PHP scripts serve as controllers handling HTTP requests.
Includes files like student-registration.php, manage-students.php, enroll.php, and index.php.
These scripts process user input, perform validation, and communicate with backend.
UI layout components (header.php, footer.php, menubar.php) included for consistent design.

Business Logic Layer (PHP Scripts)
Embedded in PHP files that:
Validate sessions for access control.
Execute CRUD operations via SQL queries.
Manage enrollment constraints and user authentication.
Session variables maintain user state and roles.
AJAX endpoints provide dynamic validations like student reg no or course availability.

Data Access Layer (MySQL Database)
Structured database with tables: students, course, admin, department, level, semester, courseenrolls, etc.
Normalized schema with indices for efficient queries.
Interaction via mysqli PHP extension executing SQL queries from PHP.

**Data Flow**
User Request:
User submits a form (e.g., registration, login, enrollment) from the browser.

Request Handling:
PHP script receives input, checks session/authentication status.
If input involves DB, PHP script constructs and executes SQL queries.

Database Interaction:
Queries executed on MySQL database.
Data fetched, inserted, updated, or deleted as per operation.

Response Generation:
PHP script prepares output (redirect, alert, or page with data).
Dynamic parts can be updated via AJAX without full page reload.

Client Update:
Browser renders new or updated content.
Session variables and cookies maintain state across requests.

Continuous Interaction:
User navigates through pages or repeats actions, with persistent session state ensuring secure and personalized usage
