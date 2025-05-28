# What drives price of Cars?


## Deployment: 
Client-Facing Summary Now that the modeling is complete, we’ve prepared a concise report tailored for used car dealers interested in improving pricing decisions and inventory planning. The goal was to identify key factors that influence used car prices and build a predictive model that supports smarter, data-driven decisions.


## Key Findings 
Vehicle age and usage are major drivers of price. Newer vehicles and those with lower odometer readings consistently command higher prices. Manufacturer and condition are also strong predictors. Well-maintained cars from reputable manufacturers tend to retain more value. Fuel type and transmission play a role, with automatic and fuel-efficient vehicles generally priced higher.

## Model Overview 
We trained a regularized linear regression model using historical data, after cleaning outliers and handling missing data. The model uses transformed prices (log scale) for improved stability and reduced the number of features using dimensionality reduction. It achieved an average prediction error (RMSE) of approximately $9,195, which is reasonable for the range of used car prices.

## What This Means for Your Business 
The model can help flag overpriced or underpriced vehicles, providing more confidence in pricing decisions. You can use it to prioritize inventory — for example, cars in good condition from high-demand manufacturers offer stronger resale potential. This approach offers a foundation for automated pricing tools, integrating into dealer systems to provide real-time estimates.

## Next Steps 
For better performance on luxury vehicles or edge cases, we recommend exploring non-linear models in the future. Incorporating additional data — like vehicle history, accident reports, or dealership location — could improve prediction accuracy even further. We’re happy to help integrate the model into your internal tools, or support training for your teams on how to use the outputs for smarter decision-making.