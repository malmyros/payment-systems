# Payment Transaction Lifecycle

The payment transaction lifecycle is segregated usually in five steps.
The Payment initiation, the Authorization & Validation, the Clearing,
the Settlement, and the Reporting.

### Payment Initiation

The Payee initiates the payment. The Payer may be the `debtor`
in case of a credit transfer or the `beneficiary` in case of a direct debit.
Then the payment instruction is issued to the payer's financial institution.

### Authorization & Validation

The payment is processed at various levels by the involved financial institutions,
central banks, regulators, networks etc. The validations include various checks
depending on the payment method, such checking the account numbers, currencies,
transaction date and eligibility.

### Clearing

At the clearing step the banks transfer the funds between themselves using
the information of the authorized payment.

### Settlement

In settlement the beneficiary's bank account is credited and the payee's
bank account is debited.

### Reporting

The final step involves reporting to the customer via statements (bank statements),
instant messages (push notifications), and the updating of the General Ledger (GL) entries. 