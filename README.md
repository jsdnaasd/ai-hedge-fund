<p align="center">
  <img src="assets/quant-agent-hero.svg" alt="AI Hedge Fund hero banner" width="100%" />
</p>

<h1 align="center">AI Hedge Fund</h1>

<p align="center">
  <strong>A multi-agent quant research lab for market analysis, valuation, risk control, and portfolio decisions.</strong>
</p>

<p align="center">
  <a href="https://github.com/jsdnaasd/ai-hedge-fund/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/jsdnaasd/ai-hedge-fund?style=for-the-badge"></a>
  <a href="https://github.com/jsdnaasd/ai-hedge-fund/network/members"><img alt="GitHub forks" src="https://img.shields.io/github/forks/jsdnaasd/ai-hedge-fund?style=for-the-badge"></a>
  <a href="LICENSE"><img alt="MIT License" src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge"></a>
  <img alt="Python" src="https://img.shields.io/badge/Python-Quant%20Agents-3776AB?style=for-the-badge&logo=python&logoColor=white">
</p>

<p align="center">
  <a href="#why-this-project">Why</a> ·
  <a href="#agent-team">Agent Team</a> ·
  <a href="#architecture">Architecture</a> ·
  <a href="#quick-start">Quick Start</a> ·
  <a href="#disclaimer">Disclaimer</a>
</p>

---

## Why This Project

AI Hedge Fund turns the idea of an investment committee into a programmable agent system. Instead of asking one model for a trade, it coordinates specialized agents that analyze fundamentals, valuation, sentiment, technicals, macro-style risk, and portfolio constraints before producing a final decision.

This repository is designed for builders who want to study:

- how LLM agents can be organized into a financial research workflow;
- how valuation, risk, sentiment, and technical signals can be combined;
- how a backtesting layer can turn model outputs into measurable experiments;
- how an AI-native investing interface can be structured without putting an LLM directly on the live order path.

> This is a research and education project, not financial advice and not a live trading system.

## Featured Workflow

<p align="center">
  <img src="assets/agent-workflow.svg" alt="Agent workflow diagram" width="100%" />
</p>

## Agent Team

The system includes a full research desk of specialized agents:

| Layer | Agents | Role |
| --- | --- | --- |
| Legendary investors | Warren Buffett, Charlie Munger, Ben Graham, Peter Lynch, Michael Burry, Mohnish Pabrai, Bill Ackman, Cathie Wood, Stanley Druckenmiller, Phil Fisher, Rakesh Jhunjhunwala, Aswath Damodaran, Nassim Taleb | Different investment philosophies, valuation styles, and risk lenses |
| Signal engines | Valuation, Fundamentals, Sentiment, News Sentiment, Technicals, Growth | Generate interpretable market signals |
| Control layer | Risk Manager, Portfolio Manager | Position sizing, exposure limits, and final decision synthesis |
| Experiment layer | Backtester, Metrics, Benchmarks | Evaluate decisions over historical data |

## Architecture

<p align="center">
  <img src="assets/system-architecture.svg" alt="AI hedge fund architecture" width="100%" />
</p>

The project is structured around a clean research loop:

1. **Data ingestion** loads prices, financial metrics, insider trades, and news.
2. **Agent analysis** converts raw data into structured opinions and signals.
3. **Risk management** constrains exposure before any portfolio action is proposed.
4. **Portfolio synthesis** combines signals into buy, sell, short, cover, or hold decisions.
5. **Backtesting** measures behavior with reproducible historical experiments.

## What Makes It Interesting

- **Multi-agent by design**: different agents represent different investment frameworks instead of one generic chatbot.
- **Risk-aware workflow**: risk and portfolio management are explicit layers.
- **Backtestable outputs**: decisions can be evaluated instead of admired in isolation.
- **Local model support**: optional Ollama flow for running local LLMs.
- **Extensible agent surface**: new investment styles, indicators, and data sources can be added as separate agents.

## Quick Start

### 1. Clone

```bash
git clone https://github.com/jsdnaasd/ai-hedge-fund.git
cd ai-hedge-fund
```

### 2. Configure API Keys

```bash
cp .env.example .env
```

Add at least one LLM provider key:

```bash
OPENAI_API_KEY=your-openai-api-key
FINANCIAL_DATASETS_API_KEY=your-financial-datasets-api-key
```

You can also use other supported providers such as Anthropic, Groq, DeepSeek, or local Ollama models depending on your setup.

### 3. Install

```bash
curl -sSL https://install.python-poetry.org | python3 -
poetry install
```

### 4. Run the Agent Team

```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA
```

Run with local LLMs:

```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA --ollama
```

Run over a specific period:

```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA --start-date 2024-01-01 --end-date 2024-03-01
```

### 5. Backtest

```bash
poetry run python src/backtester.py --ticker AAPL,MSFT,NVDA
```

## Web Application

The repository also includes a web application interface for users who prefer a visual workflow over the CLI. See the application guide in [`app/`](app/) if present in your checkout.

## Roadmap Ideas

- Crypto-native market data adapters
- On-chain wallet and protocol intelligence agents
- Agent memory for recurring market theses
- Strategy leaderboard with reproducible backtests
- Risk dashboards for position-level attribution
- Paper-trading mode with strict human approval

## Disclaimer

This project is for **educational and research purposes only**.

- It is not investment advice.
- It is not intended for live trading.
- It does not guarantee returns.
- Past performance does not imply future results.
- You are responsible for your own research, risk controls, and financial decisions.

## Attribution

This repository is a fork and presentation-enhanced edition of [`virattt/ai-hedge-fund`](https://github.com/virattt/ai-hedge-fund), originally released under the MIT License. The original copyright and license are preserved in this repository.

## License

MIT License. See [`LICENSE`](LICENSE) for details.
