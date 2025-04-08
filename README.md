# inflation-and-income-inequality-

What is the relationship between inflation and income inequality in Europe, and how do unemployment and economic growth mediate this relationship?

Description 

Income inequality is a globally significant phenomenon because it impacts economic stability but remains relatively understudied. It influences consumer demand, market size, governance, and migratory patterns (Ostry and Berg, 2011; Milanovic, 2016).
Inflation reduces purchasing power and affects economic development by generating uncertainty, distorting resource allocation, and lowering savings (Barro, 1995). Since inflation affects individuals differently, it was hypothesized that it would lead to inequality (Monnin, 2014).
This study addresses conflicting findings on the relationship between income inequality and inflation (Moradizadeh et al., 2022; Afonso & Sequiera, 2022). Since unemployment and GDP may mediate this relationship, current research is incomplete.
The study aims to evaluate theories on inflation, unemployment, income inequality, and economic growth; investigate the direct relationship between inflation and income inequality; and understand if unemployment and economic growth mediate this relationship. The research question is: "What is the relationship between inflation and income inequality in Europe, and how do unemployment and economic growth mediate this relationship?"

Dataset 

All secondary data was gathered from ourworldindata.org, a reputable and publicly accessible source containing data on CPI, Gini Coefficients, GDP, and unemployment rates. Countries in Europe were selected based on the availability of data from 1995-2021. The dataset was cleaned by excluding countries with missing years to avoid skewing statistical analyses. Outliers were determined using Z-scores. Since the data in its raw form was separate, to create the processed data, I had to combine all of the datasets for each specific country. The dataset included 11 different European countries. Namely, Estonia, France, Germany, Norway, Poland, Portugal, Russia, Spain, Sweden, Turkey, U.K and Ukraine

Problem Statement

Inflation and income inequality are widely recognised as important issues by researchers worldwide due to their multifaceted and significant impacts on society (Oner, 2010; Milanović, 2016). Despite this, conflicting findings exist throughout the field, and the actual relationship between them remains unclear (Monnin, 2014; Moradizadeh et al., 2022; Afonso & Sequeira, 2022). The Phillips curve and Kuznets curve, among other theoretical frameworks, offer opposing perspectives on how inflation, unemployment, and economic growth interact with income inequality (Barth & Bennett, 1975; Kuznets, 2019). These contrasting theories underscore a significant research gap. By incorporating these non-linear dynamics and mediating variables, this study aims to provide a more in-depth, accurate understanding of how inflation influences income inequality in different economic contexts.

Tools 

•	Programming Language: R
•	Data analysis: Jamovi & R
•	Data Visualization: Tableau
•	Data Storage: Excel
•	Data Source: ourworldindata.org

Methodology 

All statistical analyses were conducted using Jamovi, R, Excel, and Tableau. The data cleaning process involved excluding countries with missing data for key years to prevent distortions in the analysis. Outlier detection was performed using z-scores, but instead of the conventional threshold of 3, this study adopted a more conservative threshold of 6, acknowledging that extreme values, such as hyperinflation events, still hold significant information.
An exploratory data analysis was first conducted to examine averages, standard deviations, and time-series trends. Feature scaling was used in Excel for standardization, allowing for clearer visualizations in Tableau. Assumption checks included normality and multicollinearity tests in Jamovi, ensuring that the data met the prerequisites for further statistical modelling. Given the possibility of non-linear relationships suggested in the literature, Spearman’s rho was chosen over Pearson’s r for correlation analyses.
mixed-effect panel regressions were performed in R to test the relationships that the variables had with each other. This method was chosen because it accounts for both time-series and cross-sectional data, making it more robust and helping to minimize confounding variables. A Hausman’s test was used to compare fixed and random effect models. Since linear models often favor random effects, whereas quadratic models tend to favor fixed effects, a mixed-effect model was ultimately selected to balance these approaches. Model selection was further refined using Bayesian Information Criterion (BIC) over Akaike Information Criterion (AIC), as BIC penalizes model complexity more strictly, making it preferable for comparing simple and complex models.
To analyse the direct relationship between inflation and income inequality, a two-way Granger causality test was conducted to assess whether these variables could predict each other over time. This technique allowed for causal inference in a time-series context, helping to determine whether changes in inflation precede income inequality fluctuations, or vice versa.
For the mediation analysis, a causal steps approach was used, incorporating both linear and quadratic relationships identified in the panel regressions. This step established the indirect effects of unemployment and economic growth on the inflation-inequality relationship. A bootstrapped mediation test was then performed, as it provides a non-parametric approach that does not assume a specific data distribution—an important consideration given the potential non-linearity of relationships observed in this study. Sobel’s test was avoided in favor of bootstrapping, as the latter provides more reliable confidence intervals in cases of skewed data.

