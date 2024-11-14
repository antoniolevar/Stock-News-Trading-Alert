Stock News Alert Project
This project is a Python-based script that monitors stock price changes and sends alerts with relevant news articles using the Twilio API. When a stock price increases or decreases by a defined percentage threshold, the program fetches recent news related to the stock and sends alerts via SMS.

Project Overview
The script performs the following actions:

Stock Price Monitoring: Using the Alpha Vantage API, the program retrieves the latest daily closing stock prices for a specified stock.
Percentage Change Calculation: If there is a significant price change (greater than the defined threshold), the program triggers a news search.
News Retrieval: Using the News API, the script fetches relevant news articles related to the stock's company.
SMS Notification: The program sends SMS alerts with the article titles and descriptions using the Twilio API.
Prerequisites
Python 3.x installed on your machine.
Twilio Account for SMS capabilities. Set up your Twilio SID and Auth Token.
Alpha Vantage API Key for retrieving stock prices.
News API Key for fetching the latest news articles.

Setup Instructions
Clone or Download the Repository:
git clone https://github.com/your-username/stock-news-alert.git

Install Required Libraries: Install requests and twilio using pip:
pip install requests twilio

Create and Configure API Keys:

Sign up for Alpha Vantage and NewsAPI to get your API keys.
Sign up for Twilio and obtain your Account SID, Auth Token, and a Twilio virtual number.
Set Up Environment Variables Update the placeholder variables in the script with your keys:

STOCK_API_KEY, NEWS_API_KEY, TWILIO_SID, and TWILIO_AUTH_TOKEN.
Run the Script:
python stock_news_alert.py

Script Breakdown
STEP 1: Fetches the stock's closing price for the last two days and calculates the percentage change.
STEP 2: If the price change exceeds the defined threshold, it fetches the latest news articles using the News API.
STEP 3: Sends SMS alerts for each news article using Twilio.
Example Output
When the stock price change exceeds the threshold, the SMS alert includes:

Stock symbol and percentage change.
Headline and brief description of each news article.
Example SMS:
TSLA: 🔺5%
Headline: Tesla expands production. 
Brief: Tesla Inc. announced new factories in Asia...
Disclaimer
API Rate Limits: The free tiers of Alpha Vantage and News API have rate limits. To avoid hitting these limits, you may consider adjusting the frequency of API calls or upgrading to a paid plan.
Privacy: Ensure that sensitive information, like API keys and phone numbers, is kept secure. Do not commit these details to a public repository.
License
This project is licensed under the MIT License.
