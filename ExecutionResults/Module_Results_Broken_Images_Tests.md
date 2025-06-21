# ExecutionResults/Module_Results_Broken_Images_Tests.md

## Broken Images Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.119  
**OS:** Linux Ubuntu 22.04 LTS

---

### BI_01: Verify count of broken images equals 2
**Start Time:** 2025-06-21 12:19  
**Steps:** Count broken `<img>` elements  
**Result:** PASS  
**End Time:** 2025-06-21 12:23  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### BI_02: Verify alt text for each broken image
**Start Time:** 2025-06-21 12:23  
**Steps:** Inspect alt attributes of broken images  
**Result:** PASS  
**End Time:** 2025-06-21 12:28  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### BI_03: Verify images remain broken after reload
**Start Time:** 2025-06-21 12:28  
**Steps:** Reload page → Count broken images  
**Result:** FAIL  
**Actual:** One previously broken image now displays a placeholder error icon instead of alt text  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/BI_03_fail.png)  
**End Time:** 2025-06-21 12:34  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

### BI_04: Verify lazy-load scenario: scroll triggers load
**Start Time:** 2025-06-21 12:34  
**Steps:** Scroll to bottom → Observe image load  
**Result:** PASS  
**End Time:** 2025-06-21 12:38  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.119

---

## Broken Images Test Execution (Firefox)

**Browser:** Firefox 139.0.4  
**OS:** Linux Ubuntu 22.04 LTS  
_(Executed on: 2025-06-21)_

### BI_01: Verify count of broken images equals 2
**Start Time:** 2025-06-21 12:40  
**Steps:** Count broken `<img>` elements  
**Result:** PASS  
**End Time:** 2025-06-21 12:45  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### BI_02: Verify alt text for each broken image
**Start Time:** 2025-06-21 12:45  
**Steps:** Inspect alt attributes of broken images  
**Result:** PASS  
**End Time:** 2025-06-21 12:49  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### BI_03: Verify images remain broken after reload
**Start Time:** 2025-06-21 12:49  
**Steps:** Reload page → Count broken images  
**Result:** FAIL  
**Actual:** One broken image now shows a broken icon without alt text  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/BI_03_fail_firefox.png)  
**End Time:** 2025-06-21 12:55  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### BI_04: Verify lazy-load scenario: scroll triggers load
**Start Time:** 2025-06-21 12:55  
**Steps:** Scroll to bottom → Observe image load  
**Result:** PASS  
**End Time:** 2025-06-21 12:59  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4