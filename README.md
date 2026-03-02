# Financial Data Telegram Bot

**Telegram bot for retrieving financial market data** via public APIs from MOEX and the Central Bank of Russia (CBR).

The bot provides up-to-date financial information in Telegram: exchange rates, stock quotes, and dividend history.

---

## 🚀 Features

- **Exchange rates** — retrieves current currency rates from the Central Bank API  
- **Stock quotes** — fetches stock prices from the Moscow Exchange (MOEX)  
- **Dividend history** — shows past dividends for a company (if available)  
- All data retrieved from external APIs and formatted for user-friendly display in Telegram.

---

## 🧠 How It Works

- Listens for commands from users via Telegram Bot API  
- Makes HTTP requests to official APIs (CBR and MOEX)  
- Parses and organizes API responses for clear rendering in Telegram  
- Uses local storage (SQLite via Peewee ORM) for managing bot state

---

## 🛠 Tech Stack

- **Python** — core programming language  
- **Aiogram / TeleBot** — Telegram bot frameworks  
- **Requests / asyncio** — for HTTP calls and async logic  
- **SQLite + Peewee** — lightweight storage  
- **Docker + docker-compose** — containerized environment

---

## 🔧 Setup and Run

1. Clone the repository:

```bash
git clone https://github.com/NVLev/stock_exchange-telegram-bot
cd stock_exchange-telegram-bot
```

2.  Create and edit .env with your bot token:
```bash
TELEGRAM_BOT_TOKEN=your_token_here
```
3.  Install Python dependencies:
```bash
pip install -r requirements.txt
```
4. Run locally:
```bash
python bot.py
```
## 📌 Commands
| Command               | Description                                 |
| --------------------- | ------------------------------------------- |
| `/start`              | Shows welcome message                       |
| `/rates`              | Displays current exchange rates             |
| `/quote <TICKER>`     | Shows last available stock price            |
| `/dividends <TICKER>` | Shows dividend history for the given ticker |
