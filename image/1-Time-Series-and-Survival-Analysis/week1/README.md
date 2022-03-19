from statsmodels.tsa.seasonal import seasonal_decompose

### BEGIN SOLUTION -- main points 
ss_decomposition_multi = seasonal_decompose(x=dataset_A, 
                                            model='multiplicative', 
                                            period=8)

estimated_trend_multi = ss_decomposition_multi.trend
estimated_seasonal_multi = ss_decomposition_multi.seasonal
estimated_residual_multi = ss_decomposition_multi.resid