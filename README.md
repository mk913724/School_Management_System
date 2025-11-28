##Manual Testing on Registration Page
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
