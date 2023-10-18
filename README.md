# Integrated Data Visualization: Analyzing Stock and Cryptocurrency Performance
## Introduction:
In the age of data-driven decision-making, it's crucial to harness the power of data visualization to gain insights into the performance of various assets. This report dives into the world of data visualization, using Tableau to analyze both stock and cryptocurrency performance. We've meticulously collected and prepared the data for this analysis, created interactive and informative visualizations, and leveraged conditional statements to add a layer of depth to our insights.
## Stock Performance Visualization in Tableau: A Comprehensive Overview

1. Setting Up Stock Data in Google Sheets:
   * Google Sheet Creation:
   *  Open a new Google Sheet and name it "Stock Data for Tableau."
   *  Create headers for Stock, Price, Date, and Daily % Change.
2. Fetching Stock Prices:
   * Enter stock tickers (OKTA, AMZN, BBBYQ, SEDG, TSLA) in the Stock column.
   * Use the formula =GoogleFinance(A2, "price", EDATE(TODAY(), -12), TODAY()) to fetch prices for the last 12 months.
3. Calculating Daily % Change:
   * Utilize the formula = (latest Price – the price day before) / price day before for each stock.
4. Recalculation Setup:
   * Configure recalculation settings to update hourly.
### Stock Portfolio Sheet:
1. Stock Portfolio Details:
   * Create columns for Stock Name, Units Bought, Price When Purchase, and Purchase Cost.
   * Input data for each stock's units and purchase price.
2. Connect Data in Tableau:
   * Connect Stock Price and Stock Portfolio sheets in Tableau.
   * Establish a relationship using the stock name.
### Area Chart:
1. Area Chart Creation:
   * Customize the default properties for Price When Purchase, Purchase Cost, and Daily % Change.
   * Create a calculated field for Clean Stock Name to display full stock names.
   * Generate a custom date field and use it to create an area chart with Clean Stock, Day, and Close.
### Profit/Loss Calculation Sheet:
1. Profit/Loss Calculation:
   * Develop calculated fields for Last Closing Price, Current Value, and P/L.
   * Display stock names and P/L values in a tabular format.
### Portfolio Performance Line Chart:
1. Portfolio Performance Line Chart:
   * Create a calculated field for Daily Value.
   * Visualize the daily portfolio value over time using Day and Daily Value.
### Bubble Chart:
1. Bubble Chart:
   * Generate a bubble chart using Stock Name, Day, and Daily % Change.
   * Apply formatting and coloring for clarity.
### Volatility Chart:
1. Volatility Chart:
   * Create a new sheet for the Volatility Chart.
   * Display weekly average volatility using Week and Daily % Change.
   * Apply formatting and coloring based on stock names.
### Lollipop Chart:
1. Lollipop Chart:
   * Design a dual-axis chart for the top 3 holdings.
   * Use Current Value to represent the bar and circle charts.
   * Apply formatting and coloring, and create a set for the top 3 holdings.
### Overview Cards:
1. Overview Cards:
   * Create separate sheets for Portfolio Value, Profit/Loss, and Profit/Loss Percentage.
   * Develop calculated fields for relevant metrics.
   * Design cards displaying portfolio value, profit/loss, and profit/loss percentage.
### Stock Performance Dashboard:
1. Stock Performance Dashboard:
   * Combine all worksheets into a cohesive dashboard.
   * Utilize a blue color scheme for visual consistency.
   * Add a blank container for organized placement.
   * Use the period parameter as a filter for consistency across all sheets.
   * Provide clear titles for each visualization.
2. Final Touches:
   * Perform additional formatting for a polished appearance.
   * Ensure interactivity by testing the parameter's functionality.
   * Title the dashboard as "Stock Performance Dashboard."
     
### Stock Performance Analysis:
Our journey begins with an in-depth exploration of stock performance. We collect historical stock price data and portfolio information in Google Sheets, and the Tableau platform serves as our canvas for creating meaningful visualizations. Key steps include the creation of area charts, profit/loss calculations, portfolio performance line charts, bubble charts, volatility charts, and lollipop charts. We utilize calculated fields and custom parameters to make the analysis interactive and comprehensive.

