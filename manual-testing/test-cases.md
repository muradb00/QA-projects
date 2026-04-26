# Manual Test Cases – DemoBlaze

## Test Environment

* URL: https://www.demoblaze.com/index.html
* Browser: Chrome
* OS: Windows

---

## TC-001: Sign up with valid credentials

**Preconditions:**
User is on the main page

**Steps:**

1. Click "Sign up"
2. Enter username: testcase2026
3. Enter password: testcase1
4. Click "Sign up"

**Expected Result:**

* Account is created successfully
* Success message is displayed
* User can log in

---

## TC-002: Signup with empty fields

**Preconditions:**
User is on the main page

**Steps:**

1. Click "Sign up"
2. Leave username empty
3. Leave password empty
4. Click "Sign up"

**Expected Result:**

* Error message is displayed
* Account is not created

---

## TC-003: Signup with username containing only spaces

**Preconditions:**
User is on the main page

**Steps:**

1. Click "Sign up"
2. Enter username: "     " (spaces)
3. Enter password: testcase1
4. Click "Sign up"

**Expected Result:**

* Signup is rejected
* Error message for invalid username
* Account is not created

---

## TC-004: Required fields visibility

**Preconditions:**
User is on the main page

**Steps:**

1. Click "Sign up"
2. Observe username and password fields

**Expected Result:**

* Required fields are clearly marked (e.g., *, label)

---

## TC-005: Add product to cart

**Preconditions:**
User is logged in

**Steps:**

1. Click "Samsung Galaxy S6"
2. Verify product details page opens
3. Click "Add to cart"

**Expected Result:**

* Confirmation message "Product added"
* Product is added to cart

---

## TC-006: Product information consistency

**Preconditions:**
User is on the main page

**Steps:**

1. Locate "Samsung Galaxy S6"
2. Note name and price
3. Click the product
4. Compare details page

**Expected Result:**

* Product name matches
* Product price matches

---

## TC-007: Duplicate username registration

**Preconditions:**
Two devices or browsers available

**Steps:**

1. Register on Device A with username: testcase_7
2. Register on Device B with same username

**Expected Result:**

* Error message: "This user already exists"
* Second account is not created

---

