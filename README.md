
# **State Savings Automation**

**CRAFT** is a robust test automation framework designed to handle API and UI testing seamlessly. Built with Java, TestNG, and Cucumber, it supports structured and reusable components for efficient and scalable test automation.

---

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Folder Structure](#folder-structure)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Test Execution](#test-execution)
7. [Configuration Files](#configuration-files)
8. [Reports and Logs](#reports-and-logs)
9. [Test Data](#test-data)
10. [Contact](#contact)

---

## **Project Overview**
This framework provides support for:
- **API Testing**: Automates API tests with endpoint validation.
- **UI Testing**: Uses the Page Object Model (POM) design for UI interactions.
- **Reporting**: Generates comprehensive test reports using Extent and Allure.
- **Scalable Architecture**: Organized components for reusability and modularity.

---

## **Folder Structure**
### **Root Directory**
- `/SSAutomation`: Root directory of the framework.

### **Source Code Directory (`src`)**
- `/main`: Main application code (future extension scope).
- `/test`: Test-related source code:
  - `/java`: Java test classes:
    - `/cucumbercraft`: Cucumber-related reusable components.
    - `/entity`: Classes representing data entities for test operations.
    - `/framework`: Utilities and configurations to support the framework.
    - `/models`: Data models for API and UI testing.
    - `/POMPages`: Page Object Model classes for UI interactions.
    - `/runners`: TestNG runner classes:
      - `RunCucumberTests.java`: For generic test execution.
      - `RunCucumberTests_Api.java`: For API test execution.
      - `RunCucumberTests_Regression.java`: For regression test execution.
    - `/stepdefinitions`: Cucumber step definitions:
      - `YourStepDefinitions.java`: Contains test steps linked to Gherkin feature files.
  - `/resources`: Test resources:
    - `/endpoints`: API endpoint configuration.
      - `EndPointInputs`: Stores endpoint inputs.
    - `/test-data`: Test data files:
      - `Automation Data.xlsx`
      - `Buy Now Automation.xlsx`
      - `Buy Now Test Data.xlsx`
    - `/config`: Configuration files:
      - `allure.properties`: Allure reporting configuration.
      - `extent.properties`: Extent reporting configuration.
      - `extent-config.xml`: Extent report customization.
      - `Framework MetaData.xml`: Metadata for framework setup.
      - `Global Settings.properties`: Global settings for the framework.
      - `log4j.xml`, `log4j2.properties`, `logback.xml`: Logging configurations.
      - `spark-config.xml`: Spark report configuration.

### **Results and Logs**
- `/results`: Stores test execution reports.
  - `your-test-report.html`: Example test report output.
- `/logs`: Stores log files generated during test execution.
  - `your-log-file.log`: Example log file.

### **TestNG XML Files (`/testng`)**
- `TestNGRunAPITests.xml`: For running API tests.
- `TestNGRunParallelTests.xml`: For parallel test execution.
- `TestNGRunRegressionTests.xml`: For regression suite.
- `TestNGRunSmokeTests.xml`: For smoke suite.

---

## **Prerequisites**
- **Java**: Version 11  
- **Maven**: Dependency and build management  
- **Cucumber**: For BDD-based testing  
- **TestNG**: For test execution and orchestration  
- **Allure or Extent Reports** (optional for advanced reporting)

---

## **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/username/SSAutomation.git
   ```
2. Navigate to the project directory:
   ```bash
   cd SSAutomation
   ```
3. Install dependencies:
   ```bash
   mvn clean install
   ```

---

## **Usage**
### **Run Tests**
Use runners or TestNG XML files for executing specific test suites:
```bash
  mvn test -Dcucumber.filter.tags="@Smoke"
```

### **Customize Configurations**
Modify properties in the configuration files:
```bash
  resources/config/Global Settings.properties
```

---

## **Test Execution**
### **Run Using TestNG**
Execute a specific suite:
```bash
  mvn test -DsuiteXmlFile=testng/TestNGRunSmokeTests.xml
```

### **Run Using IDE**
1. Open runner classes in the `runners` folder.
2. Right-click on a runner and select:
   ```text
   Run as TestNG Test
   ```

### **Run Specific Tags**
Filter tests by Cucumber tags:
```bash
  mvn test -Dcucumber.filter.tags="@Regression"
```

---

## **Configuration Files**
Customize the framework using files in the `resources/config` directory:
- `Global Settings.properties`: Global framework settings.
- `log4j2.properties`, `logback.xml`: Logging configurations.
- `extent-config.xml`: Extent report template.
- `allure.properties`: Allure reporting options.

---

## **Reports and Logs**
- **Reports**:
    - Stored in the `/results` directory.
    - Open `your-test-report.html` to view Extent or Allure reports.
- **Logs**:
    - Logs are in the `/logs` directory.
    - Example log file: `your-log-file.log`.

---

## **Test Data**
Test data is stored in the `resources/test-data` directory:
- `Automation Data.xlsx`: Generic test data.
- `Buy Now Automation.xlsx`: Data specific to "Buy Now" tests.
- `Buy Now Test Data.xlsx`: Additional test scenarios.

---

## **Contact**
For issues, queries, or contributions, contact the project maintainer:
- **Author**: [Your Name](https://github.com/yourprofile)
- **Email**: [your.email@example.com](mailto:your.email@example.com)
- **LinkedIn**: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)

---

## **Reviewer**
- **Reviewer**: [Reviewer Name](https://github.com/reviewerprofile)
- **Email**: [reviewer.email@example.com](mailto:reviewer.email@example.com)
- **LinkedIn**: [linkedin.com/in/reviewerprofile](https://linkedin.com/in/reviewerprofile)
```
This README provides detailed documentation for understanding and working with the project. Feel free to reach out for any assistance!
