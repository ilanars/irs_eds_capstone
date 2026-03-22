# Lightning Presentation Speaker Notes

I looked at how extreme heat—an increasingly prevalent climate risk—may influence food insecurity in New York City, via affordability. 

The underlying hypothesis is that more hot days increase energy costs, which can strain household budgets and potentially increase reliance on SNAP. This is important because it can help policymakers develop energy assistance programs that properly address increasing need as summers get hotter.

To test this, I combined monthly SNAP participation data with temperature data from Central Park between 2009 and 2018.

I constructed a monthly heat metric defined as the number of days per month above 82 degrees F, and focused only on the warm season: May through September.

In the time series, we see a slight upward trend in heat days over time, while SNAP participation appears to decline over time. This already suggests that the relationship may not be positive (not ideal for my hypothesis), but I formally tested it using regression analysis.

So I ran two regressions—model 1: a simple one that just looks at the relationship between heat days and SNAP recipients in the same month, and model 2: a multiple linear regression that includes a lagged heat variable (to test for the impacts of heat in the prior month on snap recipients in the current month), and controlling for seasonality. 

Before I get into the regression results, you can see on the two scatterplots the contemporaneous (orange) and lagged (yellow) relationships are both nearly flat, although positively correlated. 

Consistent with this, neither model finds statistically significant relationships between heat days and SNAP recipients. Both models resulted in very small slopes, with quite high p-values.

Interestingly, the R squared value does increase from model 1 to model 2, potentially indicating that more of the variability in snap is explained by lagged heat effects, but the R squared could have also gone up simply because I added more variables into the regression (and the adjusted R squared was 0…)

While the main finding is that there is no statistically significant relationship between heat exposure and SNAP participation, I think there would be value in continuing to examine this question with better measures of food security, since it appears that SNAP enrollment is primarily explained by long-term trends over time, rather than by monthly heat variation. 

A next step in this study could be to look at data on monthly food expenditures, which may be more reflective of monthly budget changes than SNAP data. It would also be helpful to control for more variables, since monthly budgets have many categories that can be impacted by higher energy costs. Lastly, I would also control for income in further studies. 


