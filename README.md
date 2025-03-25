# GARCH_noise
Extension of the GARCH model to calculate jump/extreme shocks

# GARCH(1,1) Model with Synthetic Return Data

This repository demonstrates the use of the GARCH(1,1) model to analyze the volatility of financial returns. The code generates synthetic return data and fits a GARCH(1,1) model to model the conditional volatility and residuals.

## Code Overview

### Steps performed by the code:

1. **Generate Synthetic Data:**
   - We simulate 1000 return data points using a normal distribution with mean 0 and standard deviation 1.

2. **Fit a GARCH(1,1) Model:**
   - We use the `arch` library's `arch_model` function to define a GARCH(1,1) model with the simulated returns.
   - The model assumes zero mean and GARCH volatility structure with lag values `p=1` and `q=1`.

3. **Model Fitting:**
   - The model is fit using the `fit()` method, and the summary of the results is printed.

4. **Extract Results:**
   - Extract the conditional volatility (`σ_t`) and residuals (`ε_t`) from the fitted model.

5. **Plot the Results:**
   - The code generates two plots:
     1. **GARCH Noise (ε_t):** This shows the residuals or shocks in the model.
     2. **Conditional Volatility (σ_t):** This shows the volatility over time predicted by the model.

### Visualizations:

- **GARCH Noise (ε_t):** The residuals from the GARCH model, visualizing how the shocks evolve over time.
- **Conditional Volatility (σ_t):** The predicted volatility over time based on the GARCH model.

## Example Output

The model summary and two plots will be displayed:

- A plot of the GARCH noise (shocks).
- A plot of the conditional volatility over time.
