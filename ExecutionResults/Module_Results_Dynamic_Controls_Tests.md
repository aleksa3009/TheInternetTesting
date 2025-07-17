# ExecutionResults/Module_Results_Dynamic_Controls_Tests.md

## Dynamic Controls Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Linux Ubuntu 22.04 LTS

---

### DC_01: Verify that clicking Enable makes input editable 
**Start Time:** 20-06-2025 11:25  
**Steps:** Click “Enable” → Wait until enabled → Try typing  
**Result:** PASS  
**End Time:** 20-06-2025 11:33  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_02: Verify input interaction after enabling with wait handling 
**Start Time:** 20-06-2025 11:33  
**Steps:** Click “Enable” → Immediately type text before enable completes  
**Result:** FAIL  
**Actual:** Text "Test input" is lost  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/DC_02_fail.png)  
**End Time:** 20-06-2025 11:42  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_03: Verify that clicking "Disable" makes input read-only 
**Start Time:** 20-06-2025 11:43  
**Steps:** Click “Disable” → Wait until disabled → Try typing  
**Result:** PASS  
**End Time:** 20-06-2025 11:48  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_04: Verify that Add button displays the checkbox 
**Start Time:** 20-06-2025 11:48  
**Steps:** Click “Add” → Wait for checkbox to appear  
**Result:** PASS  
**End Time:** 20-06-2025 11:56  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_05: Verify that Remove button deletes the checkbox 
**Start Time:** 20-06-2025 11:56  
**Steps:** Click “Remove” → Wait for checkbox to disappear  
**Result:** PASS  
**End Time:** 20-06-2025 12:03  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_06: Verify behavior when rapidly clicking Enable/Disable 
**Start Time:** 20-06-2025 12:03  
**Steps:** Rapidly click Enable/Disable multiple times  
**Result:** FAIL  
**Actual:** UI gets stuck in loading state; input field doesn’t stabilize  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/DC_06_fail.png)  
**End Time:** 20-06-2025 12:09  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_07: Verify correctness of status message after action 
**Start Time:** 20-06-2025 12:09  
**Steps:** Click “Enable” → Observe message  
**Result:** PASS  
**End Time:** 20-06-2025 12:15  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_08: Verify that typing is blocked if input is disabled 
**Start Time:** 20-06-2025 12:15  
**Steps:** Click “Enable” → Type text instantly  
**Result:** FAIL  
**Actual:** Text field accepts keystrokes before it’s enabled  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/DC_08_fail.png)  
**End Time:** 20-06-2025 12:23  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### DC_09: Verify unexpected behavior during rapid toggles and input 
**Start Time:** 20-06-2025 12:23  
**Steps:** Randomly click Enable/Disable, try inputs  
**Result:** PASS  
**End Time:** 20-06-2025 12:28  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

## Summary

- Total Test Cases Executed: 9  
- Passed: 6  
- Failed: 3  
- Key Defects:
  - DC_02 – Input text lost if typed before enable completes
  - DC_06 – UI stuck when rapidly toggling Enable/Disable
  - DC_08 – Input accepts keystrokes while still disabled
