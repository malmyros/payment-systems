# Card Processors

A **card processor** is a critical part of the card issuing infrastructure.
It acts as the **transaction and lifecycle orchestration layer** between:

- The **card issuer**
- The **card network** (e.g. Visa or Mastercard)
- Other external systems (e.g. fraud engines, KYC providers, core banking)

Processors are responsible for:

- Real-time **transaction authorization**
- **Message routing** between issuer and network
- **Card lifecycle management** (activation, PIN, reissue, etc.)
- Handling **settlement files and clearing**
- Supporting **disputes and chargebacks**

---

## Global & Scalable Card Processors

These processors support multiple regions and are suitable for scaling across borders and product types.

| Processor           | Network Support      | Description                                                                | Recommended For                          |
|---------------------|----------------------|----------------------------------------------------------------------------|------------------------------------------|
| **Paymentology**    | Visa & Mastercard    | Cloud-native processor with real-time decisioning and advanced rule logic. | Multi-country issuing, modern banking    |
| **Marqeta**         | Primarily Mastercard | API-first platform popular among fintechs; strong in US and Europe.        | Fintechs, corporate cards, expense tools |
| **i2c**             | Visa & Mastercard    | Highly configurable platform used by Apple Card and others.                | Credit products, global fintechs         |
| **GPS (Thredd)**    | Visa & Mastercard    | Powers Revolut, Curve, and other major fintechs in EU/Asia.                | Prepaid/debit fintechs in EMEA/APAC      |
| **FIS**             | Visa & Mastercard    | Enterprise-grade processor with global reach and credit/debit support.     | Banks, large FIs, credit card programs   |
| **TSYS**            | Visa & Mastercard    | Established US-based processor; strong credit card capabilities.           | Credit issuing, US banks                 |
| **PowerCard (HPS)** | Primarily Visa       | Modular issuing/acquiring platform used by large issuers and banks.        | Enterprise-grade deployments, global FX  |

---

## Region-Specific Card Processors

These are strong within specific geographies and may offer services like BIN sponsorship, local compliance, or faster
time-to-market.

| Processor         | Network Support      | Description                                                            | Recommended For                           |
|-------------------|----------------------|------------------------------------------------------------------------|-------------------------------------------|
| **PPS (Edenred)** | Primarily Mastercard | UK/EU-based processor with BIN sponsorship and issuing infrastructure. | European fintechs, prepaid cards          |
| **Enfuce**        | Visa & Mastercard    | ESG-compliant processor offering fast issuing and compliance tooling.  | Nordic and EU fintechs, e-money providers |
| **Viva Wallet**   | Visa & Mastercard    | EU-acquirer/issuer with broad geographic reach.                        | Merchant-focused card programs in EU      |
| **Railsr**        | Mastercard           | Formerly Railsbank; EU-focused issuing and sponsoring platform.        | Early-stage fintechs, embedded finance    |
| **Nium**          | Visa & Mastercard    | Strong in cross-border FX and payout flows, with global reach.         | FX-heavy card programs, APAC expansion    |
| **Fincra**        | Visa & Mastercard    | African infrastructure platform supporting issuing and payouts.        | African fintechs and wallets              |

---

## Choosing a Card Processor

When evaluating a processor, consider the following:

- **Network compatibility** (Visa, Mastercard, both)
- **Geographic coverage** and regulatory compliance
- **Integration model** (modern API vs legacy file-based)
- Support for:
    - Real-time **authorization logic**
    - **Spend controls** and card profiles
    - **Tokenization** (e.g. Apple Pay, Google Pay)
    - **Multi-currency** and FX handling
- **BIN control and sponsorship**
- **Cost and scalability**

