📈 Redstox Analyst: AI-Powered Stock Analysis Platform

**🔴 Live Demo:** [Check out the live application here!](https://redstox-analytics.onrender.com/)

Redstox Analyst is an LLM-driven investment research platform that delivers real-time, multi-dimensional stock insights using fundamental, technical, and sentiment analysis. Built with Streamlit and powered by Llama 3.3 via Groq, it mimics expert investors to provide actionable financial evaluations.

🚀 Features
💼 Fundamental Analysis with Expert Templates
Analyze stocks in the styles of legendary investors like Warren Buffett, Peter Lynch, Ray Dalio, and Cathie Wood. Llama 3.3 generates reports using their unique frameworks and metrics.

📊 Technical Analysis Dashboard
Visualizes indicators like SMA and RSI with interactive Streamlit charts, powered by real-time Yahoo Finance data.

📰 Sentiment Analysis of Financial News
Fetches and classifies news using NewsAPI and Newspaper3k, then summarizes and scores sentiment via Llama 3.3.

🧠 AI-Powered Stock Query System
Ask questions like “Is Apple a good long-term buy?” and get context-aware, analyst-style responses grounded in financial data and LLM reasoning.

📉 Real-Time Data Fetching
Automatically pulls historical and current stock data using yFinance, enabling up-to-date analysis.

🔍 Multi-Layered Investment Insights
Combines price trends, news sentiment, and financial ratios into a single, user-friendly dashboard to aid better investment decisions.



🧱 Tech Stack
Layer	Tools / Technologies
UI	Streamlit
Data APIs	Yahoo Finance (via yfinance), NewsAPI, Newspaper3k
LLM Engine	Llama 3.3 70B via Groq
Backend	Python, Groq SDK
Visualization	Streamlit native charts

## 🏗️ Architecture

The application follows a modular structure where Streamlit handles the frontend interface, and multiple independent Python agents manage data extraction, technical computation, and LLM processing:

1. **Frontend**: Streamlit UI (`ui_components.py`, `main.py`) takes user input and renders analysis.
2. **Data Layer**: 
   - `yfinance` fetches historical stock data (`technical_utils.py`).
   - `NewsAPI` and `newspaper3k` scrape and parse financial news (`sentiment_utils.py`).
3. **AI/LLM Layer**: Data is sent via prompt templates (`agents.py`) to the Llama 3.3 70B model using the Groq API (`analysis_utils.py`).
4. **Integration Layer**: The application synthesizes fundamental, technical, and sentiment results into a cohesive dashboard.

## 🛠️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/manohar1030/redstox-Agentic-AI-StockMarket-Assistant.git
cd "redstox-Agentic-AI-StockMarket-Assistant-main/Redstox Analytics"
```

### 2. Set up the Environment Variables
Create a `.env` file in the root directory and add your API keys:
```env
GROQ_API_KEY=your_groq_api_key_here
NEWS_API_KEY=your_newsapi_key_here
```

### 3. Install Dependencies
It's recommended to use a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
pip install -r requirements.txt
```

### 4. Run the Application
```bash
streamlit run main.py
```
```

🖼️ Sample Outputs
![Sample Output 1](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778240914/Screenshot_2026-05-08_171819_a4wzk7.png)




![Sample Output 2](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778240991/Screenshot_2026-05-08_171939_vfegvq.png)




![Sample Output 3](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778241054/Screenshot_2026-05-08_172043_ibwpex.png)




![Sample Output 4](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778241133/Screenshot_2026-05-08_172152_a6u0gt.png)




![Sample Output 5](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778241194/Screenshot_2026-05-08_172303_m1mjvc.png)




![Sample Output 6](https://res.cloudinary.com/dp8wy3ooi/image/upload/v1778241225/Screenshot_2026-05-08_172334_sp2vsi.png)
