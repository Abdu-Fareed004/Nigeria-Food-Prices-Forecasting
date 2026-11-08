# Nigeria-Food-Prices-Forecasting

Nigeria Food Price Forecasting Using Machine Learning and Time-Series Models

A comparative forecasting project investigating baseline, statistical, and machine learning approaches for predicting food prices in Nigeria.

Repository: Nigeria-Food-Prices-Forecasting
Notebook: food-prices-forcasting-in-ng.ipynb
Kaggle Notebook: Food Prices Forecasting in Nigeria
Portfolio: Hassan Farid — Portfolio

⸻

1. Project Overview

Food price movements have important implications for household purchasing power, food affordability, and economic planning.

This project investigates the use of forecasting methods to model food price behaviour in Nigeria. It compares simple benchmark approaches, a statistical time-series model, and a machine learning model.

The analysis covers four food commodities:

* Rice
* Beans
* Garri
* Yam

Four forecasting approaches were evaluated:

* Last Value
* Seasonal Naive
* SARIMA
* Gradient Boosting

The central objective is to assess whether more complex forecasting models provide better predictive performance than simpler baseline approaches.

2. Project Objectives

The project aims to:

* Investigate food price forecasting as a time-series modelling problem.
* Compare baseline, statistical, and machine learning forecasting methods.
* Evaluate forecasting errors using MAE, RMSE, and MASE.
* Examine the relative performance of simple and complex forecasting approaches.
* Identify the strongest-performing approach among the evaluated models.
* Explore opportunities for improving food price forecasting through additional features and more extensive evaluation.

3. Technical Highlights

* Multi-commodity analysis: Investigated rice, beans, garri, and yam.
* Model benchmarking: Compared Last Value and Seasonal Naive baselines against SARIMA and Gradient Boosting.
* Statistical forecasting: Included SARIMA as a time-series modelling approach.
* Machine learning: Evaluated Gradient Boosting as a predictive alternative.
* Forecast evaluation: Used MAE, RMSE, and MASE to compare forecasting errors.
* Baseline assessment: Examined whether complex models improved on simpler forecasting strategies.

Key technical finding: The Last Value baseline achieved the lowest reported error across all three evaluation metrics, outperforming the more complex approaches in this evaluation.

4. Data and Scope

The project focuses on Nigerian food price observations and the forecasting of selected staple commodities.

The identified data source for this work is WFP Nigeria food-price data accessed through the Humanitarian Data Exchange (HDX).

The exact dataset version, observation period, market coverage, and data-processing details should be interpreted from the notebook’s data-loading and preparation sections.

The four commodities considered are:

Commodity	Forecasting scope
Rice	Food price forecasting
Beans	Food price forecasting
Garri	Food price forecasting
Yam	Food price forecasting

The National Bureau of Statistics (NBS) Selected Food Prices Watch may provide a supplementary source for future data integration. It should not be assumed to be part of the current experiment unless confirmed in the notebook.

5. Methodology

The project compares four forecasting approaches.

5.1 Last Value

The Last Value method uses the most recently observed value as the forecast.

It provides a simple benchmark against which more advanced forecasting methods can be assessed.

5.2 Seasonal Naive

The Seasonal Naive approach uses a previous observation from a corresponding seasonal period as its forecast.

It provides a benchmark for assessing whether seasonal repetition offers useful predictive information.

5.3 SARIMA

Seasonal Autoregressive Integrated Moving Average (SARIMA) is a statistical time-series approach designed to model autoregressive behaviour, differencing, moving-average effects, and seasonality.

Its inclusion provides a statistical forecasting comparison against the simpler baseline methods.

5.4 Gradient Boosting

Gradient Boosting is a machine learning approach that combines sequentially trained decision-tree models to improve predictive performance.

It was included to investigate whether a machine learning approach could capture useful patterns beyond those represented by the simpler forecasting methods.

6. Model Performance and Results

The reported evaluation produced the following results:

Model	MAE	RMSE	MASE
Last Value	195.87	220.22	0.80
SARIMA	207.56	234.52	0.85
Gradient Boosting	270.28	301.56	1.10
Seasonal Naive	489.64	520.01	2.00

Lower values indicate lower forecasting error for all three metrics.

6.1 Interpretation of results

Last Value — strongest reported performance

Last Value achieved the lowest MAE, RMSE, and MASE among the evaluated approaches.

This indicates that, under the reported evaluation, using the latest observed value produced more accurate forecasts than the other tested methods.

SARIMA — second-best performance

SARIMA achieved the second-lowest errors across all three metrics.

Its performance was relatively close to the Last Value benchmark, suggesting that the statistical model did not provide an improvement over the simple baseline in this experiment.

Gradient Boosting — higher forecasting error

Gradient Boosting recorded higher errors than both Last Value and SARIMA.

