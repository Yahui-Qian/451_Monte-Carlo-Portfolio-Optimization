Monte Carlo Portfolio Optimization - README

Overview

This project explores portfolio optimization through Monte Carlo simulation using three selected stocks: Apple Inc. (AAPL), Coca-Cola Co. (KO), and Tesla Inc. (TSLA). The simulation evaluates how investment constraints — particularly the allowance or prohibition of short selling — influence the portfolio's return, volatility, and Sharpe Ratio.

The goal is to generate a large number of random portfolios under different constraints and analyze the distribution of their performance on the efficient frontier.

Objectives

The study aims to:
• Simulate 10,000 portfolios using historical stock data.
• Analyze two cases: (1) long-only portfolios, and (2) portfolios with bounded short selling (weights ∈ [-1, 1]).
• Visualize and interpret the efficient frontiers and Sharpe Ratio distributions.
• Provide insights on how practical investment constraints affect optimization outcomes.

Instructions

Requirements

To run this notebook, install the following Python packages:

pip install pandas numpy matplotlib yfinance

How to Use

1. Open the file `Monte Carlo Analysis.ipynb` using Jupyter Notebook or a compatible IDE.
2. Run each cell sequentially to:
   - Fetch stock data from Yahoo Finance.
   - Calculate annualized mean returns and the covariance matrix.
   - Generate 10,000 portfolios under long-only and short-selling scenarios.
   - Plot the efficient frontier and color by Sharpe Ratio.
3. The final outputs include scatter plots visualizing the risk-return landscape for each scenario.

Simulation Highlights

• Long-Only Portfolios: All weights are constrained to be positive and sum to one. This configuration produces a smooth, interpretable efficient frontier.
• Short-Selling with Bounds: Weights are allowed to be negative, but restricted to remain within [-1, 1] after normalization. This avoids extreme leverage while still expanding the feasible portfolio space.
• Key Insights: TSLA, with its high volatility and return, plays an outsized role in shaping both the frontier and the Sharpe distribution. The introduction of practical bounds on short selling results in a frontier that remains financially plausible, whereas unrestricted shorting often leads to unstable and unrealistic results.

Summary of Findings

The simulation confirms that constraints play a crucial role in shaping portfolio outcomes. While short selling introduces more flexibility, it can lead to impractical portfolios if not carefully managed. Bounded short selling strikes a useful compromise by allowing risk diversification while preventing outliers caused by excessive leverage. The long-only model remains a reliable baseline for conservative investment strategies.

Further details and plots are available in the final report: Monte Carlo Portfolio Optimization.pdf

AI Usage Disclosure

This assignment used generative AI (ChatGPT, by OpenAI) to support the following activities:
• Writing and refining the report narrative
• Debugging simulation logic


All AI contributions were verified by the author before inclusion in the final deliverables.

License

This project is provided for academic and instructional use only. No investment advice is implied or intended.