Results & Findings

This study’s findings reveal that the relationships between income inequality, inflation, and GDP are complex and non-linear. The analysis found a U-shaped relationship between income inequality and inflation (see table 4), indicating that moderate levels of inequality—specifically between .3 and .35—are ideal for reducing inflation. It was observed that the quadratic model explained considerably more variance in inflation than the linear model, suggesting a significant non-linear effect. Furthermore, the investigation into the relationship between GDP and inequality supported the Kuznets curve (see table 5), showing an inverted U-shaped relationship where inequality initially increases with GDP and then decreases as GDP continues to rise.
Additionally, the study’s Granger causality tests revealed that income inequality granger-causes inflation, while the reverse does not hold (see table 8), emphasizing that addressing inequality is key to managing inflation. The mediation analysis further indicated that GDP acts as a small yet statistically significant mediator in the relationship between inflation and inequality, whereas unemployment does not have a significant mediating effect—challenging the traditional view of the Phillips curve (see table 10).
In summary, these findings suggest that economic stability is best maintained by avoiding extremes of inequality through targeted fiscal policies, progressive taxation, and robust social safety nets, particularly during periods of economic growth.

Future Improvements 

The field of income inequality holds great potential for future research as it remains underexplored. Although focusing on Europe reduced some confounding variables, it also limited the study's generalisability. Testing these findings in other geographical contexts would highlight the role of country-specific factors, while studies within individual countries could reduce variability due to national policies, cultures, and economies. As economies evolve, ongoing retesting is essential to maintain temporal validity.
Additionally, given the complexity of income inequality and inflation, other variables like migration or technological changes may mediate their relationship and deserve further study. Since this research challenges the traditional Phillips curve, more work—especially within Europe—is needed to corroborate these findings. Finally, the Granger causality test used here may be overly simplistic or inadequately calibrated, suggesting that future research should consider alternative time lags or more sophisticated methods to better capture non-linear relationships.

Conclusion

In conclusion, this study highlights the complex, non-linear relationship between inflation and income inequality in Europe, emphasizing the role of GDP in mediating this relationship. The findings challenge traditional economic theories, such as the Phillips curve, and suggest that addressing income inequality is crucial for managing inflation. While this research offers valuable insights, further studies in diverse geographical contexts and with more refined methodologies are necessary to fully understand these dynamics and inform policy decisions.

References

1.	Afonso, O. and Sequeira, T. (2022) ‘The effect of inflation on wage inequality: A north–south monetary model of endogenous growth with international trade’, Journal of Money, Credit and Banking, 55(1), pp. 215–249. doi:10.1111/jmcb.12914.
2.	Barro, R.J. (1995) Inflation and Economic Growth [Preprint].
3.	Kuznets, S. (2019). Economic growth and income inequality. In The gap between rich and poor. Routledge, 25–37.
4.	Milanović, B. (2016) Global inequality: A new approach for the age of globalization. Cambridge, MA: The Belknap Press of Harvard University Press.
5.	Monnin, P. (2014) ‘Inflation and income inequality in developed economies’, SSRN Electronic Journal [Preprint]. doi:10.2139/ssrn.2444710.
6.	Moradizadeh, M., Shirmehenji, M.B. and Nourahmadi, M.J. (2022) ‘The Nonlinear Effect of Inflation on Income Inequality (Developing-Countries Study). , 2(4), 29-54.’, Stable Economy Journal, 2(4), pp. 29–54.
7.	Oner, C. (2010) ‘What is inflation’, Finance & Development, 47(1).
8.	Ostry, J. and Berg, A. (2011) Inequality and unsustainable growth: Two sides of the same coin?, 11(08), p. 1. doi:10.5089/9781463926564.006.







