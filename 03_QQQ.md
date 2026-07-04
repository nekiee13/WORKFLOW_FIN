#### Indicators for QQQ (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |     736.4000 |
| Classic Pivot Point   |     717.9433 |
| 50-day MA             |     709.5574 |
| 200-day MA            |     635.4534 |
| RSI (14)              |      56.4507 |
| Stochastic %K         |      58.4929 |
| ATR (14)              |      16.0314 |
| ADX (14)              |      19.0335 |
| CCI (14)              |      46.4974 |
| Williams %R           |     -17.9385 |
| Ultimate Oscillator   |      51.7456 |
| ROC (10)              |       0.8961 |
| BullBear Power        |      14.2393 |

#### Pivot Points for QQQ (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    | 679.123 | 698.533 | 711.307 | 717.943 | 730.717 | 737.353 | 756.763 |
| Fibonacci  | 698.533 | 705.948 | 710.529 | 717.943 | 725.358 | 729.939 | 737.353 |
| Camarilla  | 718.742 | 720.522 | 722.301 | 717.943 | 725.859 | 727.639 | 729.418 |
| Woodie's   |      - | 700.112 | 714.465 | 719.522 | 733.875 | 738.933 |      - |
| DeMark's   |      - |      - | 704.920 | 714.750 | 724.330 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.0000 -> Significant (GARCH is appropriate)

#### QQQ Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   | 704.2620 | 716.3800 | 728.4980 |
| DYNAMIX |        - | 762.1192 <br> 733.9866 |        - |
| ARIMAX  | 733.8550 | 741.2448 | 748.6346 |
| PCE     | 738.9384 | 743.2999 | 747.6615 |
| LSTM    | 702.3277 | 743.9993 | 784.7731 |
| GARCH   |        - | 746.0798 |        - |
| VAR     |        - | 740.6886 |        - |
| RW      |        - | 739.0515 |        - |
| ETS     |        - | 738.4090 |        - |

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
| Time:             | 23:56:15           |
| R-squared:        | 0.012              |
| Adj. R-squared:   | 0.006              |
| Log-Likelihood:   | -471.934           |
| AIC:              | 955.867            |
| BIC:              | 978.364            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |    coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|--------:|----------:|-------:|-----------:|:-----------------------|
| Const    | -0.1875 |   0.229   | -0.819 |      0.413 | [ -0.636,  0.261]      |
| Close[1] | -0.0416 |   0.05634 | -0.739 |      0.46  | [ -0.152,6.878e-02]    |
| x0       |  0.0383 |   0.02839 |  1.35  |      0.177 | [-1.731e-02,9.397e-02] |

**Volatility Model**
|          |   coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.      |
|:---------|-------:|----------:|-------:|-----------:|:----------------------|
| omega    | 0.0482 |   0.04469 |  1.078 |  0.281     | [-3.943e-02,  0.136]  |
| alpha[1] | 0.0468 |   0.02173 |  2.156 |  0.03108   | [4.261e-03,8.943e-02] |
| beta[1]  | 0.9145 |   0.04843 | 18.883 |  1.576e-79 | [  0.820,  1.009]     |

**Covariance estimator: robust**

#### QQQ GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 2.3643   |
| 2026-07-02 | 2.3253   |
| 2026-07-03 | 2.2837   |