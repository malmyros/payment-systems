# Confirmation of Payee (CoP)

## What is Confirmation of Payee?

**Confirmation of Payee (CoP)** is a payment security service designed to reduce fraud and errors 
by verifying that the name of the intended payment recipient (beneficiary) matches the name on the account number provided.

CoP helps prevent:

- Payments sent to the wrong account due to incorrect account details.
- Fraudulent payments where the payee’s details have been altered or spoofed.

---

## Why is Confirmation of Payee Important?

- **Fraud prevention:** Protects customers from scams such as Authorized Push Payment (APP) fraud.
- **Error reduction:** Minimizes payment rejections and delays caused by incorrect beneficiary details.
- **Regulatory compliance:** Increasingly mandated by payment regulators in many countries (e.g., UK’s Payment Systems Regulator).
- **Customer trust:** Builds confidence in digital and online payment services.

---

## How Confirmation of Payee Works

1. **Initiation:** When a payer enters payment details, the payment system queries the CoP service.
2. **Verification:** The CoP service checks the account number and sort code (or equivalent) against the registered payee name.
3. **Response:** The system returns a match status, commonly one of:
    - **Exact Match:** The name matches the account details exactly.
    - **Partial Match:** The name matches partially (e.g., minor spelling differences).
    - **No Match:** The name does not match the account details.
    - **Account Not Found:** The account details do not exist or cannot be verified.
4. **Decision:** Based on the match status, the payment system can:
    - Proceed with payment.
    - Warn the user to verify details.
    - Block or hold the payment for review.

---

## Key Components of Confirmation of Payee

- **Name Matching Algorithms:** Techniques to compare the payee name entered against the registered name, handling variations, case differences, and common misspellings.
- **Data Sources:** Verified databases of account numbers and associated payee names, typically provided by banks or payment schemes.
- **APIs and Integration:** Interfaces to query CoP services in real-time during payment initiation.
- **User Interface:** Clear prompts and warnings to users when discrepancies occur.

---

## Implementation Considerations for Software Engineers

- Integrate CoP checks early in the payment flow (e.g., during beneficiary entry).
- Handle API latency and errors gracefully to avoid blocking payments unnecessarily.
- Design flexible matching thresholds to balance fraud prevention with user convenience.
- Log all CoP requests and results for audit and compliance purposes.
- Ensure data privacy and security when handling beneficiary name and account data.

---

## Example CoP Response Schema (JSON)

```json
{
  "accountNumber": "12345678",
  "sortCode": "12-34-56",
  "submittedName": "John Doe",
  "verifiedName": "John Doe",
  "matchStatus": "Exact Match",
  "confidenceScore": 98
}
