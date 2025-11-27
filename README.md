# AI Trading Advisor: Voice-Driven Technical and News-Based Market Analysis
## Project Overview

This project builds an automated AI trading advisor that processes voice commands, retrieves real-time market data, analyzes news sentiment, and generates actionable trading recommendations. The analysis focuses on multi-timeframe technical patterns, sentiment interpretation, and integrated decision-making for buy, sell, or hold strategies.

## Key Objectives

- Analyze short-term and medium-term price movements across multiple timeframes
- Evaluate sentiment direction based on recent news articles
- Assess combined influence of technical trends and sentiment on trade decisions
- Develop automated, data-driven trading recommendations with entry, stop-loss, and take-profit levels

## Dataset Description

The analysis uses data and inputs collected from:

- Polygon.io candlestick data (5-minute, 15-minute, and 1-hour intervals)
- Polygon.io news data for 7-day sentiment analysis
- Telegram voice messages transcribed using OpenAI Whisper
- LLM-generated summaries and structured outputs
- Automated JSON responses processed through n8n

Note: Due to security and API restrictions, no API keys or environment variables are included in this repository. Please refer to the setup section for configuration details.

## Repository Structure

```
ai-trading-advisor/
├── workflows/
│   └── Day_Trader.json          # Main automation workflow
├── examples/
│   └── sample_output.json       # Example trading output
├── images/                      # Workflow and system diagrams
└── README.md
```

## Key Findings

1.Market Analysis:

- Multi-timeframe price data reveals momentum, volatility, and trend alignment
- Strong signals identified when 5-minute, 15-minute, and 1-hour trends converge

2.Sentiment Interpretation:

- Weekly news summaries help contextualize catalysts and risks

- Sentiment classification provides directional bias for trading decisions

3.Trading Recommendations:

- Automated buy, sell, or hold signals generated using combined model logic
- Entry, stop-loss, and take-profit values computed programmatically

4.Workflow Automation:

- Voice-based pipeline significantly reduces analysis time
- Structured JSON outputs allow seamless integration with future systems

## Technologies Used

- n8n for workflow automation
- OpenAI Whisper and GPT-4.1 models
- Polygon.io APIs for market and news data
- JavaScript for custom logic and extraction
- Telegram Bot API for user interaction


## Getting Started

1.Clone this repository

2.Import the workflow file into n8n

3.Configure required API keys for Polygon.io, OpenAI, and Telegram

4.Send a voice message to the Telegram bot to trigger analysis

5.Example Output


<img width="780" height="414" alt="image" src="https://github.com/user-attachments/assets/db7d7a51-a419-4fbe-8236-3d5f314426f4" />


## License

This project is licensed under the MIT License - see the LICENSE file for details.


