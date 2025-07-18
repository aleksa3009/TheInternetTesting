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
- Cross-browser testing on latest stable versions: Chrome (137.0.7151.103, 137.0.7151.119), Firefox (139.0.4)
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

- **Ubuntu:** 22.04 LTS

**Browsers:**

- **Google Chrome:** 137.0.7151.103 & 137.0.7151.119
- **Mozilla Firefox:** 139.0.4

**Tools & Frameworks:**

- **Test Case Management:** TestRail
- **Bug Tracking:** GitHub Issues
- **Editor:** VS Code
- **Screenshots:** LibreOffice Draw / Flameshot
- **Data Preparation:** LibreOffice Calc / Google Sheets
- **Version Control:** Git & GitHub

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

A total of **38 test cases** were designed and executed accross key functional modules:

- **File Upload:** 15 test cases covering valid, invalid, edge-case and boundary scenarios
- **Dynamic Controls:** 9 test cases verifying asynchronous behavior and element state changes
- **Checkboxes:** 5 test cases focusing on selection logic and default states
- **Context Menu:** 5 test cases validating right-click behavior and alert handling
- **Broken Images:** 4 test cases inspecting image loading and accessibility compliance

All test cases followed a consistent template structure, including:

- **Test CaseID**
-  **Title** 
-  **Preconditions** 
-  **Test Steps**
-  **Expected Results**
-  **Type** (Functional, Negative, Boundary, UI) 
-  **Priority** (High/ Medium/ Low)

---

## 6. Execution Summary

| Module           | Browser | TC | PASS | FAIL | Exploratory (min) | Bugs Logged |
| ---------------- | ------- | -- | ---- | ---- | ----------------- | ----------- |
| File Upload      | Chrome  | 15 | 10   | 5    | 15                | 5           |
| File Upload      | Firefox | 15 | 12   | 3    | 15                | 3           |
| Dynamic Controls | Chrome  | 9  | 6    | 3    | 30                | 3           |
| Checkboxes       | Chrome  | 5  | 4    | 1    | 15                | 1           |
| Context Menu     | Chrome  | 5  | 4    | 1    | 15                | 1           |
| Broken Images    | Chrome  | 4  | 3    | 1    | 15                | 1           |
| Context Menu     | Firefox | 5  | 4    | 1    | 15                | 1           |
| Broken Images    | Firefox | 4  | 3    | 1    | 15                | 1           |

**Total Execution Time:** ~24 hours
**Total Test Cases Executed:** 62
**Total Bugs Logged:** 16
**Overall Pass Rate:** ~81%
**Browsers Covered:** Chrome 137.0.7151.103 & 137.0.7151.119; Firefox 139.0.4
**Test Types:** Functional, Negative, Exploratory, UI

---

## 7. Defect Analysis

**Defects by Severity:**

- **High:** (4)
  -  Rrace conditions in dynamic controls 
  -  Premature input acceptance before UI state is ready 
  -  Drag-and-drop area fails to handle unsupported files gracefully
- **Medium:** (8) 
  - Silent upload failures with no error feedback 
  - Unexpected alert pop-ups disrupting user flow
  - Missing alt attributes impacting accessibility
- **Low:** (4) 
  - Minor UI flickering during transitions 
  - Inconsistent spacing and layout on form elements

**Root Cause Summary:**

- **Improper synchronization** of asynchronous operations, particularly in dynamic controls and file handling modules
- **Lack of user feedback** for invalid or edge-case (e.g. uploading large files, double-triggered UI elements)
- **Accessibility oversights**, such as missing semantic attributes (alt) in image-based components

---

## 8. Exploratory Testing Highlights

1. **Upload button remains enabled** after a successful file upload - this may mislead users into thinking another upload is required or still in progress.
2. **Rapid toggling of dynamic controls** causes multiple overlapping status messages, leading to visual clutter and possible confusion..
3. **Drag-and-drop area lacks feedback** when unsupported file types or methods are used - users receive no indication of failure or limitations.
4. **Context menu intermittenly fails** when triggered via double-click instead of right-click - a poential usability inconsistency.
5. **Broken images module missing alt text** for the second image - this violates accessibility standards and hinders screen reader support.

---

## 9. Lessons Learned & Recommendations

1. Implementing **explicit waits** for async UI actions significantly reduces test flakiness and improves overall reliability of manual testing workflows.
2. Ensuring **form resets behavior** and clearly defined **disabled/enabled states** enhances UX clarity and minimizes user errors.
3. Applying **debounce logic** to user-triggered actions (e.g. double-clicks, rapid submissions) helps prevent race conditions and inconsistent UI states.
4. Enforcing the use of **alt text for all images** promotes accessibility and improves semantic HTML structure, benefiting both usability and compliance..
5. Maintaining **consistent, detailed, and traceable test documentation** improves reproducibility, simplifies debugging, and strengthens team communication.

---

## 10. Conclusion

This project presents a strong demonstration of manual testing practices, resulting in a complete suite of test artifacts, the indentification of 16 defects, and actionable QA recommendations.

It showcases practical skills relevant to QA entry-level roles, such as designing boundary and negative test scenarios, analyzing response structures etc. The combination of exploratory and structured testing led to the discovery of multiple non-obvious defects.

All findings were documented transparently to provide traceability and reproducibility. This project serves as a meaningful and independent portfolio example, showcasing readiness for real-world manual QA responsibilities.

---


