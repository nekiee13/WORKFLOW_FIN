#### Indicators for DJI (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |  52,319.1992 |
| Classic Pivot Point   |  52,147.9688 |
| 50-day MA             |  50,494.4132 |
| 200-day MA            |  48,490.8223 |
| RSI (14)              |      65.6678 |
| Stochastic %K         |      80.6204 |
| ATR (14)              |     585.8413 |
| ADX (14)              |      23.9810 |
| CCI (14)              |     125.4699 |
| Williams %R           |     -12.5377 |
| Ultimate Oscillator   |      46.6765 |
| ROC (10)              |       0.6145 |
| BullBear Power        |     952.2932 |

#### Pivot Points for DJI (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    | 51423.789 | 51785.879 | 51984.309 | 52147.969 | 52346.398 | 52510.059 | 52872.148 |
| Fibonacci  | 51785.879 | 51924.197 | 52009.650 | 52147.969 | 52286.287 | 52371.740 | 52510.059 |
| Camarilla  | 52083.164 | 52116.355 | 52149.547 | 52147.969 | 52215.930 | 52249.121 | 52282.313 |
| Woodie's   |      - | 51787.292 | 51987.135 | 52149.382 | 52349.225 | 52511.472 |      - |
| DeMark's   |      - |      - | 52066.139 | 52188.884 | 52428.229 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.0909 -> Not Significant

#### DJI Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   | 51252.0049 | 51920.6211 | 52589.2373 |
| DYNAMIX |        - | 52702.3945 <br> 52633.4727 |        - |
| ARIMAX  | 52177.9747 | 52502.5913 | 52827.2079 |
| PCE     | 52088.4469 | 52311.5594 | 52534.6719 |
| LSTM    | 50787.1340 | 52560.8877 | 54299.5161 |
| GARCH   |        - | 52496.1843 |        - |
| VAR     |        - | 52384.1430 |        - |
| RW      |        - | 52433.0110 |        - |
| ETS     |        - | 52419.6782 |        - |

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
| Time:             | 23:55:33           |
| R-squared:        | 0.011              |
| Adj. R-squared:   | 0.005              |
| Log-Likelihood:   | -367.179           |
| AIC:              | 746.358            |
| BIC:              | 768.854            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |        coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|------------:|----------:|-------:|-----------:|:-----------------------|
| Const    | -0.0603     | 0.192     | -0.314 |    0.754   | [ -0.437,  0.317]      |
| Close[1] | -0.1118     | 0.06154   | -1.817 |    0.06914 | [ -0.232,8.769e-03]    |
| x0       |  0.00030302 | 0.0003844 |  0.788 |    0.43    | [-4.503e-04,1.056e-03] |

**Volatility Model**
|          |   coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.       |
|:---------|-------:|----------:|-------:|-----------:|:-----------------------|
| omega    | 0.0319 |   0.02093 |  1.522 | 0.128      | [-9.165e-03,7.289e-02] |
| alpha[1] | 0.021  |   0.02501 |  0.839 | 0.401      | [-2.803e-02,7.001e-02] |
| beta[1]  | 0.9222 |   0.0334  | 27.61  | 8.331e-168 | [  0.857,  0.988]      |

**Covariance estimator: robust**

#### DJI GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 0.5331   |
| 2026-07-02 | 0.5414   |
| 2026-07-03 | 0.5430   |