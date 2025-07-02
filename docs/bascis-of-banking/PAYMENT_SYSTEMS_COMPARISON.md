# Payment Systems Comparison

Bellow we can see payment systems from different countries, how they operate, and what kind
of payments they support.

## Payment Systems in UK

| Description                  | BACS                                         | CHAPS                                   | Faster Payments (FPS)              | ICS (Cheque Clearing)              | Open Banking Payments                     |
|------------------------------|----------------------------------------------|-----------------------------------------|------------------------------------|------------------------------------|-------------------------------------------|
| Full Form                    | Bankers' Automated Clearing Services         | Clearing House Automated Payment System | Faster Payments Service            | Image Clearing System              | Account-to-Account via Open Banking APIs  |
| Stake                        | Public (via Pay.UK)                          | Public (Bank of England)                | Public (via Pay.UK)                | Public (via Pay.UK)                | Hybrid (Private fintechs + public APIs)   |
| Offline Mode                 | Branch submission, Direct Debit setup        | Branch-based for manual requests        | Rare (mostly online)               | Cheque drop-off in branch          | Not supported (API/internet-based only)   |
| Online Mode                  | Online banking platforms, corporate software | Corporate banking portals               | Online/mobile banking, APIs        | Cheque imaging via mobile apps     | Online/mobile apps, merchant integrations |
| Transaction Type             | Batch                                        | Real-time (high value)                  | Real-time (low/med value)          | Batch (overnight clearing)         | Real-time                                 |
| Settlement Type              | Grouped settlement                           | 1-to-1 real-time gross settlement       | 1-to-1 settlement                  | Grouped (batch)                    | 1-to-1 via FPS rails                      |
| Service Timings              | Weekdays only (3-day cycle)                  | Weekdays (6 AM–6 PM)                    | 24/7/365                           | Weekdays only                      | 24/7/365 (depends on underlying bank FPS) |
| Typical Service Types        | Salary, pensions, supplier payments          | Property, large corporate transfers     | P2P, P2B, B2B, recurring           | Personal, business cheque deposits | P2P, P2B, e-commerce, bill payments       |
| Transaction Limits (Min–Max) | Varies / Typically £20M+                     | No lower limit / No upper legal limit   | Bank-dependent / Up to £1M via FPS | NA / £50K+ common via cheque       | Bank-dependent / Often £1M max (FPS cap)  |
| Coverage                     | Domestic only                                | Domestic only                           | Domestic only                      | Domestic only                      | Domestic only (UK bank accounts only)     |

## Payment Systems in US

| Description                   | TCH                                  | FedACH                                                 | CHIPS                                   | FedWire                        | RTP*                   | FedNow (TBL)            |
|-------------------------------|--------------------------------------|--------------------------------------------------------|-----------------------------------------|--------------------------------|------------------------|-------------------------|
| Full Form                     | Clearing System - The Clearing House | Clearing System - The Federal Reserve's Clearing House | Clearing House Interbank Payment System | Federal Reserve's RTGS network | TCH's RTP rail         | NA                      |
| Stake                         | Private                              | Public                                                 | Private                                 | Public                         | Private                | Banks                   |
| Offline Mode                  | Branch, Cheque                       | Branch, Cheque                                         | NA                                      | NA                             | NA                     | NA                      |
| Online Mode                   | Net Banking, Mobile Banking          | Net Banking, Mobile Banking                            | Net Banking, Mobile Banking             | Net Banking, Mobile Banking    | Paypal, Venmo          | NA                      |
| Transaction Type              | Batch                                | Batch                                                  | Near Real Time                          | Near Real Time                 | Batch                  | Near Real Time          |
| Settlement Type               | In Groups                            | In Groups                                              | Aggregate Model                         | 1-1                            | 1-1                    | 1-1                     |
| Service Timings               | Fixed Working Hours                  | Fixed Working Hours                                    | Fixed Working Hours                     | 24*7                           | 24*7                   | 24*7                    |
| Typical Service Types         | P2P, B2B                             | P2P, P2P, P2B, B2B                                     | P2P, P2B, B2B                           | P2P, P2B, RTP                  | P2P, P2B, RTP          | P2P, P2B, RTP           |
| Transaction Limits (MIN, MAX) | NA / 1M USD                          | NA                                                     | NA                                      | NA                             | 100K USD               | 25K USD (Domestic Only) |
| Coverage                      | Domestic, International              | Domestic, International                                | Domestic, International                 | Domestic, International        | Domestic International | Domestic Only           |

### Payment Systems in India

| Description                    | NEFT                               | RTGS                        | IMPS                        | UPI                       | ACS/ECS                                               |
|--------------------------------|------------------------------------|-----------------------------|-----------------------------|---------------------------|-------------------------------------------------------|
| Full Form                      | National Electronic Funds Transfer | Real Time Gross Settlement  | Immediate Payment Service   | Unified Payment Interface | Automated Clearing House / Electronic Clearing System |
| Managed By                     | RBI                                | RBI                         | NPCI                        | NPCI                      | RBI                                                   |
| Offline Mode                   | Branch, Cheque                     | Cheque                      | Net Banking, Mobile Banking | NA                        | NA                                                    |
| Online Mode                    | Net Banking, Mobile Banking        | Net Banking, Mobile Banking | Net Banking, Mobile Banking | Gpay, Paytm, PhonePe      | Visa Payment Instructions                             |
| Transaction Type               | Batch                              | Real Time                   | Real Time                   | Real Time                 | Batch                                                 |
| Settlement Type                | In Groups (hours)                  | 1-1                         | 1-1                         | 1-1                       | In Groups (Few Business Days)                         |
| Service Timings                | Monday to Saturday                 | Monday to Saturday          | 24*7                        | 24*7                      | Monday to Sunday                                      |
| Typical Service Types          | P2P, B2B                           | P2P, P2B, B2B               | P2P, P2B, RTP               | P2P, P2B, RTP             | B2P (Payrolls)                                        |
| Transaction Limits (MIN / MAX) | INR 1 / No Limit                   | INR 2L / No Limit           | INR 1 / INR 2L              | INR 2L                    | NA                                                    |    