#  Cryptocurrency Analysis with n8n and Groq API
This repository contains an automation workflow using n8n and the Groq API to analyze cryptocurrency market data and send insights via a Telegram bot.
Table of Contents

Project Overview 
Prerequisites
Setup Instructions
Workflow Description
Telegram Bot Integration
Screenshots
Contributing
License
### Workflow Screenshot
![Workflow Screenshot](https://github.com/amir-rs/n8n-Ai-agent/blob/main/Screenshot%202025-06-05%20111157.png)

Project Overview
This project leverages n8n, an open-source workflow automation tool, to fetch real-time cryptocurrency market data (e.g., prices, trends) using a public API (such as CoinGecko or CoinMarketCap). The data is processed and analyzed using the Groq API for generating insights, such as price predictions or market sentiment. The results are then sent to a Telegram bot for user notifications.
Prerequisites
### Telegram Bot Test Screenshot
![Telegram Bot Test Screenshot](https://github.com/amir-rs/n8n-Ai-agent/blob/main/Screenshot%202025-06-05%20111157.png)
n8n: Installed locally or hosted on a server (self-hosted or cloud).
Groq API Key: Obtain from xAI API.
Telegram Bot Token: Create a bot via BotFather on Telegram.
Node.js: For running any custom scripts (optional).
Cryptocurrency API: A free API key from CoinGecko or similar.

Setup Instructions

Clone the Repository:
git clone https://github.com/your-username/crypto-analysis-n8n-groq.git
cd crypto-analysis-n8n-groq


Set Up n8n:

Install n8n locally: npm install -g n8n or use Docker: docker run -it --rm -p 5678:5678 n8n.
Access n8n at http://localhost:5678 and log in.


Configure Groq API:

Add your Groq API key in n8n under Credentials > HTTP Request > Authentication > Header Auth.
Set the header as Authorization: Bearer YOUR_GROQ_API_KEY.


Set Up Telegram Bot:

Create a bot via BotFather and obtain the token.
Add the token to n8n under Credentials > Telegram.


Import Workflow:

Import the provided workflow.json from the workflows directory into n8n.
Configure the nodes with your API keys and Telegram chat ID.


Run the Workflow:

Activate the workflow in n8n to start fetching and analyzing crypto data.



Workflow Description
The n8n workflow automates the following steps:

Schedule Trigger: Runs every hour to fetch data.
HTTP Request Node: Queries a cryptocurrency API (e.g., CoinGecko) for market data (e.g., BTC/USD price).
Groq API Node: Sends data to Groq API for analysis (e.g., trend prediction or sentiment analysis).
Telegram Node: Sends the analysis results to a specified Telegram chat.

See the workflow screenshot below for a visual representation.
Telegram Bot Integration
The Telegram bot receives messages with formatted crypto insights, such as:

Current price of a cryptocurrency.
Predicted price movement based on Groq API analysis.
Market sentiment or alerts for significant changes.

A test message screenshot is provided below.
Screenshots
Workflow Screenshot

Telegram Bot Test Screenshot

Note: Upload the workflow and Telegram bot test screenshots to the images directory in this repository and update the paths above if needed.
Contributing
Contributions are welcome! Please open an issue or submit a pull request with improvements or bug fixes.
License
This project is licensed under the MIT License. See the LICENSE file for details.
