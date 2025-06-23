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

---

## Repository Structure

```  
TheInternetTesting/
├── TestPlan/                   # Detailed Test Plan and schedule
│   └── Test_Plan.md            # Scope, Objectives, Roles, Risks, Environment, Schedule
├── TestCases/                  # Test case definitions
│   ├── the_internet_testing-file_upload_test_cases.pdf        # 15 TC covering upload flows
│   ├── the_internet_testing-checkboxes_test_cases.pdf         # 9 TC focusing on enable/disable and race conditions
│   ├── the_internet_testing-dynamic_controls_test_cases.pdf   # 5 TC for selection stability
│   ├── the_internet_testing-context_menu_tests.pdf            # 5 TC for right-click behavior
│   ├── the_internet_testing-broken_images_test_cases.pdf      # 4 TC for image load states
|   └── 
├── TestData/                   # Files used in File Upload tests
│   ├── small.txt
|   ├── aaaaaaaaaaaaaaaaaaaaaaa...txt
│   ├── čšđč.txt
│   ├── image.jpg
│   ├── sample.pdf
│   ├── 5MB.zip
│   ├── 6MB.zip
│   ├── 10MB.zip 
│   └── dangerous.exe
├── ExecutionResults/           # Execution logs and evidence
│   ├── Module_Results_File_Upload_Tests.md
│   ├── Module_Results_Dynamic_Controls_Tests.md
│   ├── Module_Results_Checkboxes_Tests.md
│   ├── Module_Results_ContextMenu_Tests.md
|   ├── Module_Results_BrokenIMages_Tests.md
│   └── Screenshots/            # All FAIL-case screenshots
└── Reports/                    # Daily & Final reports
    ├── Daily_Report_17-06-2025.md
    ├── Daily_Report_18-06-2025.md
    ├── Daily_Report_19-06-2025.md
    ├── Daily_Report_20-06-2025.md
    ├── Daily_Report_21-06-2025.md
    ├── Daily_Report_22-06-2025.md
    └── Final_Report.md         # Comprehensive summary
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
3. **Day 2:** Execute File Upload on Chrome; exploratory session; log 5 bugs
4. **Day 3:** Execute File Upload on Firefox; retest; log additional bugs; daily report
5. **Day 4:** Create & execute Dynamic Controls & Checkboxes tests; retest; log 4 bugs
6. **Day 5:** Create & execute Context Menu & Broken Images tests; exploratory; log 4 bugs
7. **Day 6:** Final verification of execution results, bug cleanup, begin Final Report
8. **Day 7:** Complete Final Report; prepare portfolio README; craft CV entry

**Daily Reports** document execution details and exploratory findings, located in `Reports/`.

---

## Test Coverage & Metrics

| Module           | TC Count | Browsers Tested | PASS | FAIL | Bugs Logged | Exploratory (min) |
| ---------------- | -------- | --------------- | ---- | ---- | ----------- | ----------------- |
| File Upload      | 15       | Chrome, Firefox | 23   | 7    | 8           | 60                |
| Dynamic Controls | 9        | Chrome          | 6    | 3    | 3           | 60                |
| Checkboxes       | 5        | Chrome          | 4    | 1    | 1           | 30                |
| Context Menu     | 5        | Chrome, Firefox | 8    | 2    | 2           | 30                |
| Broken Images    | 4        | Chrome, Firefox | 6    | 2    | 2           | 45                |

- **Total TC Executed:** 38 per browser (62 runs)
- **Total Bugs Reported:** 16
- **Average Duration per TC:** \~10 minutes

---

## Defect Analysis & Trends

**High Severity:**

- Race conditions in Dynamic Controls (DC\_06)
- Premature input acceptance (DC\_08)
- Drag-and-drop failures (FU\_012)

**Medium Severity:**

- Silent file upload failures (FU\_07, FU\_09)
- Unexpected alerts (CM\_04)
- Missing alt text on broken images (BI\_03)

**Low Severity:**

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

## Key Recommendations

1. Implement **explicit wait** and **disable UI** during asynchronous operations.
2. Provide **clear feedback** on invalid user actions (e.g., empty upload, failed drop).
3. Debounce rapid user inputs to avoid race conditions.
4. Enforce **accessibility** by always including meaningful `alt` attributes.
5. Consolidate logs and use **consistent commit messages** for traceability.

---

## Conclusion

This project illustrates a structured manual QA approach, delivering:

- Detailed planning artifacts
- Comprehensive test suites and execution logs
- 16 actionable defect reports with reproducible steps
- Professional daily and final reporting

The documented process and artifacts form a strong portfolio demonstration of manual testing competencies for a junior QA role.

---

*End of README*
