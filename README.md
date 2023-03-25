# CODE-8-Correlations-and-ANOVA

## Instructions

## Useful Python Code
* Import statsmodels formula api to execute an ANOVA analysis
  * `import statsmodels.formula.api as sm_api`
* Use a code similar to the one below for executing an ANOVA analysis
  * `model = sm_api.ols('Varible ~ C(Groups)', data=df).fit()`
  * `anova_table = sm.stats.anova_lm(model, typ=2)`
  * `print(anova_table)`
* Boxplot - Useful to visualize groups that you analyize using ANOVA
  * `df.boxplot(column="COLUMN",by="GROUPS")`
  * `plt.show()`
* Import the graphics api from statsmodels to create a correlation matrix visualization
  * `import statsmodels.graphics.api as smg`
* Use a code similar to the the one below to create your correlation matrix visualization
  * `df_num = df.select_dtypes(['number'])`
  * `corr_matrix = np.corrcoef(df_num.T)`
  * `smg.plot_corr(corr_matrix, xnames=df_num.columns)`
  * `plt.show()`
## Data sources and documentation

* **coffee.csv**
  * The data was extracted from the CORGIS Dataset Project (https://think.cs.vt.edu/corgis/csv/coffee/).

* **Flight_Delays_2018.csv**
  * The data was extracted from the Kaggle Dataset (https://www.kaggle.com/datasets/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018). The authors of the Kaggle Dataset disclosed that the data was obtained from the Department of Transportation. The extract from the dataset on this assignment can only be used for educational purposes and was obtained by Dr. Villacis Calderon.
