#### Indicators for AAPL (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |     289.3600 |
| Classic Pivot Point   |     283.3200 |
| 50-day MA             |     293.5994 |
| 200-day MA            |     271.3074 |
| RSI (14)              |      46.5541 |
| Stochastic %K         |      39.1001 |
| ATR (14)              |       8.1607 |
| ADX (14)              |      25.6260 |
| CCI (14)              |     -68.9901 |
| Williams %R           |     -45.5529 |
| Ultimate Oscillator   |      35.3537 |
| ROC (10)              |      -3.3017 |
| BullBear Power        |     -10.9607 |

#### Pivot Points for AAPL (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    | 266.280 | 274.800 | 278.270 | 283.320 | 286.790 | 291.840 | 300.360 |
| Fibonacci  | 274.800 | 278.055 | 280.065 | 283.320 | 286.575 | 288.585 | 291.840 |
| Camarilla  | 279.397 | 280.178 | 280.959 | 283.320 | 282.521 | 283.302 | 284.083 |
| Woodie's   |      - | 274.120 | 276.910 | 282.640 | 285.430 | 291.160 |      - |
| DeMark's   |      - |      - | 280.795 | 284.582 | 289.315 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.9731 -> Not Significant

#### AAPL Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   | 268.5899 | 275.1500 | 281.7101 |
| DYNAMIX |        - | 275.0734 <br> 284.7093 |        - |
| ARIMAX  | 285.2338 | 289.1491 | 293.0645 |
| PCE     | 286.8891 | 289.2402 | 291.5913 |
| LSTM    | 273.3651 | 292.4093 | 312.9412 |
| GARCH   |        - | 292.6374 |        - |
| VAR     |        - | 295.7030 |        - |
| RW      |        - | 290.1907 |        - |
| ETS     |        - | 290.1907 |        - |

* ARIMAX Model Selected: p,d,q = (1, 1, 1) with configured exogenous regressors.

#### GARCH Model Summary:

**AR-X - GARCH Model Results**
| **Parameter**     | **Value**          |
|:------------------|:-------------------|
| Dep. Variable:    | Close              |
| Mean Model:       | AR-X               |
| Vol Model:        | GARCH              |
| Distribution:     | Normal             |
| Method:           | Maximum Likelihood |
|                   |                    |
| Date:             | Tue, Jun 30 2026   |
| Time:             | 23:58:30           |
| R-squared:        | 0.007              |
| Adj. R-squared:   | 0.001              |
| Log-Likelihood:   | -568.340           |
| AIC:              | 1148.68            |
| BIC:              | 1171.18            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |    coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.     |
|:---------|--------:|----------:|-------:|-----------:|:---------------------|
| Const    | -0.2068 |   0.479   | -0.432 |      0.666 | [ -1.145,  0.732]    |
| Close[1] |  0.0827 |   0.06496 |  1.273 |      0.203 | [-4.464e-02,  0.210] |
| x0       |  0.061  |   0.09335 |  0.653 |      0.514 | [ -0.122,  0.244]    |

**Volatility Model**
|          |   coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.     |
|:---------|-------:|----------:|-------:|-----------:|:---------------------|
| omega    | 0.1474 |   0.11    |  1.342 |  0.18      | [-6.788e-02,  0.363] |
| alpha[1] | 0.0333 |   0.03429 |  0.971 |  0.332     | [-3.391e-02,  0.101] |
| beta[1]  | 0.8998 |   0.05051 | 17.815 |  5.441e-71 | [  0.801,  0.999]    |

**Covariance estimator: robust**

#### AAPL GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 3.3753   |
| 2026-07-02 | 3.3200   |
| 2026-07-03 | 3.2464   |