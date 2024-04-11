# Challenge4 Whale Analysis

This is my submition for challenge 4 homework. below is the prompt:












Background
You have been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

You just learned these quantitative analysis techniques with Python and Pandas, and you want to determine which portfolio is performing the best across multiple areas: volatility, returns, risk, and Sharpe ratios.

What You’re Creating
You need to create a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. You will be given the historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. You will then use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500 IndexLinks to an external site.).

Files
Download the following files to help you get started:

Module 4 Challenge files

Instructions
The instructions for this assignment are divided into three parts:

Prepare the Data

Perform Quantitative Analysis

Create a Custom Portfolio

Prepare the Data
First, you will read in and clean several CSV files for analysis. The CSV files contain data on whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Use the Whale Analysis starter code to complete the following steps:

Use Pandas to read the following CSV files into DataFrames. Be sure to convert the dates to a DateTimeIndex.

whale_returns.csv: Contains returns of some famous "whale" investors' portfolios.

algo_returns.csv: Contains returns from the in-house trading algorithms from your company.

sp500_history.csv: Contains historical closing prices of the S&P 500 Index.

Identify and remove null values.

Remove any non-numeric values (e.g., dollar signs) from the DataFrames and convert the data types as needed.

The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. Convert the S&P 500 closing prices to daily returns.

Join Whale Returns, Algorithmic Returns, and the S&P 500 Returns into a single DataFrame with columns for each portfolio's returns.

returns-dataframe.png

Perform Quantitative Analysis
Analyze the data to determine if any of the portfolios outperform the stock market (that is, the S&P 500). Specifically, you will do a performance analysis and a risk analysis, and then calculate rolling statistics and Sharpe ratios.

Performance Analysis
Calculate and plot daily returns of all portfolios.

Calculate and plot cumulative returns for all portfolios. Does any portfolio outperform the S&P 500?

Risk Analysis
Create a box plot for each of the returns.

Calculate the standard deviation for each portfolio.

Determine which portfolios are riskier than the S&P 500.

Calculate the annualized standard deviation.

Rolling Statistics
Calculate and plot the rolling standard deviation for all portfolios, using a 21-day window.

Calculate and plot the correlation between each stock to determine which portfolios mimic the S&P 500.

Choose one portfolio, then calculate and plot the 60-day rolling beta between that portfolio and the S&P 500.

Rolling Statistics Challenge: Exponentially Weighted Average
An alternative method to calculate a rolling window is to find the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations. Try calculating the ewmLinks to an external site. with a 21-day half-life.

Sharpe Ratios
Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right? Follow these steps:

Using the daily returns, calculate the Sharpe ratios and visualize them in a bar plot.

Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.

Create a Custom Portfolio
You’re excited that you were able to prove that the algorithmic trading portfolios are doing so well compared to the market and whales portfolios. However, now you are wondering whether you can choose your own portfolio that performs just as well as the algorithmic portfolios. Investigate by doing the following:

Use Google SheetsLinks to an external site. and its built-in GOOGLEFINANCE function to choose 3–5 stocks for your portfolio.

NOTE
In the Resources folder, you'll find CSV files for AAPL, COST and GOOG. These are provided as backup in the event that the GOOGLEFINANCE function is not working properly.

Download the data as CSV files and calculate the portfolio returns.

Calculate the weighted returns for your portfolio, assuming equal number of shares per stock.

Add your portfolio returns to the DataFrame with the other portfolios.

Run the following analyses:

Calculate the annualized standard deviation.
Calculate and plot the rolling standard deviation with a 21-day window.
Calculate and plot the correlation.
Calculate and plot beta for your portfolio compared to the S&P 60 TSX.
Calculate the Sharpe ratios and generate a bar plot.
How does your portfolio perform?

Resources
Pandas API documentationLinks to an external site.

Exponential weighted function in PandasLinks to an external site.

GOOGLEFINANCE function helpLinks to an external site.

Supplemental Guide: Fetching Stock Data Using Google Sheets

