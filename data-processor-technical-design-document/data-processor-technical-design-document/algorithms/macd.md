# 🫥 MACD

The Moving Average Covnergence Divergence (MACD) algorithm calculates the MACD values for a given set of price data. It then normalizes these histogram values.

### Formulae:

#### MACD line

$$
MACD=EMA12​−EMA26
$$

**Signal Line**:

$$
Signal Line=EMA9​(MACD)
$$

**MACD Histogram**:

$$
Histogram=MACD−Signal Line
$$
