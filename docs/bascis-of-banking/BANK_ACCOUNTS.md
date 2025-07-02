# Bank Accounts

## What is a Bank Account?

A **bank account** is a financial account maintained by a banking institution for an individual or entity, allowing
deposits, withdrawals, and other financial transactions.
In fintech, bank accounts are essential as they represent the destination or source of funds for payments, collections,
and money management.

---

## Types of Bank Accounts

| Account Type                     | Description                                                                                              | Typical Use Cases                                   |
|----------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Current Account**              | Used for day-to-day transactions, with unlimited deposits and withdrawals. Usually supports overdrafts.  | Salary payments, bill payments, merchant operations |
| **Savings Account**              | Intended for saving money, often with interest, and limited withdrawals.                                 | Personal savings, emergency funds                   |
| **Fixed Deposit / Term Account** | Locked-in funds for a fixed term with guaranteed interest.                                               | Investment, long-term savings                       |
| **Foreign Currency Account**     | Holds funds in foreign currencies. Useful for FX and international transactions.                         | Businesses operating in multiple currencies         |
| **Escrow Account**               | Held by a third party to manage funds temporarily during transactions.                                   | Property sales, complex settlements                 |
| **Virtual / E-Money Account**    | Digital representation of funds held in an EMI or fintech wallet. Not always a traditional bank account. | Wallet balances, prepaid accounts                   |

---

## Bank Account Identifiers

To uniquely identify and route payments, bank accounts use standardized identifiers, which vary by country:

| Identifier         | Description                                           | Example                  |
|--------------------|-------------------------------------------------------|--------------------------|
| **Account Number** | Customer’s unique bank account number                 | `12345678`               |
| **Sort Code**      | Bank branch identifier used in the UK                 | `12-34-56`               |
| **IBAN**           | International Bank Account Number — global standard   | `GB29NWBK60161331926819` |
| **SWIFT/BIC**      | Bank Identifier Code used for international transfers | `NWBKGB2L`               |
| **Routing Number** | Used in the US to identify banks                      | `021000021`              |
| **CLABE**          | Standardized bank code used in Mexico                 | `012345678901234567`     |

---

## Bank Account Attributes

| Attribute           | Description                                         | Example                     |
|---------------------|-----------------------------------------------------|-----------------------------|
| Account Holder Name | Name of the individual or entity owning the account | "Jane Smith"                |
| Account Type        | Type of account (current, savings, etc.)            | "Current"                   |
| Currency            | Currency of the account                             | "USD", "EUR", "GBP"         |
| Bank Name           | Name of the bank where the account is held          | "Bank of America"           |
| Branch Address      | Physical address of the bank branch                 | "100 Main St, New York, NY" |
| Account Status      | Active, dormant, closed                             | "Active"                    |
| Overdraft Facility  | Whether overdrafts are allowed                      | "Enabled"                   |

---

## Role of Bank Accounts in Fintech Architecture

- **Source & Destination of Funds:** Bank accounts are endpoints for incoming and outgoing payments.
- **Customer Identity Link:** Connects customer profiles to their financial assets.
- **Compliance & KYC:** Account details are used in verification and AML checks.
- **Settlement:** Enables reconciliation of transactions and settlements with banks.
- **Multi-Currency Handling:** Accounts in multiple currencies allow seamless FX operations.

---

## Bank Account Lifecycle

1. **Creation:** Account details are collected or linked (e.g., via account aggregation APIs or direct input).
2. **Verification:** Account ownership and validity are confirmed (e.g., micro-deposits, account verification services).
3. **Use:** Account is used for payment initiation, collection, or balance management.
4. **Monitoring:** Transactions and balances are monitored for fraud and compliance.
5. **Closure:** Account is deactivated or delinked when no longer used.

---

## Common Operations with Bank Accounts

| Operation            | Description                                     |
|----------------------|-------------------------------------------------|
| Account Linking      | Connecting a bank account to a fintech profile. |
| Account Verification | Confirming account ownership and validity.      |
| Balance Inquiry      | Checking current available funds.               |
| Transaction History  | Retrieving past transactions.                   |
| Payment Initiation   | Sending money from the account.                 |
| Direct Debit Setup   | Authorizing recurring payments.                 |
| Account Update       | Modifying account details (address, contact).   |

---

## Example Bank Account JSON Model

```json
{
  "accountHolderName": "Jane Smith",
  "accountNumber": "12345678",
  "iban": "GB29NWBK60161331926819",
  "swiftBic": "NWBKGB2L",
  "bankName": "NatWest Bank",
  "branchAddress": "250 Bishopsgate, London, UK",
  "accountType": "Current",
  "currency": "GBP",
  "accountStatus": "Active",
  "overdraftFacility": true
}
