# Verification of Payee (VoP)

## What is Verification of Payee?

**Verification of Payee (VoP)** is a service used to confirm that the payee details 
provided by a payer correspond to the correct and valid bank account before initiating a payment. 
It helps reduce payment errors and fraud by validating that the beneficiary exists and that the account information is accurate.

---

## Why is Verification of Payee Important?

- **Error reduction:** Minimizes failed or misdirected payments caused by incorrect beneficiary details.
- **Fraud prevention:** Helps prevent fraudulent transactions by verifying payee legitimacy.
- **Improved customer experience:** Reduces delays and increases confidence in electronic payments.
- **Regulatory compliance:** Supports adherence to payment industry standards and regulations.

---

## How Verification of Payee Works

1. **Input:** The payer enters beneficiary details such as account number, sort code (or equivalent), and payee name.
2. **Query:** The payment system queries the VoP service with these details.
3. **Check:** The VoP system checks the validity of the account and the match between the submitted payee name and the registered name.
4. **Response:** The service returns a verification status, which may include:
    - **Valid Account and Name Match**
    - **Valid Account but Name Mismatch**
    - **Account Not Found**
5. **Action:** Based on the response, the payment system may allow the payment, request confirmation from the payer, or block the payment.

---

## Key Components of VoP

- **Account Verification:** Confirms the account number and bank details exist and are active.
- **Name Verification:** Compares the submitted payee name against the registered name using matching algorithms.
- **API Integration:** Enables real-time or batch verification through secure interfaces.
- **User Feedback:** Provides clear status messages or warnings to users during payment initiation.

---

## Implementation Considerations

- Implement VoP checks early in the payment process to catch errors upfront.
- Ensure fallback logic if the VoP service is unavailable (e.g., allow payment with warnings).
- Balance strictness of name matching with user convenience to avoid unnecessary payment blocks.
- Log verification attempts and results for compliance and troubleshooting.
- Securely handle sensitive payee data according to data protection regulations.

---

## Example VoP API Response (JSON)

```json
{
  "accountNumber": "87654321",
  "sortCode": "65-43-21",
  "submittedName": "Alice Smith",
  "verifiedName": "Alice Smith",
  "verificationStatus": "Valid Account and Name Match",
  "confidenceScore": 95
}