This demonstrates that the more complex machine learning approach did not outperform the simpler approaches under the reported evaluation.

Seasonal Naive — weakest reported performance

Seasonal Naive produced the highest errors across the three metrics.

This suggests that the seasonal benchmark, as implemented and evaluated in this experiment, was less effective than the other tested methods.

6.2 Understanding the evaluation metrics

Metric	Meaning
MAE	Mean Absolute Error; measures average absolute forecast error.
RMSE	Root Mean Squared Error; penalises larger forecasting errors more heavily.
MASE	Mean Absolute Scaled Error; compares forecast error against a scaling benchmark.

The reported MASE of 0.80 for Last Value indicates that its scaled error was below the benchmark used in the MASE calculation.

MAE and RMSE are expressed on the same scale as the target price variable, while MASE is a scaled, unitless metric.

These metrics measure forecasting error, not classification accuracy.

7. Key Findings

The experiment highlights several important findings:

1. Last Value outperformed the three other evaluated approaches across MAE, RMSE, and MASE.
2. SARIMA achieved the second-best performance, but did not improve on the Last Value benchmark.
3. Gradient Boosting recorded higher forecasting errors than Last Value and SARIMA.
4. Seasonal Naive produced the highest reported forecasting errors.
5. Model complexity alone did not translate into improved predictive performance.

Main conclusion: The simplest forecasting approach was the strongest performer in the reported evaluation. This reinforces the importance of establishing credible baseline models before adopting more complex forecasting methods.

8. Repository Structure

The repository currently contains the following files:

Nigeria-Food-Prices-Forecasting/
│
├── README.md
│
└── food-prices-forcasting-in-ng.ipynb

File	Description
README.md	Project overview, methodology, model comparison, results, and documentation.
food-prices-forcasting-in-ng.ipynb	Main Jupyter Notebook containing the food price forecasting analysis and experiments.

There are no separate data, source-code, or dependency folders in the current repository root.

9. How to Explore and Run the Project

Option 1: Explore on GitHub

1. Open the GitHub repository.
2. Select food-prices-forcasting-in-ng.ipynb.
3. Review the data preparation, forecasting methods, evaluation outputs, and findings.

GitHub renders Jupyter Notebooks as static content. Some interactive notebook features may not work in the GitHub preview.

Option 2: Run on Kaggle

The Kaggle notebook is the recommended starting point for interactive execution.

1. Open the Food Prices Forecasting Kaggle Notebook.
2. Sign in to Kaggle if required.
3. Open the notebook.
4. Use Kaggle’s available notebook execution options to run the cells in sequence.
5. Review the data preparation, model implementations, forecasting results, and evaluation metrics.

Local execution

The current GitHub repository root contains the notebook and README but no separate requirements.txt or dataset file.

For local execution, inspect the notebook’s imports and data-loading cells, install the dependencies used by the notebook, and make the required data available at the expected location.

10. Reproducibility and Evaluation Considerations

For a meaningful technical review:

* Execute the notebook cells in their intended order.
* Examine the data-loading and preprocessing stages.
* Inspect how the forecasting target and prediction periods are defined.
* Review the evaluation procedure and the way each model is benchmarked.
* Confirm the data split and forecasting horizon from the notebook before interpreting the reported results.
* Compare the reported metrics using consistent evaluation conditions.

The repository currently uses a notebook-centred structure. A separate dependency file and standalone data directory are not included in the root.

11. Limitations

* Forecasting performance is dependent on the quality, coverage, and consistency of the available observations.
* The reported results should not automatically be generalised to every Nigerian market or future economic condition.
* The Last Value baseline’s performance does not establish that it will remain the best approach across different commodities, markets, or forecast horizons.
* The exact evaluation period, forecast horizon, and market coverage should be checked in the notebook before drawing broader conclusions.
* Changes in inflation, exchange rates, transportation costs, seasonal supply, and other economic factors may affect future food prices.
* Additional validation is required before using the forecasts to support operational or policy decisions.

12. Future Improvements

Potential extensions include:

* Commodity-level and market-level performance comparisons.
* Evaluation across multiple forecasting horizons.
* More extensive temporal validation.
* Additional seasonal and economic explanatory features.
* Improved treatment of missing observations and outliers.
* Investigation of exchange-rate and inflation-related variables where reliable data are available.
* Integration of additional official food-price data sources, subject to data compatibility and validation.
* Further statistical analysis of forecast errors and model stability.

13. Author and Project Links

Hassan Farid
Data Science | Machine Learning | Artificial Intelligence

* GitHub Profile
* Kaggle Profile
* LinkedIn
* Portfolio

⸻

This project documents an applied forecasting experiment focused on Nigerian food prices, model benchmarking, and the interpretation of predictive performance.
