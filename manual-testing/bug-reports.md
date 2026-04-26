# Bug Reports – Demoblaze

---

##  Bug 1: Username field accepts only whitespace

**ID:** BUG-001
**Severity:** Medium
**Priority:** High

### Description

The system allows users to sign up using a username that contains only whitespace characters.

### Steps to Reproduce

1. Open the website
2. Click "Sign up"
3. Enter username: `"     "` (5 spaces)
4. Enter any valid password
5. Click "Sign up"

### Expected Result

System should reject the input and display a validation error (e.g. "Username cannot be empty").

### Actual Result

Signup is processed and account is created.

### Impact

* Allows invalid data into the system
* May cause issues in authentication and user management

---

##  Bug 2: Missing required field indicators

**ID:** BUG-002
**Severity:** Low
**Priority:** Medium

### Description

The signup form does not visually indicate which fields are required.

### Steps to Reproduce

1. Open the website
2. Click "Sign up"
3. Observe input fields

### Expected Result

Required fields should be clearly marked (e.g. * or label).

### Actual Result

No visual indicators are present.

### Impact

* Poor user experience
* Users may submit incomplete forms

---

##  Bug 3: Username case sensitivity inconsistency

**ID:** BUG-003
**Severity:** Medium
**Priority:** Medium

### Description

The system allows creation of accounts with usernames that differ only by letter casing.

### Steps to Reproduce

1. Sign up with username: `testuser`
2. Sign up again with username: `TestUser`

### Expected Result

System should treat usernames as case-insensitive and prevent duplicates.

### Actual Result

Both accounts are created successfully.

### Impact

* Potential confusion
* Risk of duplicate accounts

---

## Bug 4: Signup form retains entered credentials after successful submission

**ID:** BUG-004
**Severity:** Medium
**Priority:** Medium

### Description

After a successful signup attempt, the signup form retains previously entered username and password when reopened or reused.

### Steps to Reproduce

1. Open the website
2. Click "Sign up"
3. Enter username: `testadmin1`
4. Enter password: `123456`
5. Click "Sign up" and complete registration
6. Click "Sign up" again (reopen modal)

### Expected Result

* Signup form should reset after successful registration
* Username and password fields should be empty

### Actual Result

* Previously entered username and password remain in the input fields

### Impact

* Poor user experience (form not reset)
* Potential privacy concern if multiple users use the same device

