# Bug Retest Results – 21-06-2025

## Retest Execution Summary
Re-tested all previously logged bugs in both Chrome (137.0.7151.119) and Firefox (139.0.4).

---

### Bug ID: #2 – FU_03: [BUG] PDF file is rejected as unsupported during upload (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** Unsupported type error persists.

---

### Bug ID: #3 – FU_07: [BUG] Upload fails silently for file with 255-character filename (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** Selection clears without message; needs fix.

---

### Bug ID: #4 – FU_09: [BUG] System accepts .zip file exceeding size limit without warning (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Not Reproducible  
- **Comment:** Now rejects oversized file as expected.

---

### Bug ID: #5 – FU_012: [BUG] Drag and drop upload does not detect file or provide feedback (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** No feedback on drop; remains unresolved.

---

### Bug ID: #6 – FU_015: [BUG] Upload button is active before file is selected (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Not Reproducible  
- **Comment:** Button remains disabled until selection.

---

### Bug ID: #7 – FU_03: [BUG] Valid PDF upload fails with unsupported type error (Firefox)
- **Retested on Firefox 139.0.4**  
- **Status:** Still Reproducible  
- **Comment:** Error message persists for PDF upload.

---

### Bug ID: #8 – FU_012: [BUG] Drag and drop upload shows no feedback on drop (Firefox)
- **Retested on Firefox 139.0.4**  
- **Status:** Still Reproducible  
- **Comment:** Drop area still unresponsive, no feedback.

---

### Bug ID: #9 – FU_015: [BUG] Upload button is clickable with no file selected (Firefox)
- **Retested on Firefox 139.0.4**  
- **Status:** Not Reproducible  
- **Comment:** Button now disabled until file is selected.

---

### Bug ID: #10 – CB_05: [BUG] Checkbox toggles when clicking outside its visible area (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** Clicks near label continue to toggle checkbox.  

---


### Bug ID: #11 – DC_02: [BUG] Input loses text when typing before enable completes (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Not Reproducible  
- **Comment:** Text is retained after enable confirmation; fix likely applied.  

---

### Bug ID: #12 – DC_06: [BUG] UI stuck in loading state during rapid Enable/Disable toggles (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** Loading spinner remains active indefinitely on rapid toggles.  

---

### Bug ID: #13 – DC_08: [BUG] Input field accepts keystrokes before enable completes (Chrome)
- **Retested on Chrome 137.0.7151.119**  
- **Status:** Still Reproducible  
- **Comment:** Input accepts keystrokes prematurely before enable confirmation.  

---