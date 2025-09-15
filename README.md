# TESTAUT-EX-01
For this project I designed a automation ;demonstrates comprehensive test automation for e-commerce website login functionality using Selenium WebDriver with Java and TestNG framework.

## Features
- **Page Object Model (POM)** design pattern
- **Cross-browser testing** (Chrome, Firefox, Edge, Safari)
- **Comprehensive test scenarios** including edge cases
- **Automatic screenshot capture** on test failure/success
- **Data-driven testing** with TestNG DataProvider
- **Security testing** (SQL injection, XSS prevention)
- **Detailed logging** and reporting
- **WebDriverManager** for automatic driver management

## Test Scenarios
1. **Login Page Elements Verification**
   - Verify all login page elements are displayed
   - Check page title and URL

2. **Valid Login Tests**
   - Standard user login
   - Problem user login
   - Performance glitch user login

3. **Invalid Login Tests**
   - Invalid email and password
   - Valid email, invalid password
   - Invalid email format
   - Empty credentials
   - Locked out user
   - Very long credentials

4. **Security Tests**
   - SQL injection attempts
   - Special characters handling
   - XSS prevention

5. **Edge Case Tests**
   - Empty form submission
   - Boundary value testing
   - Special character validation

## Prerequisites
- Java 11 or higher
- Maven 3.6 or higher
- Chrome/Firefox/Edge browser installed

## Dependencies
- **Selenium WebDriver** 4.15.0
- **TestNG** 7.8.0
- **WebDriverManager** 5.6.2
- **ExtentReports** 5.1.1
- **Apache Commons IO** 2.11.0

## How to Run Tests

### 1. Clone and Setup
```bash
git clone <repository-url>
cd selenium-ecommerce-tests
```

### 2. Install Dependencies
```bash
mvn clean install
```

### 3. Run All Tests
```bash
mvn test
```

### 4. Run Specific Browser
```bash
mvn test -Dbrowser=chrome
mvn test -Dbrowser=firefox
mvn test -Dbrowser=edge
```

### 5. Run Specific Test
```bash
mvn test -Dtest=LoginTest#testValidLogin
```

### 6. Run with TestNG XML
```bash
mvn test -DsuiteXmlFile=src/test/resources/testng.xml
```

## Test Sites Used
- **Primary**: SauceDemo (https://www.saucedemo.com/)
- **Alternative**: OpenCart Demo (https://demo.opencart.com/)

### Valid Test Credentials (SauceDemo)
- **Standard User**: username: `standard_user`, password: `secret_sauce`
- **Problem User**: username: `problem_user`, password: `secret_sauce`
- **Performance User**: username: `performance_glitch_user`, password: `secret_sauce`

## Test Reports
- Screenshots are automatically saved in `screenshots/` directory
- Console logs provide detailed test execution information
- ExtentReports can be configured for HTML reporting

## Configuration
- Browser type can be changed in `testng.xml` or via command line
- Timeouts and waits can be adjusted in `DriverManager.java`
- Test data can be modified in `LoginTest.java` DataProvider methods

## Screenshots
<img width="1510" height="902" alt="Screenshot 2025-09-15 at 12 16 47" src="https://github.com/user-attachments/assets/134cf1d4-7ee8-40f8-8d44-64ef0dc35581" />

