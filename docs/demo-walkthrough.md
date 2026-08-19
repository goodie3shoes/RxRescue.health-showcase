# Demo walkthrough

This walkthrough describes the de-identified scenario used to demonstrate the RxRescue hackathon prototype. It is product documentation, not a clinical recommendation.

## Scenario

A patient has a severe migraine lasting several days and is seen through video urgent care. A clinician sends a prescription for Nurtec ODT. At the pharmacy, the patient is told:

- the claim returned **Reject 75: prior authorization required**;
- the prescription cannot be processed through insurance yet; and
- the cash price is roughly **$150 per tablet**.

The patient has insurance through work but does not know whether the medication is covered, whether the prescriber submitted a prior authorization, or whether the pharmacy participates in a manufacturer savings program.

All people, organizations, and transactional details in the demo are de-identified or synthetic.

## 1. Patient intake

RxRescue starts with the patient's account of what happened and asks only for facts that change the access route, such as:

- the exact pharmacy rejection or message;
- whether the plan is commercial or government-sponsored;
- whether the clinic has already submitted a prior authorization;
- whether the payer says the medication is covered, non-formulary, or excluded;
- whether the pharmacy has the medication in stock; and
- whether the patient needs an urgent clinical reassessment.

The interaction is designed to avoid making the patient translate payer language into a diagnosis of the problem.

## 2. Barrier clarification

The prototype distinguishes between several commonly conflated states:

| State | Why it matters |
|---|---|
| Prior authorization pending | The clinic or payer needs a defined administrative action |
| Coverage exclusion | A prior authorization may not solve the problem |
| Pharmacy processing issue | The claim may need to be retried or corrected |
| Stock-out | Coverage may be fine, but dispensing cannot occur at that location |
| Affordability barrier | The prescription is technically available but financially inaccessible |
| Missing information | A safe route cannot yet be selected |

The system keeps unknowns visible instead of silently filling them with model assumptions.

## 3. Evidence-grounded cost rescue

For the demonstration medication, assistance-program facts are supplied from a curated evidence record rather than left to general model recall. The workflow treats eligibility as conditional and prompts verification of details that can change the answer, including plan type, coverage status, program exclusions, pharmacy participation, and expiration dates.

The prototype does not promise a price or guarantee eligibility.

## 4. Patient action plan

The patient receives a short sequence of concrete, role-specific actions. In this scenario, that can include confirming whether the clinic submitted the prior authorization, asking the payer whether the drug is covered or excluded, and asking the pharmacy whether it can process an eligible bridge or savings pathway.

The exact route depends on the facts gathered in the conversation.

## 5. Clinic handoff

The clinic view converts the conversation into an actionable summary:

- prescribed medication and reported rejection;
- known insurance and pharmacy details;
- access barrier currently suspected;
- facts still requiring verification;
- recommended administrative follow-ups; and
- any urgency or clinical-escalation signal.

This is meant to reduce repeated storytelling and help the clinic act without re-reading a long transcript.

## 6. Auditability

The intended audit view separates:

- **patient-reported facts**;
- **retrieved evidence**;
- **system inferences**;
- **unresolved questions**; and
- **recommended next actions**.

That separation is central to the product thesis: useful clinical AI must make uncertainty and provenance legible, not merely sound confident.

[Back to README](../README.md)