Hints
After reading in each CSV file, don't forget to sort each DataFrame in ascending order by the Date using sort_index. This is especially important when working with time series data, as you want to make sure date indexes go from earliest to latest.

Be sure to use head() or tail() when you want to look at your data, but don't want to print to a large DataFrame.

Requirements
Data Preparation (20 points)
To receive all points, you must:

Use Pandas to read each CSV file in as a DataFrame. (3 points)
Identify and remove all null values. (4 points)
Convert the S&P 500 closing prices to daily returns. (5 points)
Join the whale returns, algorithmic returns, and the S&P 500 returns into a single DataFrame with columns for each portfolio's individual returns. (8 points)
Quantitative Analysis (20 points)
To receive all points, your code must:

Calculate and plot the daily and cumulative returns of all portfolios. (2 points)
Create a box plot for each of the returns. (2 points)
Calculate the standard deviation for each portfolio. (2 points)
Determine which portfolios are riskier than the S&P 500. (3 points)
Calculate the annualized standard deviation for each portfolio. (2 points)
Calculate and plot the rolling standard deviation for all portfolios using a 21-day window. (3 points)
Calculate and plot the correlation between each stock to determine which portfolios may mimic the S&P 500. (3 points)
Choose one portfolio, then calculate and plot its beta as compared to the S&P 500. (3 points)
Sharpe Ratios (15 points)
To receive all points, your code must:

Use the daily returns to calculate the Sharpe ratios. (4 points)
Visualize the Sharpe ratios using a bar plot. (3 points)
Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios. (8 points)
Custom Portfolio (15 points)
To receive all points, your code must:

Use the GOOGLEFINANCE function to choose a portfolio. (3 points)
Download the data needed as CSV files and calculate the portfolio returns. (4 points)
Add the portfolio returns to the DataFrame with the other portfolios, then analyze and compare all portfolios. (8 points)
Coding Conventions and Formatting (10 points)
To receive all points, your code must:

Place imports at the beginning of the file, just after any module comments and docstrings and before module globals and constants. (3 points)
Name functions and variables with lowercase characters and with words separated by underscores. (2 points)
Follow Don't Repeat Yourself (DRY) principles by creating maintainable and reusable code. (3 points)
Use concise logic and creative engineering where possible. (2 points)
Deployment and Submission (10 points)
To receive all points, you must:

Submit a link to a GitHub repository that’s cloned to your local machine and that contains your files. (5 points)

Include appropriate commit messages in your files. (5 points)

Code Comments (10 points)
To receive all points, your code must:

Be well commented with concise, relevant notes that other developers can understand. (10 points)
Submission
Use the provided starter Jupyter Notebook to store the code for your data preparation, analysis, and visualizations. Put any analysis or answers to assignment questions in raw text (markdown) cells in the report.

Upload your notebook to a new GitHub repository.

Add the URL of your GitHub repository to your assignment when submitting via Bootcamp Spot.

NOTE
You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Advisor. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.

IMPORTANT
It is your responsibility to include a note in the README section of your repo specifying code source and its location within your repo. This applies if you have worked with a peer on an assignment, used code in which you did not author or create sourced from a forum such as Stack Overflow, or you received code outside curriculum content from support staff such as an Instructor, TA, Tutor, or Learning Assistant. This will provide visibility to grading staff of your circumstance in order to avoid flagging your work as plagiarized.

If you are struggling with a challenge assignment or any aspect of the academic curriculum, please remember that there are student support services available for you:

Ask the class Slack channel/peer support.

AskBCS Learning Assistants exists in your class Slack application.

Office hours facilitated by your instructional staff before and after each class session.

Tutoring GuidelinesLinks to an external site. - schedule a tutor session in the Tutor Sessions section of Bootcampspot - Canvas

If the above resources are not applicable and you have a need, please reach out to a member of your instructional team, your Student Success Advisor, or submit a support ticket in the Student Support section of your BCS application.