## Individual Stock Analysis Dashboard: A Step-by-Step Guide
### Gradient Background Setup:
1. Creating Gradient Background in Google Sheets:
   * In Google Sheets, set up two blank sheets: one named "Stock Name" and the other named "Colour."
   * In the "Colour" sheet, enter values in the "Path" and "Position" columns to create a gradient background.
2. Tableau Integration:
   * Connect both Google Sheets in Tableau and perform an inner join using the condition 1=1.
3. Path Binning:
   * In Tableau, create path bins with a bin size of 0.4.
   * Convert the "Position" field into a dimension.
4. Index Calculation:
   * Create a calculated field named "Index" using the formula INDEX() - 1.
   * Place this field in rows and set it to compute using Path bins.
5. Colour Calculation:
   * Create a calculated field named "Colour" with the formula WINDOW_MAX(MAX([STOCK])) + STR([INDEX]).
   * Add this field to the color shelf and apply a palette.
6. Adjust the Size:
   * Remove the axis to fill the entire view.
   * Create a parameter named "Stock Name" with stock names as its values.
   * Utilize a calculated field as a filter to make the parameter valid.
7. Applying Different Palettes:
   * Assign distinct palettes to each stock to match the background color.
   * Use the "Stock Name" parameter to facilitate this process.
### Stock Price Line Chart:
1. Configuring Data Source:
   * Return to the previous data source.
   * Create a new worksheet named "Stock Price Line Chart."
2. Calculated Fields:
   * Create a calculated field called "Stock Filter" to match the selected stock with the parameter.
   * Use this calculated field as a filter and format the chart as desired, including adding trendlines.
### Volatility Chart:
1. Volatility Chart:
   * Create another worksheet for displaying volatility.
   * Use "Day" on the columns shelf and "Daily % Change" on the rows shelf.
   * Apply appropriate formatting and trendlines.
### Performance Cards:
1. Performance Cards Creation:
   * Develop separate worksheets for performance cards, including "Current Price," "Current Holdings," "One-Year Performance," and "All-Time Profit/Loss."
2. Calculated Fields:
   * Create calculated fields for each performance card, such as "Current Price Title," "Current Holdings Title," "All-time P/L," "First Closing Price," and "% Change One Year."
3. Formatting and Display:
   * Design each card by dragging relevant fields (e.g., "Latest Price," "Current Value," "P/L," "% Change One Year").
   * Format the cards with appropriate number formatting and make them entirely viewable.
### Individual Stock Performance Dashboard:
1. Combining Worksheets:
   * Create another dashboard and incorporate the following elements:
       * Background gradient.
       * Stock Price Line Chart.
       * Volatility Chart.
       * Performance Cards.
2. Arrangement and Formatting:
   * Arrange the components on the dashboard canvas as desired.
   * Format the elements to match the gradient background's color pattern.
   * Make the "Stock Names" parameter visible for user interactivity.
3. Parameter as Filter:
   * Utilize the "Stock Names" parameter as a filter for all sheets.
   * This allows users to click on different stock names and view their price charts, volatility charts, and performance cards individually.

### Individual Stock Analysis:
Moving to individual stock performance, we utilize a background with color-changing gradients to create visually appealing dashboards. The emphasis is on real-time tracking of specific stocks, allowing users to filter and analyze their investments. Performance cards, such as current price, current value, overall profit/loss, and current portfolio value, provide a quick snapshot of each stock's status.

## Cryptocurrency Analysis - A Comprehensive Guide
In this guide, we will walk through the process of conducting cryptocurrency analysis using Tableau. We will start by preparing and importing data from Google Sheets and then proceed to create visualizations to analyze cryptocurrency performance.

### Data Preparation:
1. Google Sheets Setup:
   * Create a blank Google Sheets document.
   * Obtain historical data for the selected cryptocurrencies from a trusted source, e.g., https://www.investing.com/.
   * Import data into Google Sheets using the IMPORTHTML function, specifying the URL and the query as "table/list."
   * For each cryptocurrency (e.g., Bitcoin, Ethereum, Litecoin, Chainlink, Matic), create a unique formula.
2. Automated Data Refresh:
   * To ensure that data remains up-to-date, set up an automatic data refresh using Google Apps Script. Write a script to refresh the data at regular intervals, e.g., every 5 minutes.
   * Save the script and set up a time-driven trigger for it.
   * Save the Google Sheets document as "Crypto Price."
3. Coin Holdings Sheet:
   * Create a new Google Sheets document.
   * List the cryptocurrencies in column A.
   * In columns B and C, enter the number of units bought and the purchase price when buying each cryptocurrency.
4. Tableau Connection:
   * Connect Tableau to the "Crypto Price" and "Coin Holdings" Google Sheets documents.
   * Establish a relationship between the two documents.
### Candlestick Chart:
1. Candlestick Chart Creation:
   * In Tableau, create a new worksheet and name it "Candlestick Chart."
   * Calculate fields for "Close," "Low," and "High" by subtracting "Open" from "Sum (Price)" for each cryptocurrency.
   * Generate a custom date field.
2. Candlestick Chart Configuration:
   * Create a dual-axis chart by placing "Day" on columns and "High" on rows, followed by "Open" on rows.
   * Calculate the size by dragging "Close - Open" to the "Size" shelf.
   * Adjust the size to resemble a candlestick chart.
3. Coloring and Formatting:
   * Apply a red-green diverging color scheme to the candlestick chart.
   * Format the chart according to preferences.
### Performance Cards:
1. Performance Card Creation:
   * Develop performance cards, including "Latest Price," "Current Value," "Overall Profit/Loss," and "Current Portfolio Value" for the cryptocurrency holdings.
2. Calculated Fields:
   * Create calculated fields for each card, such as "Latest Close," "Current Value," "P/L Overall," and "Current Portfolio Value."
3. Card Configuration:
   * Design each card by placing the relevant fields, and format the cards for currency and percentage.
### Conditional Statements:
1. Conditional Statements Sheet:
   * Create a new worksheet for conditional statements.
   * Define calculated fields to conditionally display coin names, percentage change, and upward/downward movement.
2. Conditional Statements Configuration:
   * Arrange these fields on the worksheet to display clean coin names, percentage change for the past 30 days, and up/down status.
   * Adjust formatting and data types.
### Portfolio Line Chart:
1. Portfolio Line Chart Creation:
   * Create a new worksheet named "Portfolio Line Chart."
   * Calculate a "Daily Value" field by multiplying "Close" with "Units Bought."
2. Portfolio Line Chart Configuration:
   * Set the default properties for "Daily Value" as currency.
   * Create a line chart by placing "Day" on columns and "Daily Value" on rows.
### Dashboards:
1. Cryptocurrency Price Tracker Dashboard:
   * Create a dashboard named "Cryptocurrency Price Tracker" with a dark blue theme.
   * Add components such as the candlestick chart, price cards, performance cards, conditional statements, and cryptocurrency icons.
   * Utilize the icon sheet as a filter for all elements, arranging and formatting them to fit the background.
2. Cryptocurrency Portfolio Dashboard:
   * Create a dashboard named "Cryptocurrency Portfolio" with a similar dark blue theme.
   * Include the portfolio line chart, current portfolio value card, performance cards, and conditional statements.
   * Arrange and format the components to match the background.
By following these steps, you can successfully conduct cryptocurrency analysis using Tableau, enabling you to monitor cryptocurrency prices and your portfolio's performance effectively. This comprehensive guide covers data preparation, chart creation, card setup, conditional statements, and dashboard design for cryptocurrency analysis.

### Cryptocurrency Analysis:
In a world where cryptocurrencies are becoming increasingly relevant, we extend our analysis to include popular digital assets such as Bitcoin, Ethereum, Litecoin, Chainlink, and Matic. We fetch data from the web, create a candlestick chart, and perform extensive calculations to derive insights. The use of conditional statements helps in quickly assessing the price movement of these cryptocurrencies. An elegant dashboard provides a comprehensive view of the cryptocurrency market, while another focuses on portfolio management.

## Conclusion:
This report showcases the power of data visualization and analytics in understanding the performance of both traditional assets like stocks and emerging ones like cryptocurrencies. By combining the capabilities of Google Sheets and Tableau, we've created interactive and visually engaging dashboards that empower users to track, analyze, and make informed decisions about their investments. Whether it's assessing the stock market's historical performance or tracking the volatility of cryptocurrencies, this report serves as a valuable guide to harnessing the potential of data visualization for financial insights.

