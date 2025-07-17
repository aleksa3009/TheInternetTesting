# Daily Report – Day 2 (18-06-2025)

## Activities:
- Executed 15 File Upload test cases on Chrome
  - 10 PASS
  - 5 FAIL (screenshots saved in `ExecutionResults/Screenshots/`)
- Performed 35 minutes of exploratory testing
- Found 2 additional unexpected behaviors
- Logged 5 bugs in GitHub Issues (`#2`, `#3`, `#4`, `#5`, `#6`)

## Environment:
- **OS:** Linux Ubuntu 22.04 LTS
- **Browser:** Chrome 137.0.7151.103
- **Test Data Used:**
  - `small.txt`, `image.jpg`, `sample.pdf`, `5MB.zip`, `6MB.zip`, `dangerous.exe`, `file_with_255_characters.txt`

## Exploratory Testing Findings:
1. **Upload button remains active after successful upload**
   - *Description:* Upload button does not get disabled or reset after successful upload.
   - *Impact:* Might confuse users into clicking it again without selecting a new file.
   - *Severity:* Low-Medium
   - *Recommendation:* Reset the form or disable the button post-upload.

2. **File name with Unicode characters not displayed correctly**
   - *Description:* File named `ćevap.txt` displayed as `Ä‡evap.txt`.
   - *Impact:* Character encoding issue leads to incorrect display.
   - *Severity:* Medium
   - *Recommendation:* Investigate and fix character encoding handling.

## Issues Logged:
- GitHub Issue IDs: `#2`, `#3`, `#4`, `#5`, `#6`

## Next Steps:
- Execute the same 15 File Upload test cases on **Firefox**
- Continue logging bugs (target: 8 total)
- Write `Daily_Report_19-06-2025.md`
