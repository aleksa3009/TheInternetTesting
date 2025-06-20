# ExecutionResults/Module_Results.md

## File Upload Test Execution (Chrome)

**Browser:** Chrome 137.0.7151.103
**OS:** Linux Ubuntu 22.04. LTS

---

### FU_01 – Verify uploading a small valid text file (`small.txt`)
**Start Time:** 2025-06-18 09:30  
**Steps:** Choose `small.txt` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 09:38  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_02 – FU_02: Verify uploading a valid image file (`image.jpg`) 
**Start Time:** 2025-06-18 09:42  
**Steps:** Choose `image.jpg` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 09:47  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_03 – Verify uploading a valid PDF file (`sample.pdf`)
**Start Time:** 2025-06-18 09:54  
**Steps:** Choose `sample.pdf` → Upload  
**Result:** FAIL  
**Actual:** Page shows “Upload error: Unsupported file type.”  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_03_fail.png)  
**End Time:** 2025-06-18 10:05  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_04 – Verify uploading a valid 5MB zip file (`5MB.zip`)
**Start Time:** 2025-06-18 10:09  
**Steps:** Choose `5MB.zip` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 10:15  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_05 – Verify uploading a valid 6MB zip file (`6MB.zip`)
**Start Time:** 2025-06-18 10:18  
**Steps:** Choose `6MB.zip` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 10:23  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_06 – Verify uploading a dangerous executable file (`dangerous.exe`)
**Start Time:** 2025-06-18 10:30  
**Steps:** Choose `dangerous.exe` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 10:34  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_07 – Verify uploading a file with maximum allowed filename length (255 chars, `aaaaa...`)
**Start Time:** 2025-06-18 10:44  
**Steps:** Choose `aaaaaaaa…(255 chars)` → Upload  
**Result:** FAIL  
**Actual:** Form field clears selection without error message.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_07_fail.png)  
**End Time:** 2025-06-18 10:51  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_08 – Verify uploading without selecting any file
**Start Time:** 2025-06-18 10:54  
**Steps:** Click Upload with no file chosen  
**Result:** PASS  
**End Time:** 2025-06-18 11:06  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_09 – Verify uploading a file larger than maximum allowed size (.zip >6MB)
**Start Time:** 2025-06-18 11:12 
**Steps:** Choose `10MB.zip` → Upload  
**Result:** FAIL  
**Actual:** System accepts file.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_09_fail.png)  
**End Time:** 2025-06-18 11:23  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_10 – Verify uploading multiple files simultaneously 
**Start Time:** 2025-06-18 11:30  
**Steps:** Select `small.txt` & `image.jpg` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 11:36  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_011 – Verify UI behavior after successful upload
**Start Time:** 2025-06-18 11:43  
**Steps:** Upload `small.txt`, check if UI resets  
**Result:** PASS  
**End Time:** 2025-06-18 11:51  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_012 – Verify drag and drop upload functionality
**Start Time:** 2025-06-18 11:57  
**Steps:** Drag `small.txt` onto upload area  
**Result:** FAIL  
**Actual:** File is not detected when dropped into area. No feedback or error message shown.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_12_fail.png)  
**End Time:** 2025-06-18 12:02  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_013 – Verify re-uploading same file after cancellation
**Start Time:** 2025-06-18 12:05  
**Steps:** Cancel upload of `sample.pdf` → Choose `sample.pdf` → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 12:09  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_014 – Verify removing a selected file before upload 
**Start Time:** 2025-06-18 12:11  
**Steps:** Choose `image.jpg` → Click Clear → Upload  
**Result:** PASS  
**End Time:** 2025-06-18 12:18  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

### FU_015 – Verify that upload button is disabled until a file is selected
**Start Time:** 2025-06-18 12:21  
**Steps:** Observe Upload button → Choose `small.txt`  
**Result:** FAIL  
**Actual:** Upload button is **enabled even before** any file is selected, allowing users to click it without selecting a file. No error message is shown.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_15_fail.png)  
**End Time:** 2025-06-18 12:25  
**Environment:** Linux 22.04 LTS / Chrome 137.0.7151.103

---

## File Upload Test Execution (Firefox)

**Browser:** Firefox 139.0.4  
**OS:** Linux Ubuntu 22.04 LTS  
_(Executed on: 19-06-2025)_

### FU_01 – Verify uploading a small valid text file (`small.txt`)
**Start Time:** 2025-06-19 09:00  
**Steps:** Choose `small.txt` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:05  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_02 – Verify uploading a valid image file (`image.jpg`)
**Start Time:** 2025-06-19 09:08  
**Steps:** Choose `image.jpg` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:15  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_03 – Verify uploading a valid PDF file (`sample.pdf`)
**Start Time:** 2025-06-19 09:18  
**Steps:** Choose `sample.pdf` → Upload  
**Result:** FAIL  
**Actual:** Page shows “Upload error: Unsupported file type.”  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_03_fail_firefox.png)  
**End Time:** 2025-06-19 09:24  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_04 – Verify uploading a valid 5MB zip file (`5MB.zip`)
**Start Time:** 2025-06-19 09:28  
**Steps:** Choose `5MB.zip` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:33  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_05 – Verify uploading a valid 6MB zip file (`6MB.zip`)
**Start Time:** 2025-06-19 09:36 
**Steps:** Choose `6MB.zip` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:44  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_06 – Verify uploading a dangerous executable file (`dangerous.exe`)
**Start Time:** 2025-06-19 09:48  
**Steps:** Choose `dangerous.exe` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:52  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_07 – Verify uploading a file with maximum allowed filename length (255 chars, `aaaaa...`)
**Start Time:** 2025-06-19 09:52  
**Steps:** Choose `aaaaaaaa…(255 chars)` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 09:58  
**Environment:** Linux 22.04 LTS / Firefox 139.0.7151.103

---

### FU_08 – Verify uploading without selecting any file
**Start Time:** 2025-06-19  10:02  
**Steps:** Click Upload with no file chosen  
**Result:** PASS  
**End Time:** 2025-06-19 10:06  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_09 – Verify uploading a file larger than maximum allowed size (.zip >6MB)
**Start Time:** 2025-06-19 10:10  
**Steps:** Choose `10MB.zip` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 10:17  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_10 – Verify uploading multiple files simultaneously
**Start Time:** 2025-06-19 10:20  
**Steps:** Select `small.txt` & `image.jpg` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 10:26  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_011 – Verify UI behavior after successful upload
**Start Time:** 2025-06-19 10:29  
**Steps:** Upload `small.txt`, check if UI resets  
**Result:** PASS  
**End Time:** 2025-06-19 10:37  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_012 – Verify drag and drop upload functionality
**Start Time:** 2025-06-19 10:37  
**Steps:** Drag `small.txt` onto upload area  
**Result:** FAIL  
**Actual:** File not detected, no feedback shown.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_12_fail_firefox.png)  
**End Time:** 2025-06-19 10:43  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_013 – Verify re-uploading same file after cancellation
**Start Time:** 2025-06-19 10:44  
**Steps:** Cancel upload of `sample.pdf` → Choose `sample.pdf` → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 10:49  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_014 – Verify removing a selected file before upload
**Start Time:** 2025-06-19 10:52  
**Steps:** Choose `image.jpg` → Click Clear → Upload  
**Result:** PASS  
**End Time:** 2025-06-19 10:58  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4

---

### FU_015 – Verify that upload button is disabled until a file is selected
**Start Time:** 2025-06-19 11:02  
**Steps:** Observe Upload button → Choose `small.txt`  
**Result:** FAIL  
**Actual:** Upload button remains enabled without file selection.  
![Screenshot](/TheInternetTesting/ExecutionResults/Screenshots/FU_15_fail_firefox.png)  
**End Time:** 2025-06-19 11:11  
**Environment:** Linux 22.04 LTS / Firefox 139.0.4