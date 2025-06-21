# Daily Report – Day 5 (21-06-2025)

## Activities:
- Executed 9 test cases on **Context Menu** and **Broken Images** modules using Chrome and Firefox  
  - **Context Menu:** 5 TC total → 4 **PASS**, 1 **FAIL** (screenshots saved in `ExecutionResults/Screenshots/`)  
  - **Broken Images:** 4 TC total → 3 **PASS**, 1 **FAIL**  
- Performed 45 minutes of exploratory testing  
- Found 2 unexpected behaviors (1 in Context Menu, 1 in Broken Images)  
- Logged 4 new bugs in GitHub Issues (`#14`, `#15`, `#16`, `#17`)

## Environment:
- **OS:** Linux Ubuntu 22.04 LTS  
- **Browsers:**  
  - **Chrome:** 137.0.7151.119  
  - **Firefox:** 139.0.4  

## Test Data Used:
- No external files used; all interactions were UI/DOM-based (images, alerts, context areas)

## Exploratory Testing Findings:

1. **[Context Menu] Right-click fails after double-click on hotspot**  
   - **Description:** If a user double-clicks the hotspot and then right-clicks, the context alert fails to appear.  
   - **Impact:** Inconsistent behavior may confuse users and reduce usability.  
   - **Severity:** Medium  
   - **Recommendation:** Add debounce logic or block conflicting click events.

2. **[Broken Images] Alt attribute missing on second broken image**  
   - **Description:** The second broken image does not have an `alt` tag defined in the DOM.  
   - **Impact:** Breaks accessibility compliance; screen readers cannot describe the image.  
   - **Severity:** Low  
   - **Recommendation:** Ensure all images (including broken ones) have `alt` attributes.

## Issues Logged:
- GitHub Issue IDs: `#14`, `#15`, `#16`, `#17`

## Next Steps:
- Review all `Module_Results_*.md` files and ensure:
  - All test cases are covered (**PASS**/**FAIL**)
  - All **FAIL** cases have corresponding **screenshots**
- Clean up and organize all GitHub Issues:
  - Add **comments** for retested or clarified bugs
- Start writing `Reports/Final_Report.md`
