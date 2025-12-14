# Intelligent Stock Analysis Engine

A powerful, AI-driven stock research platform that aggregates data from multiple sources, performs deep analysis using LLMs, and presents actionable insights via a modern dashboard and API.

## 🚀 Key Features

### 📊 Deep Data Integration
- **Real-Time Data**: Live stock prices and volume via SerpApi (Google Finance).
- **Macro Indicators**: Ticker tape tracking Fed Rates, CPI, and Unemployment trends.
- **Inside Info**: "Smart Money Flow" tracking recent insider trading activity.
- **Earnings Analysis**: AI-generated summaries of recent earnings call transcripts.

### 🧠 Advanced AI Capabilities
- **Comprehensive Reports**: Generates detailed investment theses with Buy/Sell/Hold verdicts.
- **Chat with Data**: Interactive "Ask the Analyst" widget for follow-up questions on reports.
- **Scenario Modeling**: Adjust growth rates and margins to see how the AI's verdict changes.

### 💻 User Experience
- **Interactive Dashboard**: Features TradingView charts, financial bar charts, and SWOT grids.
- **User Accounts**: Secure Login/Registration system.
- **Watchlists**: Pin and track your favorite stocks.
- **PDF Export**: Download professional-grade research reports in one click.

### 🔌 Developer Tools
- **REST API**: Programmatic access to analysis via `POST /api/analyze`.

## 🛠️ Tech Stack
- **Backend**: Python, Flask (MVC Architecture)
- **Database**: SQLite, SQLAlchemy
- **AI/LLM**: OpenAI GPT-4
- **Data Sources**: SerpApi (Google Finance, News, Search)
- **Frontend**: HTML5, Bootstrap 5, Vanilla JS, Chart.js
- **Utilities**: WeasyPrint (PDF Generation)

## 📦 Installation

1.  **Clone the repository**:
    ```bash
    git clone <repository_url>
    cd scrapper
    ```

2.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Environment Setup**:
    Create a `.env` file in the root directory:
    ```env
    SERPAPI_API_KEY=your_serpapi_key
    OPENAI_API_KEY=your_openai_key
    SECRET_KEY=your_flask_secret_key
    ```

4.  **Run the Application**:
    ```bash
    python run.py
    ```
    Access the dashboard at `http://127.0.0.1:5000`.

## 🔗 API Usage

**Endpoint**: `/api/analyze`
**Method**: `POST`
**Headers**: `Content-Type: application/json`

**Request Body**:
```json
{
    "query": "AAPL"
}
```

**Response**:
```json
{
    "target": "AAPL",
    "market_price": 150.00,
    "investment_verdict": {
        "signal": "Buy",
        "rationale": "Strong fundamentals..."
    },
    ...
}
```

## 📂 Project Structure
```
/
├── app/
│   ├── controllers/   # Route descriptors (Main, Auth, API)
│   ├── models/        # Database models (User, Watchlist)
│   ├── services/      # Logic (DataFetcher, AIAnalyst)
│   ├── templates/     # HTML Views
│   └── static/        # CSS/JS Assets
├── run.py             # Entry Point
└── requirements.txt
```
