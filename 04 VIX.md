#### Indicators for VIX (2026-06-30):
| Indicator             | Value        |
|:----------------------|-------------:|
| Current Value         |      16.4500 |
| Classic Pivot Point   |      18.1967 |
| 50-day MA             |      17.6808 |
| 200-day MA            |      18.7203 |
| RSI (14)              |      45.2238 |
| Stochastic %K         |      24.0437 |
| ATR (14)              |       2.0725 |
| ADX (14)              |      22.7581 |
| CCI (14)              |     -68.1472 |
| Williams %R           |     -90.0293 |
| Ultimate Oscillator   |      34.7637 |
| ROC (10)              |       0.2438 |
| BullBear Power        |      -1.5800 |

#### Pivot Points for VIX (2026-06-30):
| Method      | S3    | S2    | S1    | Pivot Points | R1    | R2    | R3    |
|-------------|-------|-------|-------|--------------|-------|-------|-------|
| Classic    | 14.277 | 16.237 | 16.943 | 18.197 | 18.903 | 20.157 | 22.117 |
| Fibonacci  | 16.237 | 16.985 | 17.448 | 18.197 | 18.945 | 19.408 | 20.157 |
| Camarilla  | 17.111 | 17.291 | 17.470 | 18.197 | 17.830 | 18.009 | 18.189 |
| Woodie's   |      - | 16.045 | 16.560 | 18.005 | 18.520 | 19.965 |      - |
| DeMark's   |      - |      - | 17.570 | 18.510 | 19.530 |      - |      - |

ARIMAX Residual ARCH Test (p-value): 0.1099 -> Not Significant

#### VIX Forecasting results (Day 3):
| Model   | Lower CI | Forecast | Upper CI |
|:--------|:--------:|:--------:|:--------:|
| Torch   |  15.2961 |  18.8900 |  22.4839 |
| DYNAMIX |        - | 14.6670 <br> 17.1147 |        - |
| ARIMAX  |  15.1616 |  16.3254 |  17.4892 |
| PCE     |  16.1458 |  17.0273 |  17.9088 |
| LSTM    |  13.3172 |  15.8752 |  19.9151 |
| GARCH   |        - |  16.7825 |        - |
| VAR     |        - |  16.7645 |        - |
| RW      |        - |  16.3198 |        - |
| ETS     |        - |  16.5739 |        - |

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
| Time:             | 23:57:00           |
| R-squared:        | 0.038              |
| Adj. R-squared:   | 0.032              |
| Log-Likelihood:   | -1071.45           |
| AIC:              | 2154.91            |
| BIC:              | 2177.41            |
| No. Observations: | 314                |
| Df Residuals:     | 311                |
| Df Model:         | 3                  |

**Mean Model**
|          |    coef |   std err |      t |   P>abs(t) | 95.0% Conf. Int.     |
|:---------|--------:|----------:|-------:|-----------:|:---------------------|
| Const    |  1.987  |   0.909   |  2.185 |    0.02885 | [  0.205,  3.769]    |
| Close[1] | -0.1304 |   0.08112 | -1.607 |    0.108   | [ -0.289,2.861e-02]  |
| x0       | -0.7699 |   0.357   | -2.154 |    0.03121 | [ -1.470,-6.947e-02] |

**Volatility Model**
|          |    coef |   std err |     t |   P>abs(t) | 95.0% Conf. Int.     |
|:---------|--------:|----------:|------:|-----------:|:---------------------|
| omega    | 18.4943 |  10.174   | 1.818 |  0.0691    | [ -1.447, 38.435]    |
| alpha[1] |  0.0521 |   0.05835 | 0.893 |  0.372     | [-6.226e-02,  0.166] |
| beta[1]  |  0.6082 |   0.167   | 3.647 |  0.0002655 | [  0.281,  0.935]    |

**Covariance estimator: robust**

#### VIX GARCH Volatility Forecast (Variance):
| Date       | Forecast |
|:-----------|:---------|
| 2026-07-01 | 52.3300   |
| 2026-07-02 | 53.9370   |
| 2026-07-03 | 54.4381   |