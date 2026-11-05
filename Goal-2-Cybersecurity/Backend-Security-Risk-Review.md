# E2.3 — Java Backend Security Risk Review

**Evidence type:** Source-based analytical artefact, aligned with the draft A3 report dated **5 November 2026**.  
**Relevant A1 goal:** Foundational Cybersecurity.  
**Verification boundary:** Links support **inspection of existing code**, not completion of the Canvas module, new implementation during A1, penetration testing or independent execution of security tests.

## Scope and evidence

The FinLedger repository at the [inspected commit](https://github.com/wwdaas/finledger/tree/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3) contains:

- [SecurityConfiguration.java](https://github.com/wwdaas/finledger/blob/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3/src/main/java/com/finledger/security/SecurityConfiguration.java) — protected route authentication, stateless JWT resource-server configuration and issuer validation.
- [AccountService.java](https://github.com/wwdaas/finledger/blob/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3/src/main/java/com/finledger/account/service/AccountService.java) — account ownership checks, including `requireOwnedAccount`.
- [SecurityAuthorizationTest.java](https://github.com/wwdaas/finledger/blob/0a34977a70f3f4ae18541ca9b9ee2249a5207cb3/src/test/java/com/finledger/security/SecurityAuthorizationTest.java) — tests defined for missing or malformed bearer tokens and use of the JWT subject.

## Security claims, evidence and limits

| Security concern | Code evidence | What remains unverified |
|---|---|---|
| Unauthenticated requests access protected routes | Authentication rules and negative test cases | Real-path tests for expired tokens and incorrect issuers; deployment configuration |
| A valid user accesses another user's account | Owner check in `requireOwnedAccount` and related methods | Two-user end-to-end API test across relevant routes |
| Availability or data loss | CIA (confidentiality, integrity, availability) framing from the study topic | Load limits, recovery objectives, load test and backup restoration exercise |

**Key distinction:** Authentication verifies identity; authorisation determines whether that identity may act on a particular resource. A test using a mock JWT does not prove the complete token signature-verification path is secure.

## Reflection grounded in the draft report

An appropriate security argument needs a chain from **asset → threat → control → verification**. Source inspection alone identifies possible safeguards and gaps; it is not equivalent to exercising a secure deployment or demonstrating complete risk reduction.

## Recommended next real evidence

If independently performed, record:
- date and environment of a two-user authorisation API test;
- request details with secret values redacted;
- expected and actual status codes;
- any fix, follow-up commit and retest;
- which Canvas learning topic informed the test choice.

**Do not describe these as completed before they occur.**

## Cross-reference

- [Goal 2 overview](README.md)
- [Evidence register](../Evidence/README.md)
- Draft A3 report: *Professional Learning Report*, §3, p. 3 (5 November 2026).
