# ExecutionResults/Module_Results_Checkboxes_Tests.md

## Checkboxes Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Linux Ubuntu 22.04 LTS

---

### CB_01: Verify that a single checkbox can be selected
**Start Time:** 20-06-2025 12:41  
**Steps:** Load page → Click first checkbox → Verify it is selected  
**Result:** PASS  
**End Time:** 20-06-2025 12:45  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CB_02: Verify that a selected checkbox can be deselected
**Start Time:** 20-06-2025 12:45  
**Steps:** Ensure checkbox is selected → Click again → Verify it is deselected  
**Result:** PASS  
**End Time:** 20-06-2025 12:49  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CB_03: Verify that both checkboxes can be selected
**Start Time:** 20-06-2025 12:49  
**Steps:** Click both checkboxes → Confirm both are selected  
**Result:** PASS  
**End Time:** 20-06-2025 12:53  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CB_04: Verify stability during rapid select/deselect clicks
**Start Time:** 20-06-2025 12:53  
**Steps:** Rapidly click both checkboxes multiple times → Verify final state is stable → Confirm there are no UI lags or browser crashes
**Result:** PASS  
**End Time:** 20-06-2025 12:58  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CB_05: Verify that clicking outside checkbox area does not change state
**Start Time:** 20-06-2025 12:58  
**Steps:** Click label area, margin, or empty space → Confirm checkbox doesn’t change  
**Result:** FAIL 
**Actual:** Checkbox state changed after clicking outside of the checkbox area  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/CB_05_fail.png) 
**End Time:** 20-06-2025 13:02  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

## Summary

- Total Test Cases: 5
- Passed: 4
- Failed: 1 (Unexpected checkbox state change)
- Key Defect: CB_05 – Clicking near checkbox affects state