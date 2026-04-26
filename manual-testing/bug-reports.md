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

---

##  Bug 5: Product storage capacity mismatch between title and description

**ID:** BUG-005
**Severity:** High
**Priority:** High

### Description

The product title indicates a different storage capacity than the product description, leading to inconsistent and misleading information.

### Steps to Reproduce

1. Open the website
2. Navigate to product: **"iPhone 6 32GB"**
3. Open the product detail page
4. Compare product title and description

### Expected Result

Product description should match the product title, indicating **32GB storage**.

### Actual Result

* Product title shows: **32GB**
* Product description states: **16GB internal storage**

### Impact

* Misleads users about product specifications
* Can lead to incorrect purchase decisions
* Reduces trust in product data accuracy
* Potential business and credibility impact

---

##  Bug 6: Invalid credit card number format is accepted during purchase

**ID:** BUG-006
**Severity:** High
**Priority:** High

### Description

The system accepts an invalid credit card number format during purchase, allowing the transaction to proceed with incorrect payment data.

### Steps to Reproduce

1. Add any item to the cart (optional: can also proceed without items)
2. Navigate to "Cart"
3. Click "Place Order"
4. Enter valid data in required fields (e.g. Name, Country)
5. Enter credit card number: `1111`
6. Click "Purchase"

### Expected Result

* System should validate credit card format
* Invalid card numbers (e.g. too short or incorrect format) should be rejected
* Error message should be displayed

### Actual Result

* System accepts invalid credit card number (`1111`)
* Purchase is completed successfully

### Impact

* Allows invalid payment data
* Indicates weak input validation
* Potential financial and data integrity risks
* No length or format validation (e.g. Luhn check) is applied

