# E3.3 — FinLedger CI Workflow Evidence

**Evidence type:** Independently checkable GitHub Actions configuration and historical run.  
**Relevant A1 goal:** Foundational Skills in Software Development Tools.  
**Verification boundary:** Demonstrates a recorded **build/verification outcome**, not achievement of all 45 planned learning hours, custom-action development, production deployment, comprehensive test coverage or independent mastery.

## Verified source artefacts

- [FinLedger GitHub Actions workflow (`ci.yml`)](https://github.com/wwdaas/finledger/blob/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3/.github/workflows/ci.yml)
- [Successful GitHub Actions run #33718660359](https://github.com/wwdaas/finledger/actions/runs/33718660359)
- [Associated commit](https://github.com/wwdaas/finledger/commit/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3)

**Recorded date:** **3 September 2026**.  
**Observed run outcome:** `completed / success`.

### What the recorded workflow executes

1. Trigger on a push to `main` or a pull request.
2. Check out repository source.
3. Set up Java 17 on an Ubuntu runner.
4. Run Maven verification via `./mvnw --batch-mode verify`.
5. Build a Docker image tagged `finledger:ci`.

GitHub's run/job record shows the Maven verification and Docker build steps completed successfully on this recorded run.

## Why this matters

The order is meaningful: verification occurs **before** packaging, helping stop the pipeline when checks fail. Maven Wrapper promotes consistency of build invocation. Docker packages the application into an image, but an image build does not demonstrate that an application was deployed, secured or operated in production.

## What this evidence does not show

- Completion of the **Software Development Tools** Canvas module.
- A custom GitHub Action created by the student.
- A completed independent code review or GitHub Projects automation.
- That the September run occurred during an independently documented A1 learning session.
- Complete test coverage or production reliability.

## Next learning evidence to collect

Document a real issue → feature branch → commit → pull request → CI → review workflow, including a failure or design decision, and record actual learning time with dates. If this activity has not happened, it remains a future goal.

## Cross-reference

- [Goal 3 overview](README.md)
- [Evidence register](../Evidence/README.md)
- Draft A3 report: *Professional Learning Report*, §4, p. 4 (5 November 2026).
