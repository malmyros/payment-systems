# Card Transactions Documentation

## 1. Card Transactions Overview

This section provides an overview of the main types of card transaction flows commonly implemented in fintech systems.
It helps engineers understand how transactions progress through different stages, from authorization to settlement,
including associated advices, reversals, and incremental authorizations.

The main categories covered are:

- **Authorizations**: Requests to approve or decline card usage.
- **Authorization Advices**: Confirmations or additional info on authorizations.
- **Incremental Authorizations**: Modifications to original authorizations, such as tips.
- **Reversals and Reversal Advices**: Undoing or adjusting prior transactions.
- **Settlements**: Finalizing transactions for clearing and funding.

---

## 2. Authorizations

### Approved Authorizations

| Scenario                           | Description                                       |
|------------------------------------|---------------------------------------------------|
| Zero transaction amount            | Authorization with zero amount (balance inquiry). |
| Low risk score transaction         | Authorization for low-risk flagged transactions.  |
| Mag stripe ATM withdrawal          | ATM withdrawal using mag stripe card.             |
| Chip ATM withdrawal                | ATM withdrawal using chip card.                   |
| Contactless ATM withdrawal         | ATM withdrawal using contactless method.          |
| Mag stripe balance inquiry         | Balance inquiry using mag stripe card.            |
| Mag stripe purchase authorization  | Purchase using mag stripe card.                   |
| Chip purchase authorization        | Purchase using chip card.                         |
| Contactless purchase authorization | Purchase using contactless payment.               |
| MOTO without CVV2                  | Mail or telephone order without CVV2 code.        |
| MOTO with CVV2                     | Mail or telephone order with CVV2 code.           |
| MOTO with address verification     | MOTO with AVS (address verification).             |
| E-commerce with CVV2               | Online purchase with CVV2 verification.           |
| Chip manual transaction            | Manual chip card transaction.                     |
| Installment payment                | Payment made in installments.                     |
| Recurring payment                  | Automatic recurring payment.                      |
| Google Pay authorization           | Authorization via Google Pay wallet.              |
| Apple Pay authorization            | Authorization via Apple Pay wallet.               |
| Samsung Pay authorization          | Authorization via Samsung Pay wallet.             |

### Declined Authorizations

| Scenario                          | Description                               |
|-----------------------------------|-------------------------------------------|
| Do not honour transaction         | Generic issuer decline.                   |
| Insufficient funds                | Cardholder lacks sufficient balance.      |
| Invalid PIN                       | Incorrect PIN entered.                    |
| System error                      | Processing or network error.              |
| No payment authorization response | Missing authorization response.           |
| Card not found                    | Card number unrecognized.                 |
| Already processed authorization   | Authorization already handled.            |
| High risk score                   | Transaction flagged as high risk.         |
| 3DS soft decline                  | Soft decline in 3D Secure authentication. |
| Card PIN blocked                  | Decline due to blocked PIN.               |
| ATM daily limit exceeded          | Decline for exceeding withdrawal limit.   |
| High risk merchant category code  | Decline due to merchant category risk.    |
| Suspended account                 | Decline because account is suspended.     |

---

## 3. Authorization Advices

### Approved Authorization Advices

| Scenario                                            | Description                                     |
|-----------------------------------------------------|-------------------------------------------------|
| Approved advice transaction                         | Confirms approval of a transaction.             |
| Approved advice for approved authorization          | Advice for an already approved authorization.   |
| Approved advice for already approved advice         | Repeat advice for a previously approved advice. |
| Approved advice with different authorization amount | Advice with changed authorization amount.       |
| Approved advice with same authorization amount      | Advice matching original authorization amount.  |
| ATM PIN change advice                               | Advice related to ATM PIN changes.              |

### Declined Authorization Advices

| Scenario                                   | Description                                             |
|--------------------------------------------|---------------------------------------------------------|
| Declined advice                            | Advice indicating a decline after authorization.        |
| Soft declined advice                       | Non-final decline advice, allowing retry.               |
| Card PIN blocked decline advice            | Decline advice due to blocked PIN.                      |
| Approved advice for declined authorization | Advice sent despite declined authorization (edge case). |
| Visa declined advice                       | Decline advice from Visa network.                       |
| Visa declined advice for inactive card     | Decline advice when card is inactive.                   |

---

## 4. Incremental Authorizations

### Approved Incremental Authorizations

| Scenario                                     | Description                                   |
|----------------------------------------------|-----------------------------------------------|
| Incremental authorization                    | Increase in authorization amount (e.g., tip). |
| Partially reversed incremental authorization | Partial reversal of increment.                |

### Declined Incremental Authorizations

| Scenario                                         | Description                                      |
|--------------------------------------------------|--------------------------------------------------|
| Insufficient funds for incremental authorization | Declined due to insufficient funds on increment. |

---

## 5. Reversals and Reversal Advices

### Reversal Advices

| Scenario                                     | Description                                |
|----------------------------------------------|--------------------------------------------|
| Fully reversed advice transaction            | Full reversal advice confirmation.         |
| Partially reversed advice transaction        | Partial reversal advice confirmation.      |
| Reversal advice with no existing transaction | Reversal advice without matching original. |
| Fully reversed advice transaction repeat     | Repeated full reversal advice.             |
| Reversed advice transaction repeat           | Repeated reversal advice.                  |
| ADM PIN changed reversed advice              | PIN change reversal advice.                |

### Reversals

| Scenario                          | Description                     |
|-----------------------------------|---------------------------------|
| Fully reversed transaction        | Entire transaction reversed.    |
| Partially reversed transaction    | Transaction partially reversed. |
| Refund reversed transaction       | Refund reversed.                |
| Fully reversed same currency      | Full reversal in same currency. |
| Fully reversed transaction repeat | Repeated full reversal.         |

---

## 6. Settlements

| Scenario                                               | Description                                 |
|--------------------------------------------------------|---------------------------------------------|
| Approved transaction                                   | Successful settlement of a transaction.     |
| Declined transaction                                   | Failed settlement.                          |
| Offline clearing transaction                           | Offline (batch) clearing.                   |
| Offline clearing for card not found                    | Offline clearing when card is missing.      |
| Reverse partially cleared transaction                  | Partial reversal after clearing.            |
| Reverse fully cleared transaction                      | Full reversal after clearing.               |
| Offline reversed clearing when clearing does not exist | Offline reversal without original clearing. |
| Incremental authorization clearing                     | Clearing incremental authorization.         |
| Multiple refunds transaction                           | Multiple refunds in settlement.             |
| Approved transaction followed by partial reversal      | Approved transaction with partial reversal. |
| Refund followed by clearing of approved transaction    | Refund cleared after approval.              |
| Fully reversed payment failed to be cleared            | Failed clearing on full reversal.           |
| ATM cash withdrawal refund                             | Refund for ATM withdrawal.                  |
| Multiple reversed transactions                         | Multiple reversals in one settlement.       |
| Second presentment                                     | Re-presenting a transaction for settlement. |
| Settlement reversal request                            | Request to reverse settlement.              |
| Duplicate settlement reversal                          | Duplicate request to reverse settlement.    |

---
