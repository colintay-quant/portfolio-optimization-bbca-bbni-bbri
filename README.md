# portfolio-optimization-bbca-bbni-bbri
Markowitz mean-variance portfolio optimization on Indonesia banking stocks
## Overview
This project applies Markowitz Mean-Variance Optimization to find the optimal portfolio allocation across three major Indonesia Banking stocks: Bank Central Asia (BBCA), Bank Negara Indonesia (BBNI), and Bank Rakyat Indonesia (BBRI), using historycal price data from 2019-2025
## Methodology
- **Data**: Daily price stocks 2019-2025 for BBCA, BBNI, and BBRI (via yfinance/Yahoo Finance)
- **Return Calculation**: Calculate daily return from closing price, and convert to annualized expected return
- **Risk Measurement**: Calculate annualize volatility and covariance matrix between 3 stocks
- **Monte Carlo Simulation**: Generate 5000 combination random portfolio
- **Optimization**: Using Sharpe Ratio to identify portfolio with the best return-risk ratio (Max Sharpe)
## Key Finding
The Markowitz Mean Variance Optimization Idenntified the following optimal portfolio weights (Max Sharpe Ratio):
- **BBCA: 75.9%**
- **BBNI: 23.89%**
- **BBRI: 0.14%**
This results makes sense because BBCA has the lowest volatility among three stocks (24.94%), while still maintaining a competitive return (11.93%) - Nearly matching BBRI's slightlyhigher return (12.20%), which comes with much higher volatility (32.52%). This gives BBCA a better individual risk-return (Sharpe) ratio, justifying its dominant weight in the optimal portfolio.
BBNI receives a smaller allocation, likely acting a diversifier despite having the lowest return (9.41%) and highhest volatility.
**Note**: These results are spesific to this combination of stocks and the 2019-2025 data period. All three stocks belong to the same sector (banking), so sector diversification is still limitited. A natural extension would be adding stocks from other sectors.
## Visualizations
- Stock price chart
- Covariance heatmap
- Efficient frontier scatter plot
## What I learned
This is my first coding project. I had wanted to get into quantitative finance for a while, but always held back in my technical foundation and couldn't find the right person to guide me through it. So, I ended up learning with AI as my mmain study partner.
Writing my very first "Hello World" during this project was a genuinely exciting moment. From there, I ran into plenty of syntax errors and confusing concepts along the way. Python's learning curve felt overwhelming this times. But, rather than just copying code, I made a point of asking for the meaning of behind every line I wrote, so I could actually understand what the code was doing instead just runninng it.
This project taught me the fundamentals of working with financial data in Python: pulling stock data, calculating returns and volatility, understanding covariance between assets, and applying Monte Carlo simulation to find an optimal portfolio. More than the technical skills, it gave me confidence that I can actually learn and apply quantitative finance concepts, even starting from zero.
**Next steps**: I plan to extend this project by including stocks from different sectors to test sector diversification, and to explore other quant finance topics such as pairs trading and backtesting frameworks.
## Disclaimer
This is an educational project for learning purposes, not investment advice.
Built with guidance from AI tools (Claude and Chat GPT) while learning Phyton and quantitative finance concepts.
## Tools Used
Phyton, pandas, numpy, matplotlib, seaborn, yfinance
