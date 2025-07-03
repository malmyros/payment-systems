# Card Products

A **Card Product** defines the configuration, rules, and behavior for issuing a class of cards. It acts as a template
that governs card properties like network configuration, card form, lifecycle, and associated business logic.

---

## Creating a Card Product

Each card product must have a **unique name** and include the following attributes:

---

## Required Fields

| Field                     | Description                                                | Example             |
|---------------------------|------------------------------------------------------------|---------------------|
| `product_code`            | Unique short identifier used programmatically              | `travel_us_01`      |
| `name`                    | Human-readable name (must be unique)                       | `Travel Card - USD` |
| `base_currency`           | ISO 4217 currency code                                     | `USD`               |
| `card_image_id`           | ID for the card artwork                                    | `img_travel_001`    |
| `card_processor_id`       | Processor used for card lifecycle and transaction handling | `paymentology`      |
| `card_manufacturer_id`    | Manufacturer of the physical card                          | `tag_systems`       |
| `card_lifetime_months`    | Expiry time in months                                      | `36`                |
| `estimated_delivery_days` | Days for standard card delivery                            | `7`                 |
| `express_delivery_days`   | Days for express delivery                                  | `2`                 |
| `initial_card_status`     | Default status after issuance                              | `active`            |
| `market` / `jurisdiction` | Legal or regulatory region for issuance                    | `US`                |

---

## Card Type Configuration

| Field                           | Description                                  | Example                   |
|---------------------------------|----------------------------------------------|---------------------------|
| `allows_virtual_cards`          | Whether virtual cards can be issued          | `true`                    |
| `allows_physical_cards`         | Whether physical cards can be issued         | `true`                    |
| `convert_virtual_to_physical`   | If virtual cards can be upgraded to physical | `true`                    |
| `initial_card_profile_virtual`  | Profile applied to virtual cards             | `virtual_profile_fx_only` |
| `initial_card_profile_physical` | Profile applied to physical cards            | `physical_profile_full`   |

---

## Card Usage and Behavior

| Field                                | Description                                       | Example |
|--------------------------------------|---------------------------------------------------|---------|
| `enable_contactless_by_default`      | Whether contactless is enabled on card issuance   | `true`  |
| `allow_alternative_delivery_address` | If delivery can be made to a non-billing address  | `true`  |
| `max_virtual_card_replacements`      | Max number of times virtual card can be reissued  | `3`     |
| `max_physical_card_replacements`     | Max number of times physical card can be reissued | `2`     |
| `allow_emboss_name_update`           | If cardholder name can be updated post-issuance   | `false` |
| `emboss_name_max_length`             | Maximum character length for embossed name        | `26`    |

---

## Fees and Charges

| Field                  | Description                               | Example |
|------------------------|-------------------------------------------|---------|
| `first_card_fee`       | Fee for first card issuance               | `0.00`  |
| `reorder_card_fee`     | Fee for reissuing a lost or expired card  | `5.00`  |
| `express_delivery_fee` | Additional cost for express card delivery | `10.00` |
