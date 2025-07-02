# SWIFT - The Global Messaging System

SWIFT (Society for Worldwide Interbank Financial Telecommunication) is one of the most
used payment systems. It Can support multiple CSMs (Clearing and Settlement Mechanisms)
including domestic payment clearing, pan-European SEPA frameworks like EBA (Europe Banking Association)
and EACHA (European automated clearing house association) and IPF (International Payment Framework).

The current message protocols used are ISO 15022 (Jan 2021 MT) and 
it's migrating to ISO 20022 (2021 to 2025) still work in progress.

## Prominent Payment Networks that use SWIFT messages

The most prominent networks that use SWIFT messages are the following:

### Global Payment Systems Using SWIFT or SWIFT-Based Messaging

| **System**        | **Country/Region** | **Description**                                                                                      |
|-------------------|--------------------|----------------------------------------------------------------------------------------------------|
| **SEPA**          | Eurozone (Europe)  | Single Euro Payments Area enables standardized, mostly real-time payments in EUR across Europe.    |
| **RITS**          | Australia          | Reserve Bank Information and Transfer System is Australia’s RTGS for high-value payment settlement.|
| **HDFC RemitNow** | India              | HDFC’s remittance network built on SWIFT messaging for international money transfers.              |
| **Fedwire**       | United States      | Fedwire Funds Service is the Fed’s RTGS system, uses SWIFT messaging standards for communication.  |
| **CHAPS**         | United Kingdom     | High-value payment system for RTGS settlements, integrates with SWIFT for international transfers. |
| **TARGET2**       | Eurozone           | ECB’s real-time gross settlement system for euro payments across the EU, heavily SWIFT-enabled.    |
| **LVTS**          | Canada             | Large Value Transfer System; uses SWIFT messaging for secure communication in RTGS payments.       |
| **SIC**           | Switzerland        | Swiss Interbank Clearing system for RTGS transactions; uses SWIFT standards for messaging.         |
| **CNAPS**         | China              | China National Advanced Payment System; uses domestic protocols but SWIFT often for international. |
| **S.W.I.F.T.**    | Global             | The core messaging network connecting thousands of financial institutions worldwide.               |
| **TCH**           | India              | The Clearing House system facilitating payments using SWIFT infrastructure.                        |


## How SWIFT works

SWIFT assigns each financial organization a unique code that has either 8 characters or 11 characters.
The code is interchangeably called the Bank Identifier Code (BIC), or the SWIFT code, or SWIFT ID.

Example: SOGEPLPWXX

- First 4 characters: The institute code for Société Générale = SOGE
- Next 2 characters: The country code = PL for the country of Poland
- Next 2 characters: The location city code = PW for the city of Warsaw
- Last 3 characters: (Optional), organisations use it to assign codes to individual branches  