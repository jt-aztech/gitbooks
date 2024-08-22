# 🖇️ Moving Average - Average True Range

The Moving Average - Average True Range (MA-ATR) algorithm calculates the moving average (MA) and the average true range (ATR) at a given price point. It then determines the number of ATR multipliers between the moving average and the price at that point. These multipliers are subsequently normalized.

### Formulae:

#### Moving Average (MA):

$$
MA = \frac{\sum_{i=1}^{n} P_i}{n}
$$

where $$Pi$$​ is the price at time $$i$$ and $$n$$ is the period

#### Average True Range (ATR):

If there is no previous average true range then:

$$
ATR = \frac{\sum_{i=1}^{n} TR_i}{n}
$$

Otherwise:

$$
\text{ATR}_{n} = \frac{\text{Previous ATR}_{n-1} + TR}{n}
$$

Where $$TRi$$ (True Range) is the maximum of the following:

$$
TR_i = \max(P_{\text{high}} - P_{\text{low}}, |P_{\text{high}} - P_{\text{close, previous}}|, |P_{\text{low}} - P_{\text{close, previous}}|)
$$



#### ATR Multiplier:

$$
\text{Multiplier} = \frac{|P_{\text{current}} - MA|}{ATR}
$$



