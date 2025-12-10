# COMP2850 HCI Assessment: Evaluation & Redesign Portfolio

> **📥 Download this template**: [COMP2850-submission-template.md](/downloads/COMP2850-submission-template.md)
> Right-click the link above and select "Save link as..." to download the template file.

**Student**: [Your name and student ID]
**Submission date**: [DD/MM/YYYY]
**Academic Year**: 2025-26

---

## Privacy & Ethics Statement

- [ ] I confirm all participant data is anonymous (session IDs use P1_xxxx format, not real names)
- [ ] I confirm all screenshots are cropped/blurred to remove PII (no names, emails, student IDs visible)
- [ ] I confirm all participants gave informed consent
- [ ] I confirm this work is my own (AI tools used for code assistance are cited below)

**AI tools used** (if any): [e.g., "Copilot for route handler boilerplate (lines 45-67 in diffs)"]

---

**Week 6 Job Story #1**:

1. When I think of something I need to do, I want to be able to quickly add it to my list so that I can remember it later on because I struggle to remember tasks I have set myself.

**How Task 1 tests this**: Task 1 asks the user to create a task (collect mail) and it should be added to the list instantly.

------------------------------------------------------------------------

### [Evaluation Tasks (4-5 tasks)]

#### [Task 1 (T1): \[Add task\]]
- **Scenario**: Need to collect mail
- **Action**: Add task "collect mail"
- **Success**: Task is added to the list
- **Target**: <10 seconds
- **Linked to**: Week 6 Job Story #1 ("quickly add task (using keybord navigation)")


#### [Task 2 (T2): \Amend task name\]

- **Scenario**: Need to collect mail, decide to collect mail and do food shop
- **Action**: Add task "collect mail" and edit to say "collect mail and buy food"
- **Success**: Task is added to the list successfully, and then edited easily without error
- **Target**: <10 seconds
- **Linked to**: Week 6 Job Story #2 ("edit task as plans change")

#### [Task 3 (T3): \[Delete task\]]

-   **Scenario**: Have just walked the dog, want to remove it by searching for and removing it.
-   **Action**: Filter task "walk the dog", click remove
-   **Success**: Task "walk the dog" removed without error
-   **Target time**: <10 seconds
-   **Linked to**: Job story #3 ("Remove task")

#### [Task 4 (T4): \[Read through tasks\]]

-   **Scenario**: Start of the day, want to read through tasks for the day and count them.
-   **Action**: Scroll to bottom of page, read out all 3 given tasks and state there are 3 tasks
-   **Success**: All 3 tasks set read out and numbered
-   **Target time**: <6 seconds
-   **Linked to**: Job story #4 ("Read through and number tasks")


### Consent Script (They Read Verbatim)

**Introduction**:
"Thank you for participating in my HCI evaluation. This will take about 15 minutes. I'm testing my task management interface, not you. There are no right or wrong answers."

**Rights**:
- [ ] "Your participation is voluntary. You can stop at any time without giving a reason."
- [ ] "Your data will be anonymous. I'll use a code (like P1) instead of your name."
- [ ] "I may take screenshots and notes. I'll remove any identifying information."
- [ ] "Do you consent to participate?" [Wait for verbal yes]

**Recorded consent timestamp**:

P1 consented 09/12/2025 15:40
P2 consented 09/12/2025 16:45

---     

## 2. Findings Table

**Instructions**: Fill in this table with 3-5 findings from your pilots. Link each finding to data sources.

