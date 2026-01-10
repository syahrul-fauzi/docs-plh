# User Acceptance Testing (UAT) Plan

**Project:** Lawyers Hub  
**Version:** 1.0.0  
**Phase:** Staging Verification

## 1. Objectives
*   Validate end-to-end workflows for Case Management and Document Drafting.
*   Confirm "Demo Mode" functionality for stakeholder review without real auth credentials.
*   Verify collaborative editing performance under simulated conditions.

## 2. Test Cases

### TC-001: Case Management (Happy Path)
*   **Description**: Create, view, and list cases.
*   **Pre-conditions**: Staging environment accessible.
*   **Steps**:
    1. Navigate to `/dashboard`.
    2. Click "New Case".
    3. Fill details (Title: "UAT Case 1", Client: "Acme Corp").
    4. Save.
*   **Expected Result**: Case appears in the list. Details page loads.

### TC-002: Collaborative Drafting (Core Feature)
*   **Description**: Verify real-time editor loading and interaction.
*   **Steps**:
    1. Open "UAT Case 1".
    2. Navigate to "Documents" tab.
    3. Open "Draft 1".
    4. Type text "Hello World".
*   **Expected Result**: Text appears. No "Connection Error" banner.

### TC-003: Performance Benchmark
*   **Description**: Page load time check.
*   **Steps**:
    1. Refresh Dashboard.
    2. Measure load time (Subjective).
*   **Expected Result**: Dashboard loads in < 2 seconds.

## 3. Bug Reporting Template

**Title**: [Category] Short description of issue  
**Severity**: (Critical / High / Medium / Low)  
**Environment**: Staging (v1.0.0)  

**Steps to Reproduce**:
1. Go to '...'
2. Click on '...'
3. See error...

**Expected Behavior**:
[What should happen]

**Actual Behavior**:
[What actually happened]

**Screenshots/Logs**:
[Paste here]

## 4. Sign-off Criteria
*   [ ] No Critical/High severity bugs open.
*   [ ] All Happy Path test cases passed.
*   [ ] Performance meets SLA (<2s load time).
*   [ ] Stakeholder approval received from:
    *   Product Owner: __________________
    *   QA Lead: __________________
