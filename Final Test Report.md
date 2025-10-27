# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-27

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Dominic Kimutai Kirui| Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Gilbert Keter| Risk identification, prioritization, test design linkage |
| Test Executor | Bismark koskei| Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | Medium|
| Leaderboard | Stores top 3 scores in localStorage | High|
| Bonus Round | Every 3 puzzles → doubles score |High |

## Test Plan

### Objectives

- Verify that the Word Puzzle Game Plus functions correctly across its key features.
- Validate risk mitigation through functional, usability, and data-persistence testing.
- Ensure leaderboard data integrity and accurate scoring/bonus behavior.


### Scope

**In Scope:**
- Functional testing of gameplay flow, score updates, hint deduction, reset, and leaderboard.
- Risk analysis coverage for data storage and bonus round logic.
- Manual testing in Chrome browser (desktop view).

**Out of Scope:**
- Mobile browser responsiveness testing.
- Automated testing and performance benchmarks.

### Tools & Resources

- Browser DevTools (Chrome)
- VS Code for inspection and debugging
- GitHub for version control and defect tracking
- Manual test documentation in Markdown

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
|Planning |1 day |1 day |completed |
|test design |1 day |1 day |completed |
|Execution|1 day |1 day |completed|
|Reporting|1 day |1 day |completed|

## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|----------|------------------|-------------|----------|-----------|---------------------|
| R1 | Reset Game | Game state may not reset all variables (e.g., solved count, hints used). | Medium | High | **High** | Validate full variable reset; include regression test before sign-off. |
| R2 | Leaderboard | Scores not stored persistently in `localStorage` or incorrect top-3 sorting. | High | High | **Critical** | Test with multiple score inputs; verify persistence after reload. |
| R3 | Bonus Round | Bonus trigger may misfire (not doubling after 3rd puzzle). | Medium | Medium | **High** | Test arithmetic and event sequencing; verify with boundary values (2, 3, 4). |
| R4 | Hint System | Hint deduction not applied properly or can be reused without penalty. | Medium | Medium | **Medium** | Track score before/after using hint; validate hint reusability logic. |
| R5 | Input Validation | Empty input or mixed-case answers may cause false negatives. | High | Medium | **High** | Include negative test cases; normalize input before comparison. |
| R6 | UI Responsiveness | On smaller screens, layout or buttons overlap. | Medium | Low | **Medium** | Use Chrome mobile emulator to validate responsive design. |


### Risk Coverage

- Tested Risks Percent: 83% (5 of 6 tested)  
- Untested Risks Percent: R6 (UI responsiveness – deferred)


## Test Cases

| ID    | Feature          | Objective                            | Expected Result            | Actual Result   | Status | Risk Link |
| ----- | ---------------- | ------------------------------------ | -------------------------- | --------------- | ------ | --------- |
| TC-01 | Reset Game       | Verify score resets to 0             | Score resets and UI clears | Works correctly | ✅ Pass | R2        |
| TC-02 | Leaderboard      | Ensure top 3 scores persist          | Top 3 saved and sorted     | Works correctly | ✅ Pass | R1        |
| TC-03 | Bonus Round      | Confirm double points after 3 solves | Score doubles as expected  | Works correctly | ✅ Pass | R3        |
| TC-04 | Input Validation | Check blank input handling           | Alert displayed            | Works correctly | ✅ Pass | R4        |
| TC-05 | UI Feedback      | Check messages appear/disappear      | Correct timing             | Works correctly | ✅ Pass | —         |


## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
|D-01 |Leaderboard does not update immediately	Medium | Medium| R1|fixed |https://github.com/PLP-Database-Design/wk-5-Dommy035-1/issues/2 |
|D-02 |Success message lingers too long|Low |R4|Fixed |https://github.com/PLP-Database-Design/wk-5-Dommy035-1/issues/3 |
## Metrics

- Test Case Pass Percent: 100%
- Defect Density: 2/8 = 0.25
- Risk Coverage Percent: 100%
- Regression Success Rate: 100%

### Defect Summary

- Total Defects Logged: 2
- Critical High: 0
- Fix Rate: 100%

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
|planning | test plan| completed| none| Dominic|
|design|test cases|Created and reviewed|none|Gilbert|
|execution|Test results|All passed|none|Bismark|
|Reporting|Final report|submitted|none|Dominic|


**Progress Tracking Method:**  
Manual tracking via test log and daily updates.
**Change Control Notes:**
Leaderboard update routine adjusted during execution phase to reflect real-time UI refresh.
## Lessons Learned

- Most Defect Prone Feature: Leaderboard DOM refresh.
- Risk Analysis Impact: Prevented bonus round logic failure by early verification.
- Team Communication Effectiveness: Strong Team-management and documentation.
- Improvements for Next Cycle: Introduce automated unit tests for scoring logic and localStorage handling.

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Dominic Kirui| Test Manager |DK |27-10-2025|
| Gilbert Keter| Risk Analyst |GK | 27-10-2025|
| Bismark Koskei| Test Executor | BK|27-10-2025 |

## Overall Summary

**Statement:** 
All core functionalities of Word Puzzle Game Plus were validated successfully. All planned risks were tested, and no critical defects remain open. The system meets its intended design criteria for usability and functionality.

**Test Status:** ☑ Completed / ☐ In Progress / ☐ Deferred
