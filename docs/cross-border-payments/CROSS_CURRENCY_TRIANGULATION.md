# Cross-Currency Triangulation

## What is Cross-Currency Triangulation?

Cross-currency triangulation is a method to calculate the exchange rate between two currencies that don’t have a direct quoted rate by using a third “base” or “pivot” currency.

**Example:**  
You want the rate between EUR and GBP, but you only have EUR/USD and GBP/USD rates. Using USD as the pivot, you calculate:  

```
EUR/USD = 1.1
GBP/USD = 1.3

EUR/GBP = (EUR/USD) ÷ (GBP/USD) = 1.1 ÷ 1.3 ≈ 0.846
```

## Why Use Triangulation?

- Not all currency pairs have direct market quotes.
- Triangulation allows you to compute implied rates based on available pairs.
- Helps maintain consistency and detect arbitrage opportunities.

## Additional Notes

- In real fintech apps, rates constantly update, so you'd pull live rates from an FX provider.
- You may want to support more complex triangulation with multiple pivots or fallback logic.
- Be mindful of rounding and precision, especially with money.
- Always handle cases where no direct or triangulated rate is available gracefully.