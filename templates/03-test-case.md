# Test Cases - [Feature Name]

## Test Case Information
- **Module**: [Login/Registration/Checkout/...]
- **Created by**: [Tên bạn]
- **Date**: [DD/MM/YYYY]
- **Last Updated**: [DD/MM/YYYY]

---

## TC001: Verify successful login with valid credentials

**Priority**: High  
**Type**: Functional  
**Automated**: Yes

### Preconditions
- User account exists in database
- User is on login page

### Test Steps
1. Navigate to login page
2. Enter valid username: `testuser@example.com`
3. Enter valid password: `Test@123`
4. Click "Login" button

### Expected Result
- User is redirected to dashboard
- Welcome message displays: "Welcome, Test User"
- Session is created

### Test Data
```json
{
  "username": "testuser@example.com",
  "password": "Test@123"
}
```

### Automation Script Location
`src/test/java/tests/LoginTests.java` - method `testLoginWithValidCredentials()`

---

## TC002: Verify login fails with invalid password

**Priority**: High  
**Type**: Negative Testing  
**Automated**: Yes

### Preconditions
- User account exists in database
- User is on login page

### Test Steps
1. Navigate to login page
2. Enter valid username: `testuser@example.com`
3. Enter invalid password: `wrongpassword`
4. Click "Login" button

### Expected Result
- User remains on login page
- Error message displays: "Invalid username or password"
- Login button remains enabled

### Test Data
```json
{
  "username": "testuser@example.com",
  "password": "wrongpassword"
}
```

### Automation Script Location
`src/test/java/tests/LoginTests.java` - method `testLoginWithInvalidPassword()`

---

## Test Summary

| Total Test Cases | Automated | Manual | Pass | Fail | Blocked |
|-----------------|-----------|--------|------|------|---------|
| 15 | 12 | 3 | 14 | 1 | 0 |

### Test Coverage
- ✅ Valid login scenarios
- ✅ Invalid credentials scenarios
- ✅ Empty fields validation
- ✅ Password reset flow
- ⏳ Social login (pending)