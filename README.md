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
| EX-05 | Verify delete exam                     | Exam present            | 1. Click delete option 2. Confirm                              | —                        | Exam should be deleted                        | Pending | Confirm delete warning      | QA Tester 3 |


excel 
Admission	Homepage	Admission		1	In “Admit Student” , There is Missing format validation & also need to add more required Input Validation Across Multiple Sections 	next time will be fix	Address , Guardian, Health, Previous school, Board, Relational  . here all features under admit student have no any kind of validation	Sadek Sir	Lecxen Screenshort	The system accepts all kinds of inputs without restriction. No validation or error message appears.	"*More feild is required to add as input validation for compulsory feild
1. Name fields: Only alphabets allowed.
2. Contact/NID fields: Numbers only. 
3. Education/School/Board fields: Must contain alphabetic text only"	Medium			Not _Fixed	
	Manage Admission		admission>admit student	2	Nationality, Religion: When two option's inputs are not given, it shows error in the viewing of the student details 	Fixed										
		Admit Student	Admission>current information	3	Section of a class can not  be  easily modified		At the time of editing etudent details in currection information part, when i give input properly by typing in "admission information" and "Current information"  & then  clicked saved & next  button. it does not save section. The student is admitted into class without section. But when i save student clicking to "same as  admission information" , then student can be admitted  to specific section		Lecxen Screenshort	https://docs.google.com/document/d/1If6IpAm7Mmg1ehQyjY3S8fbZK-GHhMx7YVjSAf2HUBE/edit?tab=t.tc576cahtzc5	https://zaiproty-documentation.zainikthemes.com/index.html					
			Admission>Assign subject	4	Assigned subject in the admission is not used as a finaly choosen subject of a subject	Fixed	At the time of admission , when a student;s how many subject will  be read   assigned , this assigned subject don't reflect in the  class,  mark entry or result. . Again subject has to assign newly in the another module Academic setup>subject>student's  subject		Lecxen Screenshort		 Father DOB missing					
			>>Address	5	Present address & Permanent Adress structure or format is not correct .		Adress has no any sequential format such as city >district>thana>village > house. Sometimes both address may be same. but there is no option to choose same as previous		Lecxen Screenshort							
			Guardian	6	Father's DOB input given, but no output viewed				https://docs.google.com/presentation/d/1DUcBEcYtV3vVjuu7C1YVysRkZ0wY5CobRvKc0oUGF2s/edit?slide=id.g3a2fa3383dd_0_17#slide=id.g3a2fa3383dd_0_17							
			>>Previous school	7	Saved data in the previous school can not be  seen in the students details		In every feild, data given as input & saved properly. But in the  student  details, it does not show any data 		https://docs.google.com/presentation/d/1DUcBEcYtV3vVjuu7C1YVysRkZ0wY5CobRvKc0oUGF2s/edit?slide=id.g3a2fa3383dd_0_12#slide=id.g3a2fa3383dd_0_12							
			>>Relational information	8	It is no  functional		Relation can  be added using teacher & employee . but using  student can not be added. But finaly in the student information list,nothing is shown about relational information 									
				9	Students are appearing in the Employee List after being admitted, even though they are not registered as employees.	fixed	"1.Students added through Admit Student are mistakenly appearing in the Employee List.
2.These students are not employees, but the system is treating them like staff.
3.This is likely caused by wrong role assignment or missing filtering in the employee list query."	Sadek Sir		The student’s information appears in the employee list, though they have no employee designation or role.	Only users with an employee role (teacher, admin, staff, etc.) should appear in the Employee List. Students should not be included.	Higher			Fixed	
				10	Documents as a image  Cannot Be Uploaded in Student Admission	fixed	when i want to upload 9  images. it shows 9 image. but after saving   it shows the last uploaded image as 9 images	Sadik Sir				Medium			Fixed	
		Admit bulk students	admission date 	11	Range validation failed for Admission age according to session  		"1.The admission date is accepting dates outside the valid age range. 
2.Range validation is not working as per the academic session rules"									
		admit bulk students	Billing start date	12	Boundary validation failed for billing date according to session 		The billing  date is accepting dates outside the valid age boundary. Boundary validation is not working as per the academic session rules									
	Online admission 	home page		13	"Dont show in the home page
"				Lecxen Screenshort							
		Admission form		14	only class & student name  are  mandatory to form fill up. Others information is optional		No asterisk symbol  given which is compulsory to fill up form. More option should be given as compulsory to fill up the form properly 									
				15	Any option of form fill up has no any input validation											
				16	Without log in ,  after Form fill up properly , it  can not be submitted											
		Online admission>Online application	Payment status>Recieve	17	Payment amount can be negatively discounted		Payment Status (Receive), the system allows the user to enter a negative discount amount. This results in incorrect final payment calculation and invalid data entry.		Lecxen Screenshort							
				18	Without paying , it is showing paid amount by default. After paying properly,  paying amount has been  increased 		"1. 10% discount set up for admission 200tk  class one 
2.when i want to pay, it shows automaticaly created with paying where i have no paid yet ''paid amount'':180   but ''payment status'' : unpaid
3.when i want to pay in the ''payment status'', This payment can be done . This new payment is added with previous by default payment"		https://docs.google.com/presentation/d/1DUcBEcYtV3vVjuu7C1YVysRkZ0wY5CobRvKc0oUGF2s/edit?slide=id.g39a04121d0a_0_2#slide=id.g39a04121d0a_0_2							
				19	Admission with discount in the  payment status:recieve,It takes twice payment		When a student is enrolled for online admission after 2 times payment, it shows payment status : paid		Lecxen Screenshort							
				20	Without form fee set up & Payment ,student's admission status can be approved				Lecxen Screenshort							
				21	Discount column does not show discounted percentage				Lecxen Screenshort							
				22	STATUS' dropdown button can not filter 		when it is choosen status any button of 3 dropdown, it does not show any result									
				23	Gender' dropdown button can not filter 		when it is choosen status any button of 3 dropdown, it does not show any result									
				24	Admission From Date' to  'Admission To Date' can not filter											
				25	Searching by specific name in NAME column shows no matching records found		No matching records found									
				26	Searching by specific session in 'SESSION' column shows no matching records found		No matching records found									
				27	Searching by specific CLASS in 'CLASS' column shows no matching records found											
				28	Searching by specific GENDER  in 'GENDER' column shows no matching records found											
				29	Searching by specific SUBMISSION DATE  in 'SUBMISSION DATE' column shows no matching records found											
				30	Searching by specific FORM FEE in 'FORM FEE' column shows no matching records found											
				31	Searching by specific PAYMENT STATUS in 'PAYMENT STATUS' column shows no matching records found											
				32	Searching by specific DISCOUNT in 'DISCOUNT' column shows no matching records found											
				33	Searching by specific PAID AMOUNT in 'PAID AMOUNT' column shows no matching records found											
				34	Searching by specific ADMISSION STATUS in 'ADMISSION STATUS' column shows no matching records found											
		set up admission form	Download Blank admission  Form	35	Admission Blank form PDF format should be more modified		"1. PDF format is not ok.
2.Student signature option missing
3. Teacher signature option missing
4.Admission form has no unique serial number
5. No need subject selection
6. More option can be added"									
			Admission Form Top Section	36	Top section's instruction can not be set in proper place of the form		Instruction is not set in the perfect place of  the form									
			Admission Form Back Section	37	No information is found in the back section of the form in the downloaded pdf											
		Set up Form fee	Set up online admission form fee>Enable discount	38	Discount feild's title should be more modified 		From the title , it is not enough clear , if the  discount  amount will be in percentage or fixed amount		Lecxen Screenshort							
			Search :Amount	39	Search Box is  not working for “Amount” column		The search functionality is not working for the Amount column. When typing any value in the “Search: 400” input field, the list does not filter results and shows :No matching records found									
		Form fee payments	>>Discount	40	Discount column is not showing discount amount or discount percentage											
			Search: Student name	41	Search box is  not working for 'student' column											
			Search:class	42	Search box is  not working for 'class' column											
			Search: Form ID	43	Search box is  not working for 'Form Id' column											
			Search:Date	44	Search box is  not working for 'Date' column											
			Search: Recieveable amount	45	Search box is  not working for 'Recieveable amount' column	fixed		Sadek Sir				Medium			Fixed	
			Search: Recieved amount	46	Search box is  not working for 'Recieved amount' column


   again excel

   Developer	Screen-shot	Actual Result	Expected Result	Priority Status	Project Manager comment		QA Status	Requirement
Sadek Sir	Lecxen Screenshort	The system accepts all kinds of inputs without restriction. No validation or error message appears.	"*More feild is required to add as input validation for compulsory feild
1. Name fields: Only alphabets allowed.
2. Contact/NID fields: Numbers only. 
3. Education/School/Board fields: Must contain alphabetic text only"	Medium			Not _Fixed	
								
	Lecxen Screenshort	https://docs.google.com/document/d/1If6IpAm7Mmg1ehQyjY3S8fbZK-GHhMx7YVjSAf2HUBE/edit?tab=t.tc576cahtzc5	https://zaiproty-documentation.zainikthemes.com/index.html					
	Lecxen Screenshort		 Father DOB missing					
	Lecxen Screenshort							
	https://docs.google.com/presentation/d/1DUcBEcYtV3vVjuu7C1YVysRkZ0wY5CobRvKc0oUGF2s/edit?slide=id.g3a2fa3383dd_0_17#slide=id.g3a2fa3383dd_0_17							
	https://docs.google.com/presentation/d/1DUcBEcYtV3vVjuu7C1YVysRkZ0wY5CobRvKc0oUGF2s/edit?slide=id.g3a2fa3383dd_0_12#slide=id.g3a2fa3383dd_0_12							
								
Sadek Sir		The student’s information appears in the employee list, though they have no employee designation or role.	Only users with an employee role (teacher, admin, staff, etc.) should appear in the Employee List. Students should not be included.	Higher			Fixed	
