# 📄 Test Plan: The Internet - Manual Testing of Core UI Modules

**Version:** 2.0
**Author:** Aleksa Aleksić
**Date:** 17.06.2025.
**Project Name:** The Internet UI Functional Verification
**Base URL:** [https://the-internet.herokuapp.com](https://the-internet.herokuapp.com)
**Changelog:**  
- 2.0 – 17.07.2025. – Major revision: Added traceability, updated scope and exit criteria.
---

## 1. 📘 Introduction
This document serves as a formal test plan for the manual verification of five core user interface (UI) modules of the public demonstration website [The Internet](https://the-internet.herokuapp.com).

It defines the overall **testing strategy, scope, required resources and execution schedule** for this project. The primary objectives are to ensure:
- Systematic functional validation of key modules
- Timely identification of potential risks and defects
- Accurate and documented defect reporting. 

The resulting documentation is intended to demonstrate a structured and professional approach to quality assurance, suitable for inclusion in a QA portfolio.

---

## 2. 🎯 Scope

This test plan covers the **manual functional testing** of selected UI modules on [The Internet](https://the-internet.herokuapp.com) website, reflecting the actual testing performed during the project. The scope includes:

**In Scope:**
- Functional manual testing of the following modules:
  - **File Upload**
  - **Dynamic Controls**
  - **Checkboxes**
  - **Context Menu**
  - **Broken Images**
- Boundary Value Analysis (BVA) and negative testing for data limits and error conditions
- Cross-browser verification (Google Chrome and Mozilla Firefox)
- Exploratory testing sessions to uncover unexpected behaviors
- Documentation of results, logs, and defects

**Out of Scope**
- Accessibility compliance testing beyond verifying alt text on broken images
- Performance, load, or security testing
- Automated test scripts or API testing

**Traceability:**
All test cases and defects are tracked using TestRail and GitHub Issues, ensuring clear linkage between requirements, test executions and reported bugs.

---

## 3. 🎯 Objectives

The primary objectives of this test plan are to: 

- Validate that each selected UI module meets its specified functional requirements
- Identify and document defects with clear reproduction steps and relevant evidence
- Ensure boundary conditions and error handling are correctly implemented
- Perform cross-browser testing to confirm consistent behavior on supported browsers
- Produce a complete set of test artifacts (plans, cases, logs, defect reports, summaries)
- Demonstrate a professional approach to manual testing suitable for portfolio presentation

---

## 4. 👥 Roles and Responsibilities

| Role       | Name                   | Responsibility                     |
|------------|------------------------|------------------------------------|
| Tester     | Aleksa Aleksić          | Drafting test plan, creating and executing test cases, logging results, raising defects|
| Stakeholder| Self / Development Team | Reviewing and triaging defect reports  |
| Reviewer   | Aleksa Aleksić          | Providing feedback on test artifacts and final reports|

---

## 5. 📦 Test Items

|Module Name     | Description                                                     |
|----------------|-----------------------------------------------------------------|
| File Upload     | Upload various file types and sizes; test positive/negative flows|
| Dynamic Controls| Verify enable/disable functionality of input fields and adding/removing checkboxes             |
| Checkboxes      | Select/deselect one or multiple checkboxes; test rapid toggling        |
| Context Menu    | Trigger and handle right-click context menu alerts               |
| Broken Images   | Verify count and alt text of broken images, scroll behavior      |

---

## 6. 🛠️ Test Approach and Strategy
1. **Test Types:** Functional, boundary, negative, exploratory
2. **Test Design:** 
   - Risk-based prioritization to focus on high-impact and high-likelihood cases
   - Detailed, step-by-step test cases documented in TestRail
3. **Execution Order:**
   1. File Upload
   2. Dynamic Controls
   3. Checkboxes
   4. Context Menu
   5. Broken Images
4. **Cross-Browser:** All tests executed on latest versions of Google Chrome and Mozilla Firefox
5. **Defect Reporting:** Defects are logged in GitHub Issues using predefined templates for consistency and completeness
6. **Time Tracking:** Start and end times are recorded for each test case exeuction and exploratory testing session

---

## 7. 🛠️ Environment and Tools

**Hardware & OS:** Ubuntu 22.04. LTS
**Browsers:** Google Chrome (137.0.7151.103), Mozilla Firefox (139.0.4)
**Tools:**
- **Test Case Management:** TestRail
- **Defect Tracking:** GitHub Issues
- **Editor:** Visual Studio Code (VCS)
- **Screenshot:** Flameshot and LibreOffice Draw
- **Data Preparation:** Google Sheets
- **Version Control:** Git & GitHub ([TheInternetTesting](https://github.com/aleksa3009/TheInternetTesting) repository)

---

## 8. ✅ Entry Criteria

The testing process will begin when the following conditions are met: 
- Project directory structure is created and organized
- Google Chrome (v137.0.7151.103), Mozilla Firefox (v139.0.4), and screenshot/editor tools (Flameshot, LibreOffice Draw) are installed and verified
- Access to TestRail (for test case management) and GitHub Issues (for defect tracking) is confirmed
- Required test data files are available and validated in `TestData/`
- Templates for test cases and defect reports are prepared and ready to use

---

## 9. ✅ Exit Criteria

**Module-Level Exit:**
- All test cases executed (PASS/FAIL recorded)
- Defecs logged with clear reproduction steps, screenshots, environment details
- Exploratory testing session completed and documened
- Daily summary report generated and reviewed

**Project-Level Exit:**
- All modules satisfy exit criteria
- Final comprehensive test summary report completed, reviewed, and approved
- All test artifacts and reports archived in `Reports/`

---

## 10. ⚠️ Risks and Mitigation

|Risk                                   |Likelihood|Impact|Priority|Mitigation                                         |
|---------------------------------------|----------|------|--------|---------------------------------------------------|
|Uploading files >5MB may be blocked    |Medium    |High  |High    |Test boundary sizes; verify error messages         |
|Dynamic Controls timing issues         |High      |Medium|High    |Introduce explicit wait steps; repeat rapid toggles|
|Cross-browser rendering inconsistencies|Medium    |Medium|Medium  |Execute on both browsers; compare screenshots      |
|Missing alt text on images             |Low       |Low   |Low     |Manually verify alt attributes during Broken Images|

---

## 11. 📦 Deliverables

- Test Plan Document (`TestPlan/Test_Plan.md`)
- Test Case Suite in TestRail (38 cases)
- Test Data files in `TestData/`
- Execution Logs & Screenshots in `ExecutionResults`
- Defect Reports (12) in GitHub Issues
- Daily Reports (`Reports/Daily_Report_DD-MM-YYYY.md`)
- Final Summary Report (`Reports/Final_Report.md`) 

---

## 12. Schedule

### Day 0: Folder Setup & Tool Installation

|Activity                                                                                            |Duration  |
|----------------------------------------------------------------------------------------------------|----------|
|Create folder structure (`~/TheInternetTesting/` and subfolders)                                    |15 minutes|
|Install and configure browsers (Chrome, Firefox), editors (VS Code) and screenshot tools (Flameshot)|30 minutes|
|Set up GitHub repository for bug tracking                                                           |1 hour    |

---

### Day 1: Test Plan + Test Data + File Upload Test Cases

|Activity                                                 |Duration  |
|---------------------------------------------------------|----------|
|Write Test Plan (`TestPlan/Test_Plan.md`)                |2 hours   |
|Prepare test data in the `TestData/` folder              |30 minutes|
|Create File Upload test cases in TestRail (15 test cases)|2 hours   |
|Set up tools: open TestRail, GitHub Issues, editor       |30 minutes|
|Buffer / Clarifications                                  |30 minutes|

---

### Day 2: Execute File Upload Tests (Chrome)

|Activity                                                  |Duration  |
|----------------------------------------------------------|----------|
|Execute all 15 File Upload test cases on Chrome           |3 hours   |
|Exploratory testing (15 minutes) and document 2–3 findings|15 minutes|
|Start logging bugs on GitHub (3–5 bugs)                   |1 hour    |

---

### Day 3: Execute File Upload Tests (Firefox) + Bug Tracking

|Activity                                                    |Duration  |
|------------------------------------------------------------|----------|
|Execute File Upload tests on Firefox                        |2.5 hours |
|Exploratory testing (15 minutes) and add 2–3 additional bugs|1 hour    |
|Complete bug logging (target total: 10 bugs)                |30 minutes|
|Write daily report (`Reports/Daily_Report_DD-MM-YYYY.md`)   |30 minutes|

---

### Day 4: Dynamic Controls + Checkboxes – Test Cases & Execution

|Activity                                                       |Duration  |
|---------------------------------------------------------------|----------|
|Write test cases for Dynamic Controls and Checkboxes (14 TC)   |1.5 hours |
|Execute tests on Chrome                                        |1.5 hours |
|Exploratory testing (focus on race conditions and rapid clicks)|1 hour    |
|Log additional bugs and write daily report                     |1 hour    |

---

### Day 5: Context Menu + Broken Images + Bug Retest

| Activity                                                 |Duration  |
|----------------------------------------------------------|----------|
|Write test cases for Context Menu and Broken Images (9 TC)|1 hour    |
|Execute tests on Chrome and Firefox                       |1.5 hours |
|Exploratory testing (e.g., lazy loading, alt text)        |1 hour    |
|Retest bugs and verify reproducibility                    |1 hour    |
|Write daily report and update ExecutionResults            |30 minutes|

---

### Day 6: Final Testing + Bug Closure + Screenshot Verification

|Activity                                                           |Duration|
|---------------------------------------------------------------    |--------|
|Review `Module_Results.md` for coverage and screenshots            |2 hours |
|Clean and organize bugs in GitHub, assign severity and add comments|2 hours |
|Start writing final report (`Reports/Final_Report.md`)             |1 hour  |

---

### Day 7: Final Report + Portfolio & CV Preparation

|Activity                                                          |Duration  |
|------------------------------------------------------------------|----------|
|Finish final report (scope, coverage, defects, lessons learned)   |2 hours   |
|Create GitHub README with project description and links           |1 hour    |
|Prepare screenshots for portfolio (upload to Imgur or GitHub)     |1 hour    |
|Add project to CV with description of activities and technologies |1 hour    |

## 13. 📂 Initial Project Directory Structure

```bash
TheInternetTesting/
├── TestPlan/
│   └── Test_Plan.md
├── TestCases/
│   └── FileUpload_Test_Cases_Screenshots/
├── TestData/
│   └── sample_files/
├── ExecutionResults/
│   └── Screenshots/
├── Reports/
│   └── Daily_Report_DD-MM-YYYY.md
└── README.md
```