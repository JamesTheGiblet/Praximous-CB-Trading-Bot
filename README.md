## **Project: Trading Bot - Concept 1**
A Notification Bot for Manual Crypto Trading

#### **The Problem**

Trading crypto is noisy. You're either staring at charts all day or you're missing opportunities. Most of the market movement is just noise, and it's hard to stick to a disciplined strategy when you're making emotional decisions.

---
#### **The Solution**

A simple bot that watches the market for me and sends a notification when specific, pre-defined conditions are met.

**This is critical:** This first version **does not trade for you.** It's a notification engine. Its only job is to tell me when to look at the charts, based on a simple set of rules. This lets me validate the strategy with my own eyes before ever letting a line of code touch real money.

---
#### **The Strategy (The Rules)**

The logic is simple and rule-based. No machine learning, no magic.

* **What It Watches:** **BTC** and the next **4 biggest cryptocurrencies** by market cap, trading against USDT. The list of the top 4 is updated dynamically.
* **Rules for BTC (Buy-Only):**
    * It sends a "Buy Alert" when BTC drops **-5%** from a recent high.
    * That's it. We don't sell BTC, we just accumulate on dips.
* **Rules for Altcoins (Buy/Sell/Stop-Loss):**
    * **Buy Alert:** Price drops **-5%** from a recent high.
    * **Sell Alert (Take Profit):** Price rises **+5%** from my last buy price.
    * **Sell Alert (Stop-Loss):** Price drops **-25%** below my last buy price.
* **The "Skim" Rule (Profit Allocation):**
    * When an altcoin trade closes for a +5% gain, **10% of that profit is skimmed off** and put into a virtual "investment fund."
    * When the bot sends a "Buy Alert" for BTC, it will also notify me of the amount sitting in this fund, suggesting it's a good time to invest it.

---
#### **How It's Built (The Architecture)**

The system has three main parts:
1.  **Data Fetcher:** Connects to the **Coinbase Pro API** to get real-time price data.
2.  **Strategy Engine:** The core logic that checks the price data against the rules defined above.
3.  **Notifier:** The user-facing part (CLI and GUI) that sends the alerts.

**The Tech Stack:**
* **Platform:** Coinbase
* **Language:** Python (it's great for APIs and data)
* **Database:** SQLite (for local data logging, nothing fancy)

---
#### **The Testing Plan**

**Sandbox first. Always.**
* All development and testing will happen in the Coinbase sandbox environment.
* My main testing method will be to record a live data stream for a few hours, then replay it into the bot to see if it generates the alerts I expect.
* **Log everything.** Every price check, every trigger, every alert. The logs will be the proof of whether this strategy works or not.

---
#### **The Important Details**

* **UI:** It will have both a simple **CLI** to run in a terminal and a **GUI** dashboard to see current prices, a feed of alerts, and the balance of the "investment fund."
* **Security:** The API key will be stored in a `.env` file (which will be in `.gitignore`) and will have trade-only permissions.
* **Error Handling:** The bot needs to handle API connection errors gracefully with smart retries and clear logging. It will also have a "kill switch."
* **Performance Tracking:** The GUI will track basic KPIs: Net Profit/Loss (from simulated trades), Win Rate, and Average Hold Time.
* **The Fine Print (Legal & Disclaimers):** The UI and all docs will have a huge, blinking sign that says: "**This is a technical tool, not financial advice. You are responsible for your own trades, taxes, and losses.**"

This is about building a disciplined, data-driven tool to see if a simple strategy has an edge. **The code is the proof**, and in this case, the logs will show if the strategy has legs. Let's build it and see.
