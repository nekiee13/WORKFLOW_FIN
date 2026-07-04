#### Indicators for TNX (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |       4.4180 |
| Classic Pivot Point   |       4.3830 |
| 50-day MA             |       4.4564 |
| 200-day MA            |       4.2322 |
| RSI (14)              |      46.0190 |
| Stochastic %K         |      12.8497 |
| ATR (14)              |       0.0537 |
| ADX (14)              |      15.0258 |
| CCI (14)              |     -64.5855 |
| Williams %R           |     -70.5881 |
| Ultimate Oscillator   |      45.0113 |
| ROC (10)              |      -0.2258 |
| BullBear Power        |      -0.0515 |

#### Pivot Points for TNX (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    |  4.297 |  4.340 |  4.356 |  4.383 |  4.399 |  4.426 |  4.469 |
| Fibonacci  |  4.340 |  4.356 |  4.367 |  4.383 |  4.399 |  4.410 |  4.426 |
| Camarilla  |  4.360 |  4.364 |  4.368 |  4.383 |  4.376 |  4.380 |  4.384 |
| Woodie's   |      - |  4.347 |  4.370 |  4.390 |  4.413 |  4.433 |      - |
| DeMark's   |      - |      - |  4.348 |  4.379 |  4.391 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.6056 -> Not Significant

#### TNX Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   |   4.3118 |   4.3920 |   4.4722 |
| DYNAMIX |        - | 4.3949 <br> 4.3783 |        - |
| ARIMAX  |   4.3535 |   4.3873 |   4.4210 |
| PCE     |   4.3686 |   4.3954 |   4.4222 |
| LSTM    |   4.2538 |   4.4175 |   4.5841 |
| GARCH   |        - |   4.4164 |        - |
| VAR     |        - |   4.4160 |        - |
| RW      |        - |   4.4189 |        - |
| ETS     |        - |   4.4152 |        - |

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
| Time:             | 23:57:49           |
| R-squared:        | 0.005              |
| Adj. R-squared:   | -0.001             |
| Log-Likelihood:   | -435.037           |
| AIC:              | 882.075            |
| BIC:              | 904.571            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |       coef |   std err |        t |   P>abs(t) | 95.0% Conf. Int.    |
|:---------|-----------:|----------:|---------:|-----------:|:--------------------|
| Const    |  0.0082399 |   0.233   |  0.03531 |    0.972   | [ -0.449,  0.466]   |
| Close[1] | -0.0846    |   0.04906 | -1.724   |    0.08472 | [ -0.181,1.158e-02] |
| x0       |  0.133     |   4.02    |  0.0331  |    0.974   | [ -7.745,  8.011]   |

**Volatility Model**
|          |   coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|-------:|----------:|-------:|-----------:|:-----------------------|
| omega    | 0.0138 |  0.008865 |  1.562 |      0.118 | [-3.532e-03,3.122e-02] |
| alpha[1] | 0      |  0.01805  |  0     |      1     | [-3.537e-02,3.537e-02] |
| beta[1]  | 0.9831 |  0.02529  | 38.875 |      0     | [  0.934,  1.033]      |

**Covariance estimator: robust**

#### TNX GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 0.8212   |
| 2026-07-02 | 0.8270   |
| 2026-07-03 | 0.8270   |