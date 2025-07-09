# Kpattern Symbol Reference

This document serves as the symbol reference manual for the Kpattern chart structure markup language, defining all trend symbols (L, S) and K-line structure symbols (K) as well as their combinations, applicable to AI feature recognition, trading strategy descriptions, and structural annotations.

---

## Trend Symbols

Used to describe long-term (L) and short-term (S) trend directions.

| Symbol  | Meaning              | Example                         |
|---------|----------------------|--------------------------------|
| L↗     | Long-term bullish trend | MA200 rising                   |
| L↘     | Long-term bearish trend | MA200 falling                  |
| L↗↘    | Long-term trend turning from bullish to bearish | Reversal downward             |
| L↘↗    | Long-term trend turning from bearish to bullish | Reversal upward               |
| L→     | Long-term consolidation | MA200 sideways movement        |
| L↕     | Long-term high volatility | Wide range consolidation       |
| L↗⤫    | Long-term bullish trend broken | Broken below MA200 but not reversed |
| L↘⤫    | Long-term bearish trend broken | Broken above MA200 but not confirmed |

> Short-term trends are represented by S with the same semantics, for example: `S↗` indicates short-term rise, `S→` indicates short-term consolidation.

---

## K-line Structure Symbols (K)

Describe price action structures.

### 📈 Bullish Types

| Symbol | Meaning     | Description                  |
|--------|-------------|------------------------------|
| ↗      | Slow rise  | With pullbacks and consolidations, low slope |
| ↑      | Fast rise  | Reduced pullbacks, stronger bullish candles  |
| ⇑      | Sprint surge | Large bullish candle, increased ATR/volume  |
| ↑↑     | Extreme short squeeze | Consecutive large bullish candles, no pullbacks |

### 📉 Bearish Types

| Symbol | Meaning     | Description                  |
|--------|-------------|------------------------------|
| ↘      | Slow decline | With rebounds and consolidations |
| ↓      | Fast decline | Reduced rebounds, enlarged bearish candles |
| ⇓      | Sprint drop | Panic large bearish candle, volume expansion |
| ↓↓     | Extreme decline | Consecutive large bearish candles, no rebounds |

### 🔁 Reversal and Consolidation Types

| Symbol | Meaning       | Description                   |
|--------|---------------|------------------------------|
| →      | Sideways consolidation | Narrow range movement        |
| ↕      | High volatility | Long upper and lower shadows, high volatility |
| ↘↗     | Bottom structure | Decline followed by rebound, establishing support |
| ↗↘     | Top structure | Rise followed by decline, potential top formation |

### 🧲 Support / Resistance Tests

| Symbol   | Meaning           | Example Combination | Description                          |
|----------|-------------------|---------------------|------------------------------------|
| ⊥        | Support retest    | L⊥↗                | Price retests long-term support then rises |
| ⊤        | Resistance pullback | S⊤↘                | Short-term resistance pullback fails then falls |
| ⊥↗       | Confirmed support rebound |                     | Price retests support, confirms, and rebounds |
| ⊤↘       | Confirmed resistance drop |                     | Breakout failure, confirmed resistance then continues down |

---

## Combination Structure Examples

| Expression         | Explanation                                      |
|--------------------|-------------------------------------------------|
| L↗ S↘ K⊥↕          | Long-term bullish, short-term bearish, price retests support and consolidates |
| L→ S↗ K↑           | Long-term consolidation, short-term bullish, price rises quickly              |
| L↘ S↗ K⊤↘          | Long-term bearish, short-term rebound, resistance pullback fails then falls    |
| L↗ S↗ K↑↑          | Strong bullish trend, continuous advance, extreme short squeeze structure     |
| L↗⤫ S↘ K⊥↕        | Bullish trend broken, short-term bearish, price consolidates near support     |

---

## Suggested Uses

- AI K-line chart recognition and structural annotation
- Trading strategy structure definition and trigger conditions
- Multi-timeframe trend and behavior joint analysis

---

> This document is part of the Kpattern project. Community contributions and suggestions for new structure symbols are welcome.
