TDD (Test Driven Development) Documentation  

 

Objective 

The objective of the TDD Documentation is to guide the coders and testers through the TDD Lab. By thoroughly testing functionalities of the Online Bookstore using Pytest. To ensure reliability and effectiveness for the user. 

1. Introduction 

This TDD documentation outlines the testing strategy and test cases for the Online Bookstore system.  

Test Case 1: User Registration 

Input: User provides name, email, age, and book genre interest. 

Expected Output: User account is created. 

Test Case 2: User Authentication 

Input: User provides valid credentials during login. 

Expected Output: User is authenticated. 

Test Case 3: Email Validation 

Input: User provides an email. 

Expected Output: The system validates the email format. 

Test Case 4: Book Browsing and Searching 

Test Case 4: Browse Books by Category 

Input: User selects a book category. 

Expected Output: Books in the selected category are displayed. 

Test Case 5: Search for a Book 

Input: User enters a book title in the search bar. 

Expected Output: Relevant books are displayed. 

Book Details and Reviews 

Test Case 6: View Book Details 

Input: User clicks on a book. 

Expected Output: Detailed information about the book is displayed. 

Test Case 7: Submit Review and Rating 

Input: User submits a review and rating for a book. 

Expected Output: Review and rating are saved. 

Shopping Cart 

Test Case 8: Add Books to Cart 

Input: User adds books to the shopping cart. 

Expected Output: Books are added to the cart. 

Test Case 9: Modify Cart Contents 

Input: User updates the quantity of books in the cart. 

Expected Output: Cart contents are modified accordingly. 

Order Processing 

Test Case 10: Proceed to Checkout 

Input: User clicks on the checkout button. 

Expected Output: User is directed to the checkout page. 

Test Case 11: Generate Order Confirmation 

Input: User completes the purchase. 

Expected Output: System generates an order confirmation with a unique ID. 

User Account Management 

Test Case 12: Update User Profile 

Input: User updates personal information and password. 

Expected Output: User profile is updated. 

Admin Panel for Content Management 

Test Case 13: Add Book to Catalog 

Input: Admin adds a new book to the catalog. 

Expected Output: Book is added successfully. 

Test Case 14: Edit Book in Catalog 

Input: Admin edits book details in the catalog. 

Expected Output: Book details are updated. 

Test Case 15: Remove Book from Catalog 

Input: Admin removes a book from the catalog. 

Expected Output: Book is removed successfully. 

Test Case 16: Manage User Accounts 

Input: Admin views and manages user accounts. 

Expected Output: User accounts are managed successfully. 

Test Case 17: View Order Details 

Input: Admin views details of user orders. 

Expected Output: Order details are displayed. 

Non-functional Requirements: 

Performance 

Test Case 18: Concurrent User Sessions 

Input: Multiple users access the system simultaneously. 

Expected Output: System handles concurrent sessions without performance degradation. 

Reliability 

Test Case 19: System Availability 

Input: System is operational over time. 

Expected Output: System is available 99% of the time. 

Security 

Test Case 20: Password Security 

Input: User creates or updates a password. 

Expected Output: Passwords are securely stored using encryption. 

Test Case 21: Transaction Security 

Input: User performs a transaction. 

Expected Output: Transactions are secured using HTTPS. 

Scalability 

Test Case 22: System Scalability 

Input: System experiences growth in books, users, and transactions. 

Expected Output: System accommodates the growing load effectively. 

Browser Compatibility 

Test Case 23: Browser Compatibility 

Input: System accessed using modern web browsers (Chrome, Firefox, Safari). 

Expected Output: System functions seamlessly across supported browsers. 

Test Case 24: Technology Stack Compatibility 

Input: Development using HTML5, CSS3, JavaScript, and Node.JS. 

Expected Output: System is compatible with the specified technology stack. 

User Interfaces 

Test Case 25: UI (User Interface) Intuitiveness 

Input: Users interact with the system interface. 

Expected Output: UI is intuitive and user-friendly. 
