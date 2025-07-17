# Final Report – The Internet Manual Testing Project

**Project:** Manual Testing of Core UI Modules on "The Internet" Demo Site\
**Tester:** Aleksa Aleksić\
**Duration:** 17-06-2025 to 22-06-2025\
**Base URL:** [https://the-internet.herokuapp.com]

---

## 1. Introduction

This report outlines a structured manual testing initiative conducted on five critical UI modules of the public demo site **The Internet**. Over the course of six working days, the project applied a combination of functional, boundary, negative, positive and exploratory testing approaches. Cross-browser validation was performed using Chrome and Firefox, with all activities documented in a professional and reproducible format using industry-standard tools.

**Note:** This is a personal portfolio project. A few of the reported bugs were intentionally fabricated to demonstrate defect documentation and reporting skills.

---

## 2. Scope & Objectives

**Scope:**

- Functional verification of modules: File Upload, Dynamic Controls, Checkboxes, Context Menu, Broken Images
- Cross-browser coverage (Chrome 137.0.7151.103, 137.0.7151.119; Firefox 139.0.4)
- Exploratory sessions targeting asynchronous behaviors and UI stability
- Documentation of 38 test cases, execution logs, defect reports, and daily summaries

**Objectives:**

1. Validate core functionality, error handling, and boundary conditions.
2. Identify and log defects with precise reproduction steps and screenshots.
3. Perform risk-based and exploratory testing to uncover hidden issues.
4. Produce professional artifacts suitable for inclusion in a QA portfolio and CV.

---

## 3. Test Environment & Tools

**Hardware & OS:**

- Ubuntu 22.04 LTS

**Browsers:**

- Google Chrome 137.0.7151.119
- Mozilla Firefox 139.0.4

**Tools & Frameworks:**

- Test Case Management: TestRail
- Bug Tracking: GitHub Issues
- Editor: VS Code
- Screenshots: LibreOffice Draw / Flameshot
- Data Preparation: LibreOffice Calc / Google Sheets
- Version Control: Git & GitHub

---

## 4. Folder Structure & Artifacts

```
~/TheInternetTesting/
├── TestPlan/                   # Test planning documents
│   └── Test_Plan.md
├── TestCases/                  # TestRail exports
│   ├── FileUpload_TC.xlsx
│   ├── DynamicControls_TC.xlsx
│   ├── Checkboxes_TC.xlsx
│   ├── ContextMenu_TC.xlsx
│   └── BrokenImages_TC.xlsx
├── TestData/                   # Files used for File Upload testing
│   ├── small.txt
│   ├── image.jpg
│   ├── sample.pdf
│   ├── 5MB.zip
│   ├── 6MB.zip
│   ├── 10MB.zip
│   └── dangerous.exe
├── ExecutionResults/           # Execution logs and screenshots
│   ├── Module_Results_File_Upload_Tests.md
│   ├── Module_Results_Dynamic_Controls_Tests.md
│   ├── Module_Results_Checkboxes_Tests.md
│   ├── Module_Results_ContextMenu_BrokenImages_Tests.md
│   └── screenshots/
└── Reports/                    # Daily and Final reports
    ├── Daily_Report_17-06-2025.md
    ├── Daily_Report_18-06-2025.md
    ├── Daily_Report_19-06-2025.md
    ├── Daily_Report_20-06-2025.md
    ├── Daily_Report_21-06-2025.md
    └── Final_Report.md
```

---

## 5. Test Case Coverage

A total of **38 test cases** were designed and executed per module:

- **File Upload:** 15 cases
- **Dynamic Controls:** 9 cases
- **Checkboxes:** 5 cases
- **Context Menu:** 5 cases
- **Broken Images:** 4 cases

Test case templates included:

- **ID**, **Title**, **Preconditions**, **Test Steps**, **Expected Results**, **Type**, **Priority**

---

## 6. Execution Summary

| Module           | Browser | TC | PASS | FAIL | Exploratory (min) | Bugs Logged |
| ---------------- | ------- | -- | ---- | ---- | ----------------- | ----------- |
| File Upload      | Chrome  | 15 | 10   | 5    | 15                | 5           |
| File Upload      | Firefox | 15 | 13   | 2    | 15                | 3           |
| Dynamic Controls | Chrome  | 9  | 6    | 3    | 30                | 3           |
| Checkboxes       | Chrome  | 5  | 4    | 1    | 15                | 1           |
| Context Menu     | Chrome  | 5  | 4    | 1    | 15                | 1           |
| Broken Images    | Chrome  | 4  | 3    | 1    | 15                | 1           |
| Context Menu     | Firefox | 5  | 4    | 1    | 15                | 1           |
| Broken Images    | Firefox | 4  | 3    | 1    | 15                | 1           |

**Total Execution Time:** \~24 hours **Total Bugs Logged:** 16

---

## 7. Defect Analysis

**Defects by Severity:**

- **High:** 6 (race conditions, premature input, drag-and-drop failure)
- **Medium:** 7 (silent upload failures, unexpected alerts, missing alt text)
- **Low:** 4 (UI flicker, layout minor issues)

**Root Causes:**

- Asynchronous operations not synchronized (Dynamic Controls, drag-and-drop)
- Missing UI feedback for invalid actions (upload button, file size)
- Accessibility oversights (missing alt attributes)

---

## 8. Exploratory Testing Highlights

1. **Upload button remains enabled** after successful upload – potential UX trap.
2. **Rapid toggles** cause multiple overlapping status messages.
3. **Drag-and-drop** area gives no feedback when unsupported.
4. **Context menu** sometimes fails if double-clicked.
5. **Broken images** second image lacking alt text breaks accessibility.

---

## 9. Lessons Learned & Recommendations

1. **Explicit waits** for async UI actions reduce flakiness.
2. **Form resets** and disable states improve UX clarity.
3. **Debounce user actions** to prevent race conditions.
4. **Enforce alt text** for all images – accessibility first.
5. **Consistent test documentation** ensures reproducibility.

---

## 10. Conclusion

This project delivers a robust demonstration of manual testing practices, producing a full suite of test artifacts, uncovering 16 defects, and providing actionable recommendations.

The work reflects practical QA skills relevant to entry-level roles, such as designing boundary and negative test scenarios, analyzing response structures etc. Additionally, the combination of exploratory and structured testing led to the discovery of multiple non-obvious defects.

All findings and artifacts were documented transparently to provide traceability and reproducibility. This project serves as a meaningful and independent portfolio example, showcasing readiness for real-world manual QA responsibilities.

---


