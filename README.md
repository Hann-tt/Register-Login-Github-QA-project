# Register-Login-Github-QA-project
This project contains manual test cases for core user authentication flows, including **Register**, **Login**, and **Forgot Password**. It was created to demonstrate practical QA skills in designing, executing, and documenting test scenarios for common authentication modules.
## 📌 Project Overview

- Type: Manual Testing
- Scope: Register, Login, Forgot Password
- Tester: Ngọc Hân
- Tools Used: Excel, GitHub

## 📋 Test Case Summary

- Total test cases: 45 
- Bugs identified: 1  
- Severity level: High 
- Affected module: Registration

| ID        | Priority | Test Title                         | Test Data Example                        | Expected Result                                                                 | Status  |
|-----------|----------|-------------------------------------|------------------------------------------|----------------------------------------------------------------------------------|---------|
| TC_P_012  | High     | Invalid Password – Blank Field      | Password: *(empty)*                      | System displays “Password cannot be blank.” Registration is blocked.            | ✅ Pass |
| TC_E_002  | High     | Invalid Email Format                | Email: `vann170723@gmali.com`            | System should reject malformed email. However, it was incorrectly accepted.     | ❌ Fail |
| TC_USN_004| High     | Invalid Username – Blank Field      | Username: *(empty)*                      | System displays “Username cannot be blank.” Registration is blocked.            | ✅ Pass |
| TC_R_030  | High     | Valid Registration Information      | Email: `vann170723@gmail.com`<br>Username: `Hann-tt`<br>Password: `an198802@!` | Account is successfully created and user is redirected to login.                | ✅ Pass |
| TC_V_029  | High     | CAPTCHA Verification                | CAPTCHA: *(correct / incorrect / blank)* | System allows registration only with correct CAPTCHA. Shows error if incorrect. | ⏳ Pending |


## 🐞 Bug Reports
Bug reports are documented in the `bugs/` folder with:

| DEFECT ID   | DESCRIPTION                                 | VERSION     | STEPS                                                        | CREATE DATE | FILE             | CREATE BY | STATUS  | FIXED BY | CLOSE DATE | SEVERITY | PRIORITY |
|-------------|---------------------------------------------|-------------|--------------------------------------------------------------|-------------|------------------|------------|---------|----------|-------------|----------|----------|
| BUG_001     | System accepts invalid email domain format  | v1.0.3      | 1. Open registration page<br>2. Enter email: `vann170723@gmali.com`<br>3. Fill other fields<br>4. Submit form | 2025-08-26  |<img width="AUTO" height="auto" alt="BUG" src="https://github.com/user-attachments/assets/741bab16-2f1d-4d01-958c-b02e16e237a5" />
 | NGOC HAN| OPEN | - | - | MAJOR | HIGH | 
