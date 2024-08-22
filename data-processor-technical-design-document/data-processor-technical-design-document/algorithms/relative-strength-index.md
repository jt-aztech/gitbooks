# 💪 Relative Strength Index

The Relative Strength Index (RSI) algorithm calculates the RSI value for a given set of price data. It then normalizes these RSI values.

### Formulae:

#### RSI:

$$
RSI = 100 - \frac{100}{1 + RS}
$$

where $$RS$$ (Relative Strength) is:

$$
RS = \frac{\text{Average Gain}}{\text{Average Loss}}
$$

* **Average Gain:** Average of all gains over the specified period.
* **Average Loss:** Average of all losses over the specified period.