| Finding | Data Source | Observation (Quote/Timestamp) | WCAG | Impact (1-5) | Inclusion (1-5) | Effort (1-5) | Priority |
|---------|-------------|------------------------------|------|--------------|-----------------|--------------|----------|
| Keyboard navigation confusing | metrics.csv + P2 notes| P2: "It's hard to tell which button I'm selecting" | WCAG 2.4.7 | 2 | 4 | 1 | 5 |
| No confirmation when adding task | P2 notes | (Opon being asked if they saw confirmation) P1: "No, I did not see any confirmation" | WCAG 3.2.2 | 2 | 3 | 1 | 4 |
| Didn't seen confirmation when removing task | P2 notes | P2: "I saw that it was removed, but nothing else." | WCAG 3.2.2 | 2 | 3 | 1 | 4 |
| P2 exceeded expected times significantly | P2 notes, metrics.csv | Task 2 - expected <10 seconds, took 18, Task 3 - expected <10 seconds, took 18 | WCAG 3.2.2 | 2 | 5 | 4 | 3 |

**Priority formula**: (Impact + Inclusion) - Effort

**Top 3 priorities for redesign**:
1. [Finding #1 - Priority score 5]
2. [Finding #2 - Priority score 4]
3. [Finding #1 - Priority score 4]

---

## 3. Pilot Metrics (metrics.csv)

**Instructions**: Paste your raw CSV data here OR attach metrics.csv file

```csv
ts_iso,session_id,request_id,task_code,step,outcome,ms,http_status,js_mode
2025-11-22T14:18:23.456Z,P1_a7f3,req_001,T1_add,success,,890,200,on
2025-12-09T16:29:36.347797200Z,P1_7a9f,r_6544e5a1,T0_list,success,,23,200,off
2025-12-09T16:30:47.915748300Z,P1_7a9f,r_8404cea5,T4_delete,success,,7,200,on
2025-12-09T16:31:56.142822Z,P1_7a9f,r_72bbdc46,T3_add,success,,16,200,on
2025-12-09T16:33:54.448655800Z,P1_7a9f,r_ee440a3d,T2_edit,success,,7,200,on
2025-12-09T16:36:21.891572700Z,P1_7a9f,r_6d75c48c,T1_filter,success,,8,200,on
2025-12-09T16:36:23.413635700Z,P1_7a9f,r_6c7ee288,T1_filter,success,,9,200,on
2025-12-09T16:36:28.815723600Z,P1_7a9f,r_43ec1b47,T4_delete,success,,6,200,on
2025-12-09T16:37:40.974823500Z,P1_7a9f,r_fb14e612,T1_filter,success,,12,200,on
2025-12-09T16:38:00.518269200Z,P1_7a9f,r_8b57ccf5,T1_filter,success,,9,200,on
2025-12-09T16:40:19.451657Z,P1_7a9f,r_d70330b5,T1_filter,success,,1,200,off
2025-12-09T16:40:19.499657900Z,P1_7a9f,r_f32cf804,T0_list,success,,32,200,off
2025-12-09T16:40:32.700872400Z,P1_7a9f,r_1cbd157d,T3_add,success,,15,200,on
2025-12-09T16:41:31.169836100Z,P1_4a5f,r_1f81860e,T4_delete,success,,5,200,on
2025-12-09T16:43:08.422520600Z,P2_4a5f,r_593bbfa3,T0_list,success,,20,200,off
2025-12-09T16:45:33.604086200Z,P2_4a5f,r_a36e170e,T0_list,success,,18,200,off
2025-12-09T16:45:45.470386500Z,P2_4a5f,r_8ddb0672,T3_add,success,,11,200,on
2025-12-09T16:47:10.848440800Z,P2_4a5f,r_77aa08c0,T2_edit,success,,7,200,on
2025-12-09T16:48:13.019553100Z,P2_4a5f,r_9076bc5d,T1_filter,success,,6,200,on
2025-12-09T16:48:14.092033800Z,P2_4a5f,r_e5887307,T1_filter,success,,7,200,on
2025-12-09T16:48:14.853841200Z,P2_4a5f,r_f3a1fa0e,T1_filter,success,,6,200,on
2025-12-09T16:48:18.720752800Z,P2_4a5f,r_4a037383,T1_filter,success,,4,200,on
2025-12-09T16:48:21.677582700Z,P2_4a5f,r_bb501db3,T1_filter,success,,6,200,on
2025-12-09T16:48:22.599939600Z,P2_4a5f,r_c662c9d2,T1_filter,success,,5,200,on
2025-12-09T16:48:25.443582600Z,P2_4a5f,r_3361975e,T1_filter,success,,8,200,on
2025-12-09T16:48:25.639535700Z,P2_4a5f,r_2820f4c8,T1_filter,success,,6,200,on
2025-12-09T16:48:28.538253700Z,P2_4a5f,r_1bcd2b64,T4_delete,success,,5,200,on
2025-12-09T16:49:08.804420200Z,P2_4a5f,r_4ecdab33,T1_filter,success,,11,200,on
```

**Participant summary**:
- **P1**: [Variant - "Standard mouse + HTMX"]
- **P2**: [Variant - "Keyboard-only + HTMX"]

**Total participants**: [n=2]

---

## 4. Implementation Diffs

**Instructions**: Show before/after code for 1-3 fixes. Link each to findings table.

### Fix 1: [Fix Name]

**Addresses finding**: [Finding #2 from table above]

**Before** ([src\main\resources\templates\_layout\base.peb:14]):
```css
<style>
    /* Visually hidden but accessible to screen readers (WCAG 1.3.1) */
    .visually-hidden {
      position: absolute !important;
      height: 1px;
      width: 1px;
      overflow: hidden;
      clip: rect(1px, 1px, 1px, 1px);
      white-space: nowrap;
    }
    
    /* Skip link for keyboard navigation (WCAG 2.4.1) */
    .skip-link {
      position: absolute;
      left: -10000px;
      width: 1px;
      height: 1px;
      overflow: hidden;
    }
    .skip-link:focus {
      position: static;
      width: auto;
      height: auto;
      background: #1976d2;
      color: white;
      padding: 0.5rem 1rem;
      text-decoration: none;
      font-weight: bold;
      z-index: 9999;
    }
    
    /* Pagination styles */
    .pagination {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }

    /* Override Pico.css button color for WCAG 1.4.3 AA compliance */
    button[type="submit"],
    button {
      color: white !important; /* White text on blue background for better contrast */
    }
  </style>
```

**After** ([src\main\resources\templates\_layout\base.peb:58]):
```css
    /* AMENDED CODE ------------- */
    /* Make button focus better contrasted with button */
    button:focus {
      outline: 3px solid light-dark(#000000,#ffffff);
      outline-offset: 2px;
    }
    /*---------------------------- */
  </style>
```

**What changed**: I added css to base.peb so that when selecting the button the focus highlight is better contrasted with the button, both in light and dark mode.

**Why**: This fixed WCAG 2.4.7 - Focus Visible, as although the original highlighting colour was well contrasted against text fields and the page background, it wasn't well contrasted against the buttons themselves.

**Impact**: This improves the user experience as it is now more clear what is being selected when using keyboard navigation, as it was flagged by peer pilot P2, who was using keyboard navigation. In general, this makes the website more accessible to anyone using keyboard navigation, expecially those who are partially sighted and therefore may struggle to differentiate between colours, whilst also relying on keyboard navigation. When re-testing with a peer pilot using keyboard navigation, this should decrease the time taken to perform tasks requiring keyboard navigation over buttons.

---

### Fix 2: [Fix Name]

**Addresses finding**: [Finding #X]

**Before**:
```kotlin
[Original code]
```

**After**:
```kotlin
[Fixed code]
```

**What changed**:

**Why**:

**Impact**:

---

[Add Fix 3 if applicable]

---

## 5. Verification Results

### Part A: Regression Checklist (20 checks)

**Instructions**: Test all 20 criteria. Mark pass/fail/n/a + add notes.

| Check | Criterion | Level | Result | Notes |
|-------|-----------|-------|--------|-------|
| **Keyboard (5)** | | | | |
| K1 | 2.1.1 All actions keyboard accessible | A | [pass] | All buttons and fields accessible by tab and usable by keyboard |
| K2 | 2.4.7 Focus visible | AA | [fail] | 2px border on active elements, similar colour to buttons |
| K3 | No keyboard traps | A | [pass] | Can go through entire page and fill in text boxes (i.e. filter and add) without any trap |
| K4 | Logical tab order | A | [pass] | Pressing tab takes the focus from the top to the bottom |
| K5 | Skip links present | AA | [pass] | Skip to main content perfectly functional |
| **Forms (3)** | | | | |
| F1 | 3.3.2 Labels present | A | [pass] | All input fields have a label which is read by screenreader |
| F2 | 3.3.1 Errors identified | A | [pass/fail] | All errors have attribute role=alert, added in routing code whenever an error is handled |
| F3 | 4.1.2 Name/role/value | A | [pass] | [e.g., "All form controls have accessible names"] |
| **Dynamic (3)** | | | | |
| D1 | 4.1.3 Status messages | AA | [pass] | [e.g., "Status div has role=status"] |
| D2 | Live regions work | AA | [fail] | NVDA does not mention "task added" |
| D3 | Focus management | A | [fail] | Focus does not move after submitting |
| **No-JS (3)** | | | | |
| N1 | Full feature parity | — | [pass] | All CRUD operations work without JS enabled |
| N2 | POST-Redirect-GET | — | [pass] | Refreshing doesn't resend any data |
| N3 | Errors visible | A | [pass] | Errors still shown without JS enabled |
| **Visual (3)** | | | | |
| V1 | 1.4.3 Contrast minimum | AA | [pass] | Text is 16:1 against buttons and 13:1 against background, and 5:1 between default text and text field backgrounds (e.g. "Type to filter..." against filter textbox) which is just above the 4:1 requirement for smaller text |
| V2 | 1.4.4 Resize text | AA | [pass] | Everything remains clear even at maximum () |
| V3 | 1.4.11 Non-text contrast | AA | [pass] | [e.g., "Focus indicator 4.5:1"] Focus indicator 5.2:1 against button and (after fix #1) and 17:1 against background so easily distinguishable against both |
| **Semantic (3)** | | | | |
| S1 | 1.3.1 Headings hierarchy | A | [pass] | Headings all clearly declared programmatically, lower heading always follows a higher heading |
| S2 | 2.4.1 Bypass blocks | A | [pass] | "Skip to main content" option available at top of page |
| S3 | 1.1.1 Alt text | A | [pass] | No images present on page |

**Summary**: [X/20 pass], [Y/20 fail]
**Critical failures** (if any): [List any Level A fails]

---

### Part B: Before/After Comparison

**Instructions**: Compare Week 9 baseline (pre-fix) to Week 10 (post-fix). Show improvement.

| Metric | Before (Week 9, n=X) | After (Week 10, n=Y) | Change | Target Met? |
|--------|----------------------|----------------------|--------|-------------|
| SR error detection | [e.g., 0/2 (0%)] | [e.g., 2/2 (100%)] | [e.g., +100%] | [✅/❌] |
| Validation error rate | [e.g., 33%] | [e.g., 0%] | [e.g., -33%] | [✅/❌] |
| Median time [Task X] | [e.g., 1400ms] | [e.g., 1150ms] | [e.g., -250ms] | [✅/❌] |
| WCAG [criterion] pass | [fail] | [pass] | [— ] | [✅/❌] |

**Re-pilot details**:
- **P5** (post-fix): [Variant - e.g., "Screen reader user, NVDA + keyboard"] - [Date piloted]
- **P6** (if applicable): [Variant] - [Date]

**Limitations / Honest reporting**:
[If metrics didn't improve or only modestly: explain why. Small sample size? Wrong fix? Needs more iteration? Be honest - valued over perfect results.]

---

## 6. Evidence Folder Contents

**Instructions**: List all files in your evidence/ folder. Provide context.

### Screenshots

| Filename | What it shows | Context/Link to finding |
|----------|---------------|-------------------------|
| button-contrast-before.png | Highlighting around button not well contrasted against button itself | Finding #1 - Low contrast when selecting buttons |
| button-contrast-after.png | Button selected with better contrast | Fix #1 |
| regression-axe-report.png | axe DevTools showing 0 violations | Verification Part A |
| [your-screenshot-3.png] | [Description] | [Which finding/fix this supports] |

**PII check**:
- [ ] All screenshots cropped to show only relevant UI
- [ ] Browser bookmarks/tabs not visible
- [X] Participant names/emails blurred or not visible

---

### Pilot Notes

**Instructions**: Attach pilot notes as separate files (P1-notes.md, P2-notes.md, etc.). Summarize key observations here.

**P1** ([ Variant - Standard mouse+keyboard + HTMX]):
- **Key observation 1**: [Quote + timestamp - e.g., "Struggled with filter button (09:47)"] Didn't notice any explicit confirmation when deleting task () - "I can't see any confirmation but I can see it's no longer in the list"
- **Key observation 2**: [Quote + timestamp]

**P2** ([Variant - Keyboard navigation + HTMX]):
- **Key observation 1**: [Quote + timestamp]
- **Key observation 2**: [Quote + timestamp]

[Repeat for P3, P4 if applicable]

---

## Evidence Chain Example (Full Trace)

**Instructions**: Pick ONE finding and show complete evidence trail from data → fix → verification.

**Finding selected**: [e.g., "Finding #1 - SR errors not announced"]

**Evidence trail**:
1. **Data**: metrics.csv lines 47-49 show P2 (SR user) triggered validation_error 3 times
2. **Observation**: P2 pilot notes timestamp 14:23 - Quote: "I don't know if it worked, didn't hear anything"
3. **Screenshot**: before-sr-error.png shows error message has no role="alert" or aria-live
4. **WCAG**: 3.3.1 Error Identification (Level A) violation - errors not programmatically announced
5. **Prioritisation**: findings-table.csv row 1 - Priority score 7 (Impact 5 + Inclusion 5 - Effort 3)
6. **Fix**: implementation-diffs.md Fix #1 - Added role="alert" + aria-live="assertive" to error span
7. **Verification**: verification.csv Part A row F2 - 3.3.1 now PASS (tested with NVDA)
8. **Before/after**: verification.csv Part B - SR error detection improved from 0% to 100%
9. **Re-pilot**: P5 (SR user) pilot notes - "Heard error announcement immediately, corrected and succeeded"

**Complete chain**: Data → Observation → Interpretation → Fix → Verification ✅

---

## Submission Checklist

Before submitting, verify:

**Files**:
- [ ] This completed template (submission-template.md)
- [X] metrics.csv (or pasted into Section 3)
- [-] Pilot notes (P1-notes.md, P2-notes.md, etc. OR summarised in Section 6)
- [ ] Screenshots folder (all images referenced above)
- [ ] Privacy statement signed (top of document)

**Evidence chains**:
- [X] findings-table.csv links to metrics.csv lines AND/OR pilot notes timestamps
- [ ] implementation-diffs.md references findings from table
- [ ] verification.csv Part B shows before/after for fixes

**Quality**:
- [ ] No PII in screenshots (checked twice!)
- [ ] Session IDs anonymous (P1_xxxx format, not real names)
- [ ] Honest reporting (limitations acknowledged if metrics didn't improve)
- [ ] WCAG criteria cited specifically (e.g., "3.3.1" not just "accessibility")

**Pass criteria met**:
- [X] n=2+ participants (metrics.csv has 2+ session IDs)
- [ ] 3+ findings with evidence (findings-table.csv complete)
- [ ] 1-3 fixes implemented (implementation-diffs.md shows code)
- [ ] Regression complete (verification.csv has 20 checks)
- [ ] Before/after shown (verification.csv Part B has data)

---

**Ready to submit?** Upload this file + evidence folder to Gradescope by end of Week 10.

**Estimated completion time**: 12-15 hours across Weeks 9-10

**Good luck!** 🎯
