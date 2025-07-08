# Idempotency

Idempotency is a critical principle in software engineering — and in **fintech**, it's absolutely non-negotiable.

**Definition:**  
An operation is _idempotent_ if **performing it multiple times has the same effect as doing it once**.

---

## Why It Matters

In banking and fintech systems, idempotency protects both the **customer** and the **business** from:

- Duplicate payments due to retries
- Network failures or timeouts
- UI glitches (e.g., double-tap of "Transfer" button)
- Inconsistent ledger state

Let’s explore this through two lenses.

---

## Customer's Perspective

Without idempotency, a customer might unintentionally send **more funds than intended**.

**Example:**

```
Customer selects a beneficiary
    -> Customer enters 40 GBP to transfer
        -> Customer selects a transfer reason
            -> Customer presses the Transfer Funds button
```

If this action is **accidentally submitted twice**, and the operation is not idempotent:

- The wallet may be charged **twice** (80 GBP)
- The customer might be **overdrawn**, even if no overdraft is allowed

In real life, this leads to **customer complaints, chargebacks, or even legal exposure**.

---

## Bank's Perspective

From the bank’s backend, a transfer may flow like this:

**Example:**

```
The service receives and consumes an event from Kafka to transfer 40 GBP
    -> The system looks up the beneficiary details for the external provider
        -> The system initiates an external payment from the GBP Wallet Account
```

Now imagine the same event is **processed twice** (e.g., due to retries, timeout, or duplicated messages):

- The customer sees a single 40 GBP debit
- The bank **sends 80 GBP** externally

This discrepancy leads to **financial loss, audit failures, and incident escalations**.

---

## Real Incident: The Post Office Scandal

The Post Office scandal — sometimes called the Horizon scandal — is one of the most serious  
miscarriages of justice in UK legal history. It revolves around the Post Office’s Horizon accounting system,  
developed by Fujitsu, which led to the wrongful prosecution of hundreds of innocent sub-postmasters.

The Horizon system incorrectly reported financial discrepancies, leading to:

- Hundreds of **false fraud accusations**
- **Criminal convictions**, job losses, and even **suicides**
- A public inquiry, overturned convictions, and a national scandal

This case proves how **software bugs in financial systems** can destroy lives.

---

## Best Practices for Idempotency

> **Tip:** To mitigate this risk, there are several strategies we can implement 
> to **sleep better at night**, avoid unnecessary **on-call alerts**, 
> and stay clear of those **dreaded incident review meetings**.

| Technique                                  | Description                                                                                              |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Idempotency-Key Header                     | Client provides a unique, operation-scoped key to ensure single execution                                |
| Store results in database                  | Persist idempotency key, response body, and HTTP status code for auditing and traceability               |
| Cache results in Redis with TTL and jitter | Store idempotency keys in Redis with 24h TTL and random jitter to avoid thundering herd on expiry        |
| Make operations atomic                     | Ensure the entire operation either completes fully or not at all                                         |
| Lock funds temporarily                     | Hold funds before external calls to avoid race conditions or double sends                                |
| Use retries with deduplication             | Enable safe retries by checking stored results for existing idempotency key                              |
| Correlate with external provider           | Tag external payment requests with both customer and internal IDs to trace or recover in case of timeout |


