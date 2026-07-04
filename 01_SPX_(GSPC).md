#### Indicators for GSPC (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |   7,499.3599 |
| Classic Pivot Point   |   7,411.2100 |
| 50-day MA             |   7,394.8964 |
| 200-day MA            |   6,948.4215 |
| RSI (14)              |      55.9397 |
| Stochastic %K         |      55.5898 |
| ATR (14)              |      93.2125 |
| ADX (14)              |      21.6411 |
| CCI (14)              |      48.7195 |
| Williams %R           |     -24.5048 |
| Ultimate Oscillator   |      49.3576 |
| ROC (10)              |      -0.1596 |
| BullBear Power        |      82.1753 |

#### Pivot Points for GSPC (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    | 7220.330 | 7315.770 | 7378.100 | 7411.210 | 7473.540 | 7506.650 | 7602.090 |
| Fibonacci  | 7315.770 | 7352.228 | 7374.752 | 7411.210 | 7447.668 | 7470.192 | 7506.650 |
| Camarilla  | 7414.184 | 7422.933 | 7431.682 | 7411.210 | 7449.179 | 7457.927 | 7466.676 |
| Woodie's   |      - | 7323.495 | 7393.550 | 7418.935 | 7488.990 | 7514.375 |      - |
| DeMark's   |      - |      - | 7346.935 | 7395.627 | 7442.375 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.2053 -> Not Significant

#### GSPC Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   | 7257.1227 | 7357.4902 | 7457.8578 |
| DYNAMIX |        - | 7623.7280 <br> 7449.8701 |        - |
| ARIMAX  | 7472.7592 | 7526.3679 | 7579.9766 |
| PCE     | 7510.5608 | 7542.5882 | 7574.6155 |
| LSTM    | 7268.8069 | 7540.7507 | 7790.3577 |
| GARCH   |        - | 7546.3885 |        - |
| VAR     |        - | 7481.7317 |        - |
| RW      |        - | 7519.3859 |        - |
| ETS     |        - | 7516.8843 |        - |

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
| Time:             | 23:54:38           |
| R-squared:        | 0.019              |
| Adj. R-squared:   | 0.013              |
| Log-Likelihood:   | -370.265           |
| AIC:              | 752.531            |
| BIC:              | 775.027            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |       coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|-----------:|----------:|-------:|-----------:|:-----------------------|
| Const    | -0.2025    |  0.168    | -1.203 |    0.229   | [ -0.533,  0.128]      |
| Close[1] | -0.0621    |  0.05631  | -1.103 |    0.27    | [ -0.172,4.823e-02]    |
| x0       |  0.0042797 |  0.002385 |  1.795 |    0.07273 | [-3.945e-04,8.954e-03] |

**Volatility Model**
|          |   coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|-------:|----------:|-------:|-----------:|:-----------------------|
| omega    | 0.0389 |   0.0228  |  1.707 |  0.08787   | [-5.773e-03,8.361e-02] |
| alpha[1] | 0.0275 |   0.02604 |  1.056 |  0.291     | [-2.354e-02,7.854e-02] |
| beta[1]  | 0.9061 |   0.04358 | 20.792 |  5.118e-96 | [  0.821,  0.992]      |

**Covariance estimator: robust**

#### GSPC GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 0.6582   |
| 2026-07-02 | 0.6560   |
| 2026-07-03 | 0.6515   |