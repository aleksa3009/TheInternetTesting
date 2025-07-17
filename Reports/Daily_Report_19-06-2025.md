# Daily Report – Day 3 (19-06-2025)

## Activities:
- Executed 15 File Upload test cases on **Firefox**
  - 12 PASS  
  - 3 FAIL (screenshots saved in `ExecutionResults/Screenshots/`)
- Performed 45 minutes of exploratory testing
- Found 3 additional unexpected behaviors
- Logged 3 bugs in GitHub Issues (`#7`, `#8`, `#9`)

## Environment:
- **OS:** Linux Ubuntu 22.04 LTS  
- **Browser:** Firefox 139.0.4  
- **Test Data Used:**  
  - `small.txt`, `image.jpg`, `sample.pdf`, `5MB.zip`, `6MB.zip`, `dangerous.exe`, `file_with_255_characters.txt`

## Exploratory Testing Findings:
1. **Drag and drop sometimes triggers two upload events**
   - *Description:* When dragging the file too quickly onto the drop zone, the page registers two upload attempts.
   - *Impact:* May cause duplicate submissions or unintended server requests.
   - *Severity:* Medium
   - *Recommendation:* Debounce the drop event or limit to one active upload per file.

2. **"No file selected" label remains even after selecting a file**
   - *Description:* After choosing a file, the label doesn't update to reflect the selected filename.
   - *Impact:* Misleads user into thinking file wasn't selected.
   - *Severity:* Medium
   - *Recommendation:* Ensure the label dynamically updates on file input change.

3. **Upload confirmation message overlaps input field**
   - *Description:* On smaller resolutions (under 1024px width), the confirmation text overlaps the "Choose File" button.
   - *Impact:* Hurts UX and may block further interaction.
   - *Severity:* Low-Medium
   - *Recommendation:* Improve responsive layout and spacing for confirmation message.

## Issues Logged:
- GitHub Issue IDs: `#7`, `#8`, `#9`

## Next Steps:
- Write test cases for **Dynamic Controls** and and **Checkboxes** 
- Execute test cases for **Dynamic Controls** and **Checkboxes** on Chrome
- Continue exploratory testing
- Log new bugs and write `Daily_Report_20-06-2025.md`
