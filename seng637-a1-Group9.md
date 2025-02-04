>   **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 9      |
|-----------------|
| Student 1 name: David Nguyen                |   
| Student 2 name: Kate Reimann              |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

# Introduction

Assignment 1 serves as an introduction to exploratory and manual functional testing by allowing us to interact with a system under test (SUT) in the form of an ATM simulation application. This assignment provides hands-on experience in developing an Exploratory Test Plan, executing Manual Scripted Testing (also known as Manual Functional Testing, MFT), and conducting Regression Testing on an updated version of the application. Through this process, we gain a deeper understanding of testing methodologies and their role in ensuring software reliability.

Before this lab, our knowledge of these testing techniques was primarily theoretical, based on lecture slides. We had a basic understanding of the following testing approaches:

- **Exploratory Testing**: A dynamic testing approach where we developed a high level test plan from the requirements. The test plan is flexible and is useful for discovering unexpected issues and improving test coverage in an intuitive manner.
- **Manual Scripted Testing (Manual Functional Testing, MFT)**: A structured testing approach where testers follow predefined test cases to systematically verify that the application meets specified requirements. This method ensures repeatability and consistency in test execution.
- **Regression Testing**: Testing performed after changes, such as updates or bug fixes, to ensure that previously working functionality remains intact and no new defects are introduced.

# High-level description of the exploratory testing plan

## A. Test Types:
For Exploratory Testing, we will be focusing on System Testing: conducted on a complete, integrated system to evaluate the system's compliance with its specified requirements.


## B. System Under Test Overview:

- B.1. System under test: ATM System - Lab 1 Version 1.0
- B.2. Environment: Windows 10 or Mac with Java installed to run the JAR file.
- B.3. Startup: start ATM with a specific number of $20 bills (for example: 10 - $20 bills for Session 1 and 3 - $20 bills for Session 2).
- B.4. Card #1 (PIN:42), Checking, Savings.
- B.5. Card #2 (PIN: 1234), Checking, Money Market
- B.6. Initial Balances: Checking -> $100, Savings -> $1000, Money Market -> $5000.

## C. Approach and Strategy:

- C.1. Perform exploratory testings of ~30 minutes each.
- C.1.1. First focus on successful and typical paths (valid PIN, normal deposits, etc.)
- C.1.2. Second focus on scenarios that are higher risk that may crush the program (incorrect PIN, incorrect inputs, etc.)
- C.2. Document briefly session notes on the tested scenarios.
- C.3. Log any bugs in Jira.

## D. Scope of Test and Testing Logistics:
We will be focusing on the Use Cases below:
- Deposit: tests valid deposits could be completed and invalid deposits should be rejected with appropriate error message
- Withdraw: tests valid withdrawals could be completed and invalid withdrawals should be rejected with appropriate error message
- Transfer: tests valid transfers could be completed and invalid transfers should be rejected with appropriate error message
- Inquiry: tests valid inquiries could be completed and invalid inquiries should be rejected with appropriate error message
- Log: tests the accuracy of the log
- PIN/Card: tests the PIN accuracy and card insert 
- Receipt: tests the accuracy of the receipts for each transaction
- Cancel: tests the cancellation function for each transaction

## E. Testing Logistics:
We will be splitting the tests in half, with David finishing tests related to Deposit, Withdraw, PIN/Card and Kate finishing tests related to Transfer, Inquiry, Receipt, and Cancel. 

A copy of the full Test Plan with test cases and results can be found in attached Excel file: SENG637 Assignment 1 Group 9 - Defect List and Test Plans in Exploratory Testing tab.

# Comparison of exploratory and manual functional testing

Exploratory testing allowed us to freely explore the system and find issues early on. This helped uncover more errors and patterns that might have been harder to catch with manual scripted testing. However, manual scripted testing was useful for covering some functions that were missed during exploratory testing, either due to distractions or skipped steps. For example, exploratory testing only documented informationto see what happened after 3 incorrect PIN entries. While the manual test captured what occurs after the first and second invalid PIN entry. On the other hand, the exploratory testing helped dig deeper into issues, like discovering that the withdrawal selection was off by one—choosing option 1 for $20 would actually select option 2 for $40. Since this required multiple deposits to notice, it might not have been caught in manual testing.

We have provided an Excel sheet called Defect List, which includes all bugs and issues found in both testing approaches for ATM versions 1.0 and 1.1. The file also contains the Exploratory Testing sheet, documenting the step-by-step findings, and the Manual Scripted Testing sheet, which includes the results from Appendix C.

# Notes and discussion of the peer reviews of defect reports

## Method for Peer-Review
After conducting the Exploratory Testing and the Manual Scripted Testing, each member of the group populated the Defect List, which was peer reviewed by the other member of the group. Defects that have already been listed was not listed again, but instead received edits and revision to have a consistent format.

## Discussion
The first version of the Defect List had many repeated defects due to the Exploratory Test Plan being very detailed. However, after refining and removing duplicates (such as testing checking withdrawal for card 1 and card 2), we are left with 11 defects. The entire list is retested in Regression Testing for v1.1 and updated with the new status. 4 of which were resolved.

We noticed some tests would Pass / Fail depending on the assumption that was not listed in the requirement. For example, the SUT takes a fee for each deposit. We assumed this should not happen and marked those tests as Fail. 

# How the pair testing was managed and team work/effort was divided 

Both team members split evenly the Exploratory Test, MFT and Regression Testing and provided notes for each other.

# Difficulties encountered, challenges overcome, and lessons learned

Exploratory testing was challenging at first because we worried about getting the steps wrong. We also recorded a lot of bugs that seemed similar, but without certainty, we included them all. Over time, we realized that certain recurring issues, like the incorrect card number appearing on receipts, didn’t necessarily mean other functionalities were failing. Another challenge was learning two platforms—Jira and Azure—which felt time-consuming, and their export options were not very user-friendly. In the end, we switched to Excel because it was the most efficient option.

# Comments/feedback on the lab and lab document itself

The instructions felt scattered and unclear, making it hard to understand what was required. For example, the link to the Test Sample report didn’t work, so we weren’t sure what format to follow. We completed this report in markdown format, hoping it aligned with the expectations.
