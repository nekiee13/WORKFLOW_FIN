### GSPC
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

---
### DJI
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

---
### QQQ
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

---
### VIX
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

---
### TNX
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

---
### AAPL 
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