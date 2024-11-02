# 🤹 Puell

The Puell algorithm calculates the Puell multiple for Bitcoin. It then normalizes these histogram values.

### Formulae:

#### Daily issuance:

$$
\text{Daily Bitcoin Issuance} = \text{Block Reward} \times 144
$$

#### Daily issuance in USD:

$$
\text{Daily Revenue in USD} = (\text{BTC Daily Issuance}) \times (\text{Current Price in USD})
$$



365 Moving average of USD issuance:

$$
\text{365-Day Moving Average of Daily Issuance in USD} = \frac{1}{365} \sum_{i=1}^{365} \text{Daily Issuance in USD}_i
$$



#### Puell Multiple:

$$
\text{Puell Multiple} = \frac{\text{Daily Issuance in USD}}{\text{365-Day Moving Average of Daily Issuance in USD}}
$$
