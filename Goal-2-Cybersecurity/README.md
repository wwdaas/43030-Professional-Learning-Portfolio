# Goal 2 — Foundational Cybersecurity

**Original A1 learning goal:** Demonstrate foundational skills in Cybersecurity.  
**A1 planned effort:** Approximately 45 hours.  
**A1 baseline:** SFIA Level 1 — Follow (self-assessment in Skills Audit).  
**Current completion status:** Pending verification.

## 1. Why I selected this learning goal

My A1 Skills Audit identified introductory knowledge of authentication, access control, input validation and data privacy, along with some exposure to JWT-based authentication in a Spring Boot project. However, I had not yet completed structured professional learning in cybersecurity. Secure backend development requires more than implementing features: it involves identifying threats, selecting controls and evaluating risks.

## 2. Learning activities planned in A1

| Week | Planned activity | Evidence to collect |
|---|---|---|
| 1 | Study introductory threats, vulnerabilities and security controls; take notes | Dated learning notes |
| 2 | Study authentication, authorisation, access control and secure data handling in the **Introduction to Cybersecurity** module | Module record; topic summary |
| 3 | Complete cybersecurity module activities/assessments and revisit knowledge gaps | Completion record or assessment result |
| 4 | Apply learning to a Java backend scenario: identify risks in authentication, APIs and database access, then document appropriate controls | Security-risk analysis |

The A1 Skills Audit also mentioned a plan to study **OWASP Top 10** and explore role-based access control. Include these only if actually completed.

## Available analytical artefact

- [E2.3: Source-based backend security risk review](Backend-Security-Risk-Review.md) — documented evaluation of existing project code; not proof of real security test execution or course completion.

## Canvas quiz results

- **E2.6:** Cybersecurity Assessment 1 — **18.5/20 (92.5%)**, submitted **7 November 2026 at 17:06**.
- **E2.7:** Cybersecurity Assessment 2 — **18/20 (90%)**, submitted **7 November 2026 at 17:10**.

[View verified score record and evidence scope](Cybersecurity-Quiz-Results.md). Original screenshot images still need uploading to this public repository after privacy review.

## 3. Evidence to add

- [ ] **E2.1** — Introduction to Cybersecurity module record
- [ ] **E2.2** — Dated cybersecurity study notes
- [ ] **E2.3** — Security-risk analysis of a Java application (risks, impact, proposed controls)
- [ ] **E2.4** — Specific relevant code, configuration or testing evidence, if actually performed
- [ ] **E2.5** — Actual time entries in [learning-hours log](../Learning-Log/learning-hours.csv)

See the [evidence register](../Evidence/README.md).

## 4. Optional practical risk-analysis template

| Component | Risk to investigate | Possible mitigation to evaluate | Evidence / outcome |
|---|---|---|---|
| Login and authentication | Weak or missing authentication | Secure authentication and session/token handling | Pending |
| API endpoints | Unauthorised access | Server-side authorisation checks | Pending |
| User input | Unsafe handling of untrusted input | Validation, parameterised queries and safe error handling | Pending |
| Database | Excessive access or exposed credentials | Least privilege and secure secret management | Pending |

This is a **template**, not a claim that the listed risks were found or controls implemented.

## 5. Critical reflection — to complete after verifying activities

What changed between knowing security vocabulary and analysing a concrete application? Which control was difficult to justify or test? What risk remains? How could a security consideration change an architectural decision or the way I communicate with teammates?

## 6. Future development

Choose a specific security skill to strengthen, set a feasible timeline and define verification (such as a documented threat model, reviewed API tests or demonstrated role-based authorisation).
