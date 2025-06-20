# Daily Report – Day 4 (20-06-2025)

## Activities:
- Executed 14 test cases on **Dynamic Controls** and **Checkboxes** modules using Chrome  
  - **Dynamic Controls:** 9 TC total → 6 PASS, 3 FAIL (screenshots in `ExecutionResults/screenshots/`)  
  - **Checkboxes:** 5 TC total → 4 PASS, 1 FAIL  
- Performed 40 minutes of exploratory testing  
- Found 3 unexpected behaviors (2 in Dynamic Controls, 1 in Checkboxes)  
- Logged 4 new bugs in GitHub Issues (`#10`, `#11`, `#12`, `#13`)  

## Environment:
- **OS:** Linux Ubuntu 22.04 LTS  
- **Browser:** Chrome 137.0.7151.119  
- **Test Data Used:**  
  - No external files used for these modules; all interactions were UI-based.

## Exploratory Testing Findings:

1. **[Dynamic Controls] Enable/Disable buttons trigger multiple status messages**  
   - *Description:* Rapid clicks on Enable/Disable sometimes stack multiple "Please wait..." or "It's enabled" messages without clearing the previous one.  
   - *Impact:* Leads to confusing UI behavior and possible message overlap.  
   - *Severity:* Medium  
   - *Recommendation:* Ensure status container is cleared before rendering new message.

2. **[Dynamic Controls] Input field flickers briefly during enable transition**  
   - *Description:* While enabling the input field, it flickers (visible DOM refresh) before becoming editable.  
   - *Impact:* Affects UI stability perception; might hint at redundant rendering or reflow.  
   - *Severity:* Low  
   - *Recommendation:* Debounce or optimize rendering during transition.

3. **[Checkboxes] Clicking label margin toggles checkbox state unexpectedly**  
   - *Description:* Clicking the label near its edge (outside the text) still triggers the checkbox toggle.  
   - *Impact:* May cause accidental interactions if users click near the box but not intentionally.  
   - *Severity:* Low  
   - *Recommendation:* Add more precise hitbox mapping or padding rules for label interaction.

## Issues Logged:
- GitHub Issue IDs: `#10`, `#11`, `#12`, `#13`

## Next Steps:
- ✅ **Day 5 Tasks – Context Menu + Broken Images + Bug Retesting**
  - Write test cases for Context Menu and Broken Images modules
  - Execute test cases on both Chrome and Firefox
  - Perform exploratory testing (focus: lazy loading, missing alt attributes, context interactions)
  - Retest logged bugs (`#2`–`#13`) for reproducibility
  - Write Daily Report + update `ExecutionResults/` documents
