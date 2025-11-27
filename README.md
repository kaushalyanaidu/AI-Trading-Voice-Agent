### AI Trading Advisor (Voice-Powered)

End-to-End Automated Trading Analysis Using n8n, OpenAI \& Polygon.io



#### Overview



This project is an AI-powered trading advisor that converts a voice request into a full trading decision.



The system automatically:



Extracts the stock ticker from your voice



Fetches multi-timeframe price data



Analyzes news sentiment



Combines technical + fundamental signals



Outputs BUY / SELL / HOLD with entry, stop-loss, and take-profit



All orchestrated using n8n, OpenAI, and Telegram.



##### Key Features



Voice-Based Input via Telegram



Automated Ticker Extraction (company names + regex logic)



Multi-Timeframe Market Data (5m, 15m, 1h candles)



7-Day News Scraping \& Sentiment Analysis



Dual-Agent System



Outlook Agent → news sentiment



Trading Agent → recommendation



Structured Output to Telegram



Fully automated E2E pipeline (no manual steps)



##### Data Sources



1\. Polygon.io



Price data (5m, 15m, 1h)



Ticker news (last 7 days)



2\. OpenAI



Whisper for transcription



GPT-4.1 mini for reasoning



Structured JSON output



3\. Telegram Bot API



Voice input



Final output delivery



##### Architecture



###### A simplified view of the workflow:



Voice Message → Whisper STT → Ticker Extraction → 

&nbsp;  ├─ 5m Market Data  

&nbsp;  ├─ 15m Market Data  

&nbsp;  ├─ 1h Market Data  

&nbsp;  └─ News (7 days)  

→ Outlook Agent (Sentiment)  

→ Trading Agent (Decision)  

→ Telegram Message (Final Output)



##### How the AI Works

###### 

###### Outlook Agent



Analyzes news for:



sentiment



themes



catalysts



risks



Outputs:



{ "ticker": "TSLA", "sentiment": "positive", "summary": "..." }



###### Trading Agent



Combines technical + sentiment data and outputs:



{

&nbsp; "recommendation": "buy",

&nbsp; "entry\_point": 218.4,

&nbsp; "stop\_loss": 209.0,

&nbsp; "take\_profit": 235.5,

&nbsp; "justification": "..."

}



###### Tech Stack



n8n – workflow orchestration



OpenAI Whisper – speech-to-text



GPT-4.1 mini – decision engine



Polygon.io – market data + news



JavaScript – ticker extraction \& logic



Telegram Bot API – user interface





##### How to Run Locally

1. &nbsp;Clone the Repository

   git clone https://github.com/kaushalyanaidu/ai-trading-advisor.git
   cd ai-trading-advisor
   
2. Import Workflow

   Upload Day Trader.json into n8n:

   Settings → Import → Select File
   
3. Add Credentials

   OpenAI API Key
   Polygon.io Key
   Telegram Bot Token
   
4. Start Workflow



Speak to your bot:



“Analyze NVDA for me.”



Example Output:


<img width="741" height="400" alt="image" src="https://github.com/user-attachments/assets/c8faf149-efda-486d-b7ba-4bcdbf31f794" />


##### 

##### Future Improvements



* Portfolio-based recommendations
* Backtesting engine
* Confidence scores
* Custom risk profile options
* Dashboard for trade history

