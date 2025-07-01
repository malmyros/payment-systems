# Types of Payment Transactions

There are many different types of transactions when it comes to payments.
We can try to segregate them in the following categories to understand
what kind of systems are involved.

## Based on value, (#)  Number of messages & processing SLA

### High Value Payments
- Large Amount
- Single Message
- E.g RTGS (Real time gross settlement)

### Mass Payments
- File Based Processing
- Bulk Messages
- E.g NEFT (National Electronic Funds Transfer system)

### Real Time Payments
-  Instant / Immediate processing
- Single Message
- E.g IMPS (Immediate Payment Service), UPI (India's Unified Payment Interface)

## Based on Purpose of message, Credit, Debit

### Credit Transfer
- One entity sending payment credit to another

### Direct Debit
- Biller sending a request to Debit account based on a standing order

### Request to Pay
- Request from an e-Commerce site and approving via APP/OTP

## Based on Payment Direction

### Outward Payments
- Initiated from Sending Bank and Sent Out to Clearing / SWIFT

### Inward Payments
- Received from Clearing / SWIFT and Beneficiary is the Receiving bank's customer

### Onward Payments
- Received from Clearing / SWIFT and Sent Out to another bank. 
(The beneficiary is not the Receiving bank's customer)

### Booked Payments
- Both Debtor and Creditor are the Bank's customers.
(There is no outbound message Sent Out)

## Based on Customer Types

### Corporate Payments
- Big corporates or companies

### Retail / Consumer Payments
- Individuals

## Based on Processing Time

### Batch Based Payments
- Payment initiation happens in groups, and typically takes 2-3 days for settlement to complete
- Method: Net Settlement Method
- Use cases for batch payments include: Direct Debits, Payroll, Billdesk payments
- Examples of processors: NEFT, ECS (India), TCH (US), BACS (UK)
- Common modes of payment: Credit Cards, Debit Cards, Internet Banking, Cheques
- Coverage: Domestic (Account holders within the same country)
- Typical Usage: High Volume / Low Value

### Near Real Time
- Payments initiated and settled within the same day (or within a few hours).
- Method: Gross Settlement Method
- Use cases for `near` real time payments include: Wallet Payments, Wire Transfers
- Example of processors: RTGS, IMPS (India), CHIPS, FedWire (US), CHAPS (UK), TARGET2 (Europe)
- Common modes of payment: Mobile Wallets, Wire Transfers
- Coverage: Domestic, International
- Typical Usage: High Volume / Low Value, Low Volume / High Value  

### Real Time
- Payments initiated and settled instantaneously
- Use cases for real time payments include: B2B Transfers, P2P Transfers, RTP
- Example of processors: UPI (India), TCHRTP, FedNow *(US), FasterPayments (UK), SEPA (Europe)
- Common modes of payment: Mobile Banking
- Coverage: Domestic, International
- Typical Usage: High Volume / Low Value, Low Volume / High Value