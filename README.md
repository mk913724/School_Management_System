Manual Testing on Registration Page
This repository contains manual testing documents for a registration form, showing step-by-step testing and how issues are tracked. It includes clear test cases, bug reports, and summary reports. Both positive and negative scenarios are covered, with results marked as Passed, Failed, or Warning to reflect real-life testing.

Features Tested
Validate username length
Enforce password rules (special characters, uppercase letters, and minimum length)
Ensure correct format for email and phone number
Validate Date of Birth (DOB) to prevent future dates
Verify selection of gender and country fields
Require acceptance of terms and conditions via checkbox
Conduct XSS and security testing on input fields
Prevent duplicate email registrations
Sample Test Case Document[student-attendance-blank-sheet (7).pdf](https://github.com/user-attachments/files/23822240/student-attendance-blank-sheet.7.pdf)

[student-list (6).pdf](https://github.com/user-attachments/files/23822279/student-list.6.pdf)

Recommendation
Apply robust validation for password requirements, ensuring compliance with minimum length and digit inclusion rules.
Correct backend logic to reject usernames exceeding 15 characters.
Ensure the Terms and Conditions checkbox remains editable after form submission.
Enhance the Country Dropdown functionality to preserve the selected value upon resubmission.
[Test_Case_Documents.pdf](https://github.com/user-attachments/files/23822291/Test_Case_Documents.pdf)
| TC ID | Description                   | Pre-Condition                | Steps                              | Test Data     | Expected Result                        |
| ----- | ----------------------------- | ---------------------------- | ---------------------------------- | ------------- | -------------------------------------- |
| MK-01 | Enter valid marks             | Students & subjects assigned | 1. Open marks entry 2. Enter marks | Student 1: 85 | Marks saved                            |
| MK-02 | Enter marks above full mark   | Full marks = 100             | Enter 120                          | 120           | Show error: “Cannot exceed full marks” |
| MK-03 | Enter negative marks          | —                            | Enter -5                           | -5            | Show error: “Invalid marks”            |
| MK-04 | Bulk upload marks             | Excel upload                 | Upload valid file                  | Excel file    | Marks imported                         |
| MK-05 | Bulk upload with wrong format | Wrong columns                | Upload invalid file                | Wrong Excel   | System shows format error              |




hjbjk
| TC ID | Test Case Description                  | Pre-Condition           | Test Steps                                                     | Test Data                | Expected Result                               | Status  |
| ----- | -------------------------------------- | ----------------------- | -------------------------------------------------------------- | ------------------------ | --------------------------------------------- | ------- |
| EX-01 | Verify exam creation with valid data   | User logged in as Admin | 1. Go to Exam Module → Create Exam 2. Enter valid data 3. Save | Exam: “Half Yearly 2025” | Exam should be created successfully           | Pending |
| EX-02 | Verify validation for empty exam name  | Admin logged in         | 1. Create Exam 2. Keep name empty 3. Save                      | Name: ""                 | System should show error "Exam name required" | Pending |
| EX-03 | Verify duplicate exam name not allowed | Existing exam present   | 1. Create Exam with same name 2. Save                          | Name: “Mid Term 2025”    | System should show "Exam already exists"      | Pending |
| EX-04 | Verify edit exam details               | Exam already created    | 1. Select exam 2. Edit details 3. Save                         | Change: “Session 2025”   | Exam should update successfully               | Pending |
| EX-05 | Verify delete exam                     | Exam present            | 1. Click delete option 2. Confirm                              | —                        | Exam should be deleted                        | Pending |

| TC ID | Test Case Description                  | Pre-Condition           | Test Steps                                                     | Test Data                | Expected Result                               | Status  | Comment                     | Assignee    |
| ----- | -------------------------------------- | ----------------------- | -------------------------------------------------------------- | ------------------------ | --------------------------------------------- | ------- | --------------------------- | ----------- |
| EX-01 | Verify exam creation with valid data   | User logged in as Admin | 1. Go to Exam Module → Create Exam 2. Enter valid data 3. Save | Exam: “Half Yearly 2025” | Exam should be created successfully           | Pending | Basic positive flow         | QA Tester 1 |
| EX-02 | Verify validation for empty exam name  | Admin logged in         | 1. Create Exam 2. Keep name empty 3. Save                      | Name: ""                 | System should show error "Exam name required" | Pending | Required field validation   | QA Tester 1 |
| EX-03 | Verify duplicate exam name not allowed | Existing exam present   | 1. Create Exam with same name 2. Save                          | Name: “Mid Term 2025”    | System should show "Exam already exists"      | Pending | Check unique constraint     | QA Tester 2 |
| EX-04 | Verify edit exam details               | Exam already created    | 1. Select exam 2. Edit details 3. Save                         | Change: “Session 2025”   | Exam should update successfully               | Pending | Ensure DB updates correctly | QA Tester 2 |
| EX-05 | Verify delete exam                     | Exam present            | 1. Click delete option 2. Confirm                              | —                        | Exam should be deleted 



hbkj


| Pending | Confirm delete warning      | QA Tester 3 |
