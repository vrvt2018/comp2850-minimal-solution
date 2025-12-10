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
| Keyboard navigation confusing | metrics.csv + P2 notes| P2: "It's hard to tell which button I'm selecting" | WCAG 2.4.7 | 2 | 3 | 2 | 4 |
| No confirmation when adding task | P2 notes | (Opon being asked if they saw confirmation) P1: "No, I did not see any confirmation" | WCAG 3.2.2 | 2 | 3 | 1 | 5 |
| No explicit confirmation when removing task | P2 notes | P2: "I saw that it was removed, but nothing else." | WCAG 3.2.2 | 2 | 3 | 1 | 5 |
| P2 exceeded expected times significantly | P2 notes, metrics.csv | Task 2 - expected <10 seconds, took 18, Task 3 - expected <10 seconds, took 18 | WCAG 3.2.2 | 2 | 3 | 1 | 5 |

**Priority formula**: (Impact + Inclusion) - Effort

**Top 3 priorities for redesign**:
1. [Finding #3 - Priority score 5]
2. [Finding #2 - Priority score 5]
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

**Before** ([file path:line number]):
```kotlin
// ❌ Problem code
[Paste your original code here]
```

**After** ([file path:line number]):
```kotlin
// ✅ Fixed code
[Paste your improved code here]
```

**What changed**: I added a confirmation which appears below the search bar whenever something is deleted.

**Why**: [1 sentence - which WCAG criterion or usability issue this fixes]

**Impact**: [1-2 sentences - how this improves UX, who benefits]

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
| K1 | 2.1.1 All actions keyboard accessible | A | [pass/fail] | [e.g., "Tested Tab/Enter on all buttons"] |
| K2 | 2.4.7 Focus visible | AA | [pass/fail] | [e.g., "2px blue outline on all interactive elements"] |
| K3 | No keyboard traps | A | [pass/fail] | [e.g., "Can Tab through filter, edit, delete without traps"] |
| K4 | Logical tab order | A | [pass/fail] | [e.g., "Top to bottom, left to right"] |
| K5 | Skip links present | AA | [pass/fail/n/a] | [e.g., "Skip to main content works"] |
| **Forms (3)** | | | | |
| F1 | 3.3.2 Labels present | A | [pass/fail] | [e.g., "All inputs have <label> or aria-label"] |
| F2 | 3.3.1 Errors identified | A | [pass/fail] | [e.g., "Errors have role=alert (FIXED in Fix #1)"] |
| F3 | 4.1.2 Name/role/value | A | [pass/fail] | [e.g., "All form controls have accessible names"] |
| **Dynamic (3)** | | | | |
| D1 | 4.1.3 Status messages | AA | [pass/fail] | [e.g., "Status div has role=status"] |
| D2 | Live regions work | AA | [pass/fail] | [e.g., "Tested with NVDA, announces 'Task added'"] |
| D3 | Focus management | A | [pass/fail] | [e.g., "Focus moves to error summary after submit"] |
| **No-JS (3)** | | | | |
| N1 | Full feature parity | — | [pass/fail] | [e.g., "All CRUD ops work without JS"] |
| N2 | POST-Redirect-GET | — | [pass/fail] | [e.g., "No double-submit on refresh"] |
| N3 | Errors visible | A | [pass/fail] | [e.g., "Error summary shown in no-JS mode"] |
| **Visual (3)** | | | | |
| V1 | 1.4.3 Contrast minimum | AA | [pass/fail] | [e.g., "All text 7.1:1 (AAA) via CCA"] |
| V2 | 1.4.4 Resize text | AA | [pass/fail] | [e.g., "200% zoom, no content loss"] |
| V3 | 1.4.11 Non-text contrast | AA | [pass/fail] | [e.g., "Focus indicator 4.5:1"] |
| **Semantic (3)** | | | | |
| S1 | 1.3.1 Headings hierarchy | A | [pass/fail] | [e.g., "h1 → h2 → h3, no skips"] |
| S2 | 2.4.1 Bypass blocks | A | [pass/fail] | [e.g., "<main> landmark, <nav> for filter"] |
| S3 | 1.1.1 Alt text | A | [pass/fail] | [e.g., "No images in interface OR all have alt"] |

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
| before-sr-error.png | Error message without role="alert" | Finding #1 - SR errors not announced |
| after-sr-error.png | Error message WITH role="alert" added | Fix #1 verification |
| regression-axe-report.png | axe DevTools showing 0 violations | Verification Part A |
| [your-screenshot-3.png] | [Description] | [Which finding/fix this supports] |

**PII check**:
- [ ] All screenshots cropped to show only relevant UI
- [ ] Browser bookmarks/tabs not visible
- [ ] Participant names/emails blurred or not visible

---

### Pilot Notes

**Instructions**: Attach pilot notes as separate files (P1-notes.md, P2-notes.md, etc.). Summarize key observations here.

**P1** ([ Variant - e.g., "Standard mouse + HTMX"]):
- **Key observation 1**: [Quote + timestamp - e.g., "Struggled with filter button (09:47)"]
- **Key observation 2**: [Quote + timestamp]

**P2** ([Variant]):
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
- [ ] metrics.csv (or pasted into Section 3)
- [ ] Pilot notes (P1-notes.md, P2-notes.md, etc. OR summarised in Section 6)
- [ ] Screenshots folder (all images referenced above)
- [ ] Privacy statement signed (top of document)

**Evidence chains**:
- [ ] findings-table.csv links to metrics.csv lines AND/OR pilot notes timestamps
- [ ] implementation-diffs.md references findings from table
- [ ] verification.csv Part B shows before/after for fixes

**Quality**:
- [ ] No PII in screenshots (checked twice!)
- [ ] Session IDs anonymous (P1_xxxx format, not real names)
- [ ] Honest reporting (limitations acknowledged if metrics didn't improve)
- [ ] WCAG criteria cited specifically (e.g., "3.3.1" not just "accessibility")

**Pass criteria met**:
- [ ] n=2+ participants (metrics.csv has 2+ session IDs)
- [ ] 3+ findings with evidence (findings-table.csv complete)
- [ ] 1-3 fixes implemented (implementation-diffs.md shows code)
- [ ] Regression complete (verification.csv has 20 checks)
- [ ] Before/after shown (verification.csv Part B has data)

---

**Ready to submit?** Upload this file + evidence folder to Gradescope by end of Week 10.

**Estimated completion time**: 12-15 hours across Weeks 9-10

**Good luck!** 🎯
