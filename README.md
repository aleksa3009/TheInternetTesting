# The Internet – Manual Testing Project

**A comprehensive manual testing suite for five core UI modules of "The Internet" demo site**

---

## Project Overview

This repository demonstrates a full manual QA cycle, from planning to final reporting, performed over a condensed five-day sprint. It covers:

- **Functional** testing of critical UI components
- **Boundary** and **negative** scenarios for robust coverage
- **Exploratory** testing for uncovering hidden issues
- **Cross-browser** validation on Chrome and Firefox

**Target Modules:** File Upload, Dynamic Controls, Checkboxes, Context Menu, Broken Images

**Project Timeline:** 17-06-2025 to 23-06-2025

This project simulates real-world QA workflows to showcase practical manual testing skills applicable for junior QA roles.

---

## Repository Structure

```
TheInternetTesting/
├── README.md
├── TestPlan/
│   └── Test_Plan.md
├── TestData/
│   ├── 5MB.zip
│   ├── 6MB.zip
│   ├── 10MB.zip
│   ├── aaa....txt
│   ├── čšđć:,.txt
│   ├── dangerous.exe
│   ├── images.jpg
│   ├── sample.pdf
│   ├── small.txt
│   └── README.md
├── TestCases/
│   ├── the_internet_testing - file_upload_test_cases.pdf
│   ├── the_internet_testing - dynamic_controls_test_cases.pdf
│   ├── the_internet_testing-context_menu_tests.pdf
│   ├── the_internet_testing - checkboxes_test_cases.pdf
│   ├── the_internet_testing-broken_images_test_cases.pdf
│   ├── File_Upload_Test_Cases_Screenshots/
│   ├── Dynamic_Controls_Test_Cases_Screenshots/
│   ├── Context_Menu_Test_Cases_Screenshots/
│   ├── Checkboxes_Test_Cases_Screenshots/
│   └── Broken_Images_Test_Cases_Screenshots/
├── Reports/
│   ├── Final_Report.md
│   ├── Daily_Report_17-06-2025.md
│   ├── Daily_Report_18-06-2025.md
│   ├── Daily_Report_19-06-2025.md
│   ├── Daily_Report_20-06-2025.md
│   ├── Daily_Report_21-06-2025.md
│   └── Daily_Report_22-06-2025.md
└── ExecutionResults/
    ├── Bug_Retest_21-06-2025.md
    ├── Module_Results_Broken_Images_Tests.md
    ├── Module_Results_Checkboxes_Tests.md
    ├── Module_Results_Context_Menu_Tests.md
    ├── Module_Results_Dynamic_Controls_Tests.md
    ├── Module_Results_File_Upload_Tests.md
    └── Screenshots/

```

---

## Tools & Environment

- **Operating System:** Ubuntu 22.04 LTS (primary), Windows 10 Pro (verification)
- **Browsers:**
  - Google Chrome 137.0.7151.103, 137.0.7151.119
  - Mozilla Firefox 139.0.4
- **Test Management:** TestRail (offline export to Google Sheets (.pdf))
- **Bug Tracking:** GitHub Issues (issue template, labels)
- **Editors:** VS Code
- **Screenshots:** Flameshot, LibreOffice Draw
- **Data Preparation:** Microsoft Excel, Google Sheets, LibreOffice Calc
- **Version Control:** Git, GitHub

---

## Test Planning & Execution Flow

1. **Day 0:** Folder setup, tool installation, GitHub repo initialization
2. **Day 1:** Write Test Plan; prepare `TestData`; design 15 File Upload test cases
3. **Day 2:** Execute File Upload on Chrome; exploratory testing session; log 5 bugs
4. **Day 3:** Execute File Upload on Firefox; retest; log additional bugs; daily report
5. **Day 4:** Create and execute Dynamic Controls & Checkboxes tests; retest; log 4 bugs
6. **Day 5:** Create and execute Context Menu & Broken Images tests; exploratory testing sessions; log 4 bugs
7. **Day 6:** Final verification of execution results, bug cleanup, begin Final Report
8. **Day 7:** Complete Final Report; prepare portfolio README; craft CV entry

**Daily Reports** document execution details and exploratory findings, located in `Reports/` directory.

---

## Test Coverage & Metrics

| Module           | TC Count | Browsers Tested | PASS | FAIL | Bugs Logged | Exploratory (min) |
| ---------------- | -------- | --------------- | ---- | ---- | ----------- | ----------------- |
| File Upload      | 15       | Chrome, Firefox | 23   | 7    | 8           | 60                |
| Dynamic Controls | 9        | Chrome          | 6    | 3    | 3           | 60                |
| Checkboxes       | 5        | Chrome          | 4    | 1    | 1           | 30                |
| Context Menu     | 5        | Chrome, Firefox | 8    | 2    | 2           | 30                |
| Broken Images    | 4        | Chrome, Firefox | 6    | 2    | 2           | 45                |

- **Total TC Executed:** 38 test cases executed across Chrome and Firefox (62 total runs)
- **Total Bugs Reported:** 16
- **Average Duration per TC:** \~10 minutes

---

## Defect Analysis & Trends

**High Severity Defects:**

- Race conditions in Dynamic Controls (DC\_06)
- Premature input acceptance (DC\_08)
- Drag-and-drop failures (FU\_012)

**Medium Severity Defects:**

- Silent file upload failures (FU\_07, FU\_09)
- Unexpected alerts (CM\_04)
- Missing alt text on broken images (BI\_03)

**Low Severity Defects:**

- UI flicker during control transitions
- Checkbox hitbox issues

**Trend Observations:** Most defects stemmed from asynchronous UI changes and lack of user feedback on invalid actions.

---

## Exploratory Testing Highlights

1. **Upload button remains active** after successful upload – potential UX confusion.
2. **Stacked status messages** appear during rapid enable/disable toggles.
3. **Drag-and-drop zone** gives no visual feedback on drop.
4. **Context menu hotspot** fails after double-click.
5. **Accessibility lapse:** second broken image missing `alt` text.

---

## 9. Lessons Learned & Recommendations

1. Implementing **explicit waits** for async UI actions significantly reduces test flakiness and improves overall reliability of manual testing workflows.
2. Ensuring **form resets behavior** and clearly defined **disabled/enabled states** enhances UX clarity and minimizes user errors.
3. Applying **debounce logic** to user-triggered actions (e.g. double-clicks, rapid submissions) helps prevent race conditions and inconsistent UI states.
4. Enforcing the use of **alt text for all images** promotes accessibility and improves semantic HTML structure, benefiting both usability and compliance..
5. Maintaining **consistent, detailed, and traceable test documentation** improves reproducibility, simplifies debugging, and strengthens team communication.

---

## Conclusion

This manual testing project successfully demonstrates a comprehensive QA lifecycle applied to the “The Internet” demo site. Through meticulous planning, test case design, and cross-browser execution, a broad spectrum of functional, boundary, and exploratory tests were conducted across five critical UI modules.

A total of 16 defects were identified, analyzed, and documented with clear reproduction steps, screenshots, and severity classifications. The combination of structured test cases and exploratory sessions uncovered both expected and non-obvious issues, showcasing practical testing skills relevant for junior QA roles.

The project artifacts — including detailed test plans, execution results, daily and final reports — provide clear traceability and professional standards in QA documentation. This work not only validates the application under test but also serves as a strong portfolio example illustrating readiness for real-world manual testing responsibilities.

**Note:** This is a personal portfolio project. A few of the reported bugs were intentionally fabricated to demonstrate defect documentation and reporting skills.

---

*End of README*
