# Personas

> Three personas drive the Patient Consent Service. Each story in [user-stories](./03-user-stories/) should map back to one of them.

## 👩‍⚕️ The Clinician (primary user)

- ED Consultant at Hospital A, 12 years experience.
- Comfortable with the EHR, frustrated by anything that adds clicks.
- Sees 30+ patients per shift; consent capture must take **under a minute**.
- Trusts the system if the audit trail is visible.

**Top needs:** speed, no duplicate data entry, clear "who else can see this".

## 🧑‍🦳 The Patient

- 72-year-old with chronic conditions.
- Limited digital literacy; consent is verbal and witnessed by the Clinician.
- Wants to know what they're agreeing to and how to withdraw later.

**Top needs:** plain-English summary, easy withdrawal path, confidence.

## 🧑‍💼 The Data Custodian

- Runs cohort extracts for approved research projects.
- Currently spends hours reconciling consent status against extract requests.
- Accountable to the Ethics Committee for any misuse.

**Top needs:** authoritative "is this patient consented right now?" API, withdrawal events pushed in near-real-time.
