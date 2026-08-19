# Safety, scope, and deployment boundary

RxRescue is a **medication-access coordination prototype**. Its intended job is to help people understand why a prescribed medication is stalled and organize the next administrative or communication step.

It is not a substitute for a clinician, pharmacist, payer, or emergency service.

## In scope

- collect the patient's report of an access problem;
- clarify missing administrative facts;
- distinguish common barrier categories without pretending uncertainty is resolved;
- retrieve and summarize curated access-program information;
- organize role-specific next actions; and
- prepare a concise clinic handoff.

## Out of scope

- diagnosis, triage, or treatment planning;
- recommending a new medication or autonomous substitution;
- advising a patient to start, stop, split, or change a medication;
- determining that a payer must cover a medication;
- guaranteeing pharmacy inventory, price, coverage, approval, or assistance eligibility;
- completing a prior authorization without clinician review and appropriate source data; or
- handling an emergency instead of directing the person to appropriate human care.

## Output discipline

Safe access guidance should keep five categories distinct:

1. **Patient report** — what the person says happened.
2. **Verified fact** — what a cited or authoritative source establishes.
3. **Inference** — the system's current interpretation of the barrier.
4. **Unknown** — a fact that still needs confirmation.
5. **Next action** — a bounded step assigned to a patient, clinic, pharmacy, or payer.

The system should not turn an inference into a fact or turn a conditional program term into a promise.

## Prototype privacy posture

The hackathon version uses de-identified or synthetic scenarios and stores session content only in process memory. It does not include production identity, authorization, data-retention, or health-system integration infrastructure.

“No PHI persisted” describes the demo architecture; it is not a certification and does not make the prototype suitable for real patient data.

## Before any clinical deployment

A production release would require, at minimum:

- a formal clinical-risk assessment and defined human oversight;
- security architecture, threat modeling, access controls, and incident response;
- HIPAA and applicable state-law analysis, including vendor agreements where required;
- validated source governance and update/expiration controls;
- documented evaluation thresholds and failure-mode testing;
- logging and auditability without unnecessary sensitive-data retention;
- usability and human-factors testing with patients and clinic staff; and
- clear ownership of escalations, corrections, and adverse events.

## Reporting a concern

Please open a GitHub issue for a documentation error, unsafe product assumption, missing failure mode, or relevant evidence source. Do not include personal health information in issues.

[Back to README](../README.md)
