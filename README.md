# Grazioso Salvare Dashboard Enhancement Repository

## Overview
The Grazioso Salvare Dashboard is a real-time data visualization and filtering tool designed to assist animal rescue organizations in analyzing and managing rescue animal data. It uses MongoDB for database storage and retrieval, along with Dash and Plotly for a dynamic user interface. However, the initial application had several limitations in its database operations, including inefficient query performance, hardcoded credentials, limited error handling, and the absence of formal testing for its CRUD operations. 

This enhancement focused on addressing these challenges through four major improvements: query optimizations, secure credential handling, structured error management, and the development of unit tests for CRUD functionality. These updates align with industry best practices for scalable, secure, and efficient database solutions while significantly improving the application’s usability and maintainability.

## Key Enhancements
### 1. Query Optimization
- **Issue:** Frequently queried fields (`breed`, `location`, `animal_type`) lacked indexing, leading to slower data retrieval.
- **Solution:** Added MongoDB indexes to these fields using the `createIndex()` method and verified them with `getIndexes()`.
- **Impact:** Enhanced query performance, ensuring near-instantaneous filtering and improved scalability for larger datasets.

### 2. Secure Credential Storage
- **Issue:** Hardcoded database credentials in the source code posed significant security risks.
- **Solution:** Replaced hardcoded credentials with environment variables using Python’s `os.getenv()` function.
- **Impact:** Strengthened security by eliminating sensitive data from the codebase and improved maintainability by allowing credential updates without modifying the code.

### 3. Structured Error Handling
- **Issue:** Errors during CRUD operations were only printed to the console, making debugging difficult and reducing reliability.
- **Solution:** Implemented structured error handling using Python’s `try-except` blocks and centralized error logging in a file (`crud_operations.log`).
- **Impact:** Improved debugging efficiency, streamlined issue tracking, and enhanced application reliability with user-friendly error feedback.

### 4. Unit Testing for CRUD Operations
- **Issue:** No formal tests existed to validate CRUD functionality, increasing the risk of undetected bugs.
- **Solution:** Developed a comprehensive suite of unit tests in `test_crud_operations.py` to validate CRUD operations. A separate `test_animals` collection was used to prevent interference with production data.
- **Impact:** Improved reliability by proactively identifying potential issues and established a robust foundation for future development.

## Screenshots
### Enhancement 3
- **Dash_Filter:** Dashboard filtering in action  
  ![Dash_Filter](Screenshots/Enhancement%203/Dash_Filter.png)

- **Dash_Modules:** Code for enhanced dashboard integration  
  ![Dash_Modules](Screenshots/Enhancement%203/Dash_Modules.png)

- **Indexes:** MongoDB indexes for optimized query performance  
  ![Indexes](Screenshots/Enhancement%203/Indexes.png)

- **Log:** Example of centralized error logging  
  ![Log](Screenshots/Enhancement%203/Log.png)

- **Test_Crud:** Successful unit test execution for CRUD operations  
  ![Test_Crud](Screenshots/Enhancement%203/Test_Crud.png)

- **User_Pass:** Environment variables used for secure credential storage  
  ![User_Pass](Screenshots/Enhancement%203/User_Pass.png)

- **User_Pass_Global:** Global credential setup validation  
  ![User_Pass_Global](Screenshots/Enhancement%203/User_Pass_Global.png)

### Project 2 Screenshots
- **Disaster:** Original dashboard filtering based on rescue type  
  ![Disaster](Screenshots/Project%202%20Screenshots/Disaster.png)

- **Mountain:** Original dashboard filtering based on rescue type  
  ![Mountain](Screenshots/Project%202%20Screenshots/Mountain.png)

- **Reset:** Original dashboard filtering based on rescue type  
  ![Reset](Screenshots/Project%202%20Screenshots/Reset.png)

- **Startup:** Original dashboard filtering based on rescue type  
  ![Startup](Screenshots/Project%202%20Screenshots/Startup.png)

- **Water:** Original dashboard filtering based on rescue type  
  ![Water](Screenshots/Project%202%20Screenshots/Water.png)

## Conclusion
The Grazioso Salvare Dashboard is now a more efficient, secure, and reliable tool for managing rescue animal data. Through query optimization, credential security, structured error handling, and unit testing, this enhancement demonstrates my proficiency in database management and secure software practices, aligning with CS-499 outcomes and industry standards.
