# SWIFT - The Global Messaging System

SWIFT (Society for Worldwide Interbank Financial Telecommunication) is one of the most
used payment systems. It Can support multiple CSMs (Clearing and Settlement Mechanisms)
including domestic payment clearing, pan-European SEPA frameworks like EBA (Europe Banking Association)
and EACHA (European automated clearing house association) and IPF (International Payment Framework).

The current message protocols used are ISO 15022 (Jan 2021 MT) and 
it's migrating to ISO 20022 (2021 to 2025) still work in progress.

## Prominent Payment Networks that use SWIFT messages

The most prominent networks that use SWIFT messages are the following:

### SEPA - Single Euro Payments Area 
SEPA is the Pan-European network enables standardized real time payment processing in EURO (EUR)

### RITS - Reserve Bank Information and Transfer System
RITS is Australia's high value settlement system which is used to by banks and other approved
institutions to settle their payment obligations in real-time gross settlement (RTGS) basis.

### HDFC RemitNow - Housing Development Finance Corporation

HDFC is India's network for processing payments using the SWIFT protocol

## How SWIFT works

SWIFT assigns each financial organization a unique code that has either 8 characters or 11 characters.
The code is interchangeably called the Bank Identifier Code (BIC), or the SWIFT code, or SWIFT ID.

Example: SOGEPLPWXX

- First 4 characters: The institute code for Société Générale = SOGE
- Next 2 characters: The country code = PL for the country of Poland
- Next 2 characters: The location city code = PW for the city of Warsaw
- Last 3 characters: (Optional), organisations use it to assign codes to individual branches  