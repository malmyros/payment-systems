# Beneficiaries

## What is a Beneficiary?

A **beneficiary** is the recipient of funds in a payment or foreign exchange transaction. 
Whether the transaction involves sending money internationally (cross-border) or converting 
currencies domestically or internationally (FX), the beneficiary is the party who ultimately receives the funds.

---

## Importance of Beneficiary Information

Accurate and complete beneficiary details are critical because:

- They ensure funds reach the correct recipient without delays or errors.
- They help comply with regulatory and compliance requirements, such as anti-money laundering (AML) and sanctions screening.
- They minimize the risk of payment rejection or returns caused by incorrect or incomplete data.
- They enable proper tracking, reconciliation, and auditing of transactions.

---

## Key Beneficiary Data Fields in Cross-Border and FX Payments

| Field                     | Description                                                | Examples                             |
|---------------------------|------------------------------------------------------------|------------------------------------|
| Beneficiary Name           | Full legal name of the recipient                           | "John Doe"                         |
| Beneficiary Address        | Physical or registered address                             | "123 Main St, London, UK"          |
| Beneficiary Account Number | Recipient's bank account number or IBAN                   | "GB29NWBK60161331926819"            |
| Bank Identifier Code (BIC) / SWIFT Code | Unique identifier for the beneficiary’s bank       | "NWBKGB2L"                        |
| Currency                   | Currency of the beneficiary’s account                      | "GBP"                             |
| Beneficiary Bank Name      | Name of the bank where the beneficiary holds the account | "NatWest Bank"                    |
| Purpose of Payment         | Reason or description of the payment (often mandatory)    | "Invoice payment"                  |

---

## Roles of Beneficiaries in Payment Flows

1. **End Beneficiary:** The final recipient of funds, whether domestic or international.
2. **Intermediary Beneficiary:** Sometimes funds pass through intermediary parties or banks before reaching the end beneficiary.
3. **Third-Party Beneficiary:** Occasionally, a party receives funds on behalf of the ultimate beneficiary; this requires enhanced compliance scrutiny.

---

## How Beneficiary Data Affects Payment and FX Processing

- **Validation:** Input data such as IBAN and SWIFT codes must be validated to prevent errors.
- **Compliance:** Beneficiary details are screened against sanction lists and AML watchlists.
- **Routing:** Beneficiary bank information determines the payment route and any intermediaries involved.
- **Currency Considerations:** Currency of the beneficiary’s account informs whether FX conversion is required.
- **Fee Calculation:** Certain beneficiary banks or currencies may involve additional fees.
- **Notifications:** Contact info related to the beneficiary may be used for payment status updates.

---

## Common Challenges with Beneficiary Data

- Mismatched or incomplete beneficiary information leads to failed or delayed payments.
- Varying international standards for bank account numbers and identifiers complicate validation.
- Name mismatches can cause compliance flags and delays.
- Privacy regulations require secure handling of beneficiary data.

---

## Best Practices for Managing Beneficiary Information

- Use international standards like **ISO 20022** for data formats.
- Implement strict validation rules and provide user-friendly error messages.
- Encrypt beneficiary data both at rest and in transit.
- Maintain detailed logs of data access and changes for auditing.
- Regularly update validation and compliance rules.
- Guide users clearly on how to enter beneficiary data.

---

## Example: Beneficiary Data JSON Schema

```json
{
  "beneficiaryName": "John Doe",
  "beneficiaryAddress": "123 Main St, London, UK",
  "beneficiaryAccountNumber": "GB29NWBK60161331926819",
  "beneficiaryBankBIC": "NWBKGB2L",
  "currency": "GBP",
  "beneficiaryBankName": "NatWest Bank",
  "purposeOfPayment": "Invoice payment"
}
