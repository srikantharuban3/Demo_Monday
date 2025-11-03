# Instruction 

- You are a test automation engineer.  
- Execute all test cases listed in the **"Test Suite"** section.  
- Use **Playwright MCP tools** to perform each test step.  
- If any step or verification fails, mark the **entire test case as failed**.  
- After completing one test case, proceed to the next until all are executed.  
- When all test cases are completed, generate a **Test Execution Report** in `.html` format.  
- The report must include all relevant details such as:  
  - Test case ID and description  
  - Steps executed  
  - Pass/Fail status  
  - Error messages or screenshots (if applicable)  
  - Execution timestamp 
  - Add Bar chart


# Test suite

## TC 001 - Verify that user can register a new customer (FR-1)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Click on the Register link.
- Fill the registration page. 
- Use unique username and password. 
- user name should be 10 charactors and should be unique.
- submit the form by clicking on the register page. 
- Verify that welcome message with the new username is displayed.

## TC 002 - Verify user login functionality (FR-3)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Enter valid username and password in the login section
- Click "Log In" button
- Verify that user is successfully logged in and dashboard is displayed
- Verify that Account Services menu is visible

## TC 003 - Verify "Forgot login info" functionality (FR-4)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Click on "Forgot login info?" link
- Enter valid information to recover login details
- Verify that appropriate recovery message or form is displayed
- Verify navigation back to login page

## TC 004 - Verify user logout functionality (FR-6)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Log Out" link from Account Services menu
- Verify that user is successfully logged out
- Verify that login page is displayed

## TC 005 - Verify Account Overview/Dashboard (FR-7, FR-8)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Accounts Overview" from Account Services menu
- Verify that all user accounts are displayed with account numbers
- Verify that account types and current balances are shown
- Click on an account number to view detailed account information

## TC 006 - Verify Account History functionality (FR-9)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Navigate to Account Overview
- Click on an account number to view account details
- Verify transaction history is displayed with date, description, amount
- Verify that balance after each transaction is shown

## TC 007 - Verify Transfer Funds functionality (FR-10, FR-11, FR-12, FR-13)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Transfer Funds" from Account Services menu
- Select source account from dropdown
- Enter transfer amount
- Select destination account
- Click "Transfer" button
- Verify confirmation screen is displayed
- Verify transfer is completed successfully
- Verify confirmation message is shown

## TC 008 - Verify Bill Pay functionality (FR-14, FR-15, FR-16)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Bill Pay" from Account Services menu
- Fill payee information (name, address, city, state, zip, phone, account)
- Enter amount to pay
- Select account to pay from
- Click "Send Payment" button
- Verify payment confirmation is displayed
- Verify payment details are correct

## TC 009 - Verify Open New Account functionality

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Open New Account" from Account Services menu
- Select account type (Checking/Savings)
- Select existing account to transfer funds from
- Enter minimum deposit amount
- Click "Open New Account" button
- Verify new account is created successfully
- Verify account number is generated and displayed

## TC 010 - Verify Find Transactions functionality

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Find Transactions" from Account Services menu
- Select an account from dropdown
- Search by transaction ID or date range or amount
- Click "Find Transactions" button
- Verify search results are displayed correctly
- Verify transaction details match search criteria

## TC 011 - Verify Update Contact Info functionality

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Update Contact Info" from Account Services menu
- Update profile information (first name, last name, address, city, state, zip, phone)
- Click "Update Profile" button
- Verify profile is updated successfully
- Verify confirmation message is displayed

## TC 012 - Verify Request Loan functionality

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Login with valid credentials
- Click on "Request Loan" from Account Services menu
- Enter loan amount
- Enter down payment amount
- Select account for down payment from dropdown
- Click "Apply Now" button
- Verify loan application is processed
- Verify loan approval/denial status is displayed

## TC 013 - Verify About Us page navigation (FR-22)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Click on "About Us" link in navigation
- Verify About Us page loads successfully
- Verify page contains bank information, mission, vision
- Verify page layout and content are properly displayed

## TC 014 - Verify Services page navigation (FR-23)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Click on "Services" link in navigation
- Verify Services page loads successfully
- Verify page lists key banking services offered
- Verify ATM Services and Online Services sections are displayed

## TC 015 - Verify Contact Us page navigation (FR-26)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Click on "Contact Us" link in navigation
- Verify Contact Us page loads successfully
- Verify contact form is available with required fields
- Fill contact form with valid information
- Submit the form and verify confirmation

## TC 016 - Verify responsive design across devices (NFR-3)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Test page display on desktop resolution (1920x1080)
- Resize browser to tablet resolution (768x1024)
- Verify page elements are properly responsive
- Resize to mobile resolution (375x667)
- Verify mobile layout is functional and readable

## TC 017 - Verify page load performance (NFR-2)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Measure page load time for homepage
- Verify page loads within 3 seconds
- Login and measure dashboard load time
- Verify dashboard loads within 2 seconds
- Navigate to different pages and verify load times

## TC 018 - Verify security features and HTTPS (FR-35, NFR-7)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Verify that all pages use HTTPS protocol
- Check for secure connection indicators in browser
- Verify that sensitive data is not exposed in URLs
- Test that session management is secure
- Verify password fields are properly masked

## TC 019 - Verify navigation menu consistency (NFR-4)

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Verify all navigation links are accessible (Home, About Us, Services, Products, Locations, Contact Us)
- Click each navigation link and verify it loads correctly
- Verify consistent navigation structure across all pages
- Verify breadcrumb navigation where applicable

## TC 020 - Verify error handling and validation

- Navigate to `https://parabank.parasoft.com/parabank/index.htm`
- Attempt login with invalid credentials
- Verify appropriate error message is displayed
- Try registration with missing required fields
- Verify field validation messages appear
- Test transfer with insufficient funds
- Verify proper error handling and user feedback