Kaggle:
https://www.kaggle.com/code/marmurrr/raid-alert-prediction

Datasets:
https://github.com/Vadimkin/ukrainian-air-raid-sirens-dataset/tree/main

Overview: This project analyzes historical air raid alerts in Ukraine as a continuous time series to identify long-term trends, intraday cycles, and the predictability of conflict-related threat metrics.

Methodology: The pipeline standardizes data at the oblast level, filters out simultaneous duplicate alerts, and evaluates the forecasting performance of an ARIMA model against Meta's Prophet.

Insights: While Prophet proved more resilient against extreme volatility spikes (lower RMSE), ARIMA captured localized short-term dependencies slightly better (lower MAE), demonstrating that combining structural trend fitting with local autoregression yields the most reliable results.

Future Enhancements:
Integrate Real-Time Exogenous Factors: Incorporating external open-source intelligence (OSINT) data—such as monitored military aviation patterns, weather conditions affecting drone flight paths, and tactical asset deployments—as exogenous regressors inside Prophet or ARIMAX models to structurally reduce forecasting error spikes during sudden escalations.

Implement Algorithmic Change-Point Detection: Deploying a time-series segmentation algorithm like PELT (Pruned Exact Linear Time) to automatically identify major structural shifts in alert intensity over time, allowing the models to automatically adjust their weights to separate historical phases of the conflict from current patterns.

Refactoring:
Split the notebook into different files and folders according to best practices.
