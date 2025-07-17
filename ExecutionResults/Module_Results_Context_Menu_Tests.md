# ExecutionResults/Module_Results_Context_Menu_Tests.md

## Context Menu Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Linux Ubuntu 22.04 LTS

---

### CM_01: Verify alert text appears on right-click hotspot
**Start Time:** 21-06-2025 11:30  
**Steps:** Right-click hotspot → Observe alert text  
**Result:** PASS  
**End Time:** 21-06-2025 11:34  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CM_02: Verify no page change when dismissing alert
**Start Time:** 21-06-2025 11:34  
**Steps:** Right-click hotspot → Click Cancel  
**Result:** PASS  
**End Time:** 21-06-2025 11:39  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CM_03: Verify expected behavior when accepting alert
**Start Time:** 21-06-2025 11:39  
**Steps:** Right-click hotspot → Click OK  
**Result:** PASS  
**End Time:** 21-06-2025 11:45  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CM_04: Verify no alert when clicking outside hotspot
**Start Time:** 21-06-2025 11:45  
**Steps:** Click outside hotspot → Observe no alert  
**Result:** FAIL  
**Actual:** Unexpected alert appears when clicking outside hotspot  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/CM_04_fail.png)  
**End Time:** 21-06-2025 11:52  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### CM_05: Verify behavior during rapid right-click and double-click combo
**Start Time:** 21-06-2025 11:52  
**Steps:** Rapid right-click + double-click hotspot  
**Result:** PASS  
**End Time:** 21-06-2025 11:56  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

## Context Menu Test Execution (Firefox)

**Browser:** Firefox 139.0.4  
**OS:** Linux Ubuntu 22.04 LTS  
_(Executed on: 21-06-2025)_

### CM_01: Verify alert text appears on right-click hotspot
**Start Time:** 21-06-2025 11:56  
**Steps:** Right-click hotspot → Observe alert text  
**Result:** PASS  
**End Time:** 21-06-2025 12:01  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### CM_02: Verify no page change when dismissing alert
**Start Time:** 21-06-2025 12:01  
**Steps:** Right-click hotspot → Click Cancel  
**Result:** PASS  
**End Time:** 21-06-2025 12:06  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### CM_03: Verify expected behavior when accepting alert
**Start Time:** 21-06-2025 12:06  
**Steps:** Right-click hotspot → Click OK  
**Result:** PASS  
**End Time:** 21-06-2025 12:10  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### CM_04: Verify no alert when clicking outside hotspot
**Start Time:** 21-06-2025 12:10  
**Steps:** Click outside hotspot → Observe no alert  
**Result:** FAIL  
**Actual:** Unexpected alert appears when clicking outside hotspot  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/CM_04_fail_firefox.png)  
**End Time:** 21-06-2025 12:15  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### CM_05: Verify behavior during rapid right-click and double-click combo
**Start Time:** 21-06-2025 12:15  
**Steps:** Rapid right-click + double-click hotspot  
**Result:** PASS  
**End Time:** 21-06-2025 12:19  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

## Summary

- Total Test Cases Executed: 10 (5 on Chrome, 5 on Firefox)  
- Passed: 8  
- Failed: 2 (Same failure in both browsers)  
- Key Defect: CM_04 – Alert incorrectly triggered when clicking outside the context menu hotspot