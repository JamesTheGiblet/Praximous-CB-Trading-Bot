🪙 Praximous Trading Bot: Concept 1
A Ritual of Market Divination  
MODULARITY IS MYTHOS · GLYPH IS IDENTITY · DESIGN IS RITUAL

This codex outlines the design and functional blueprint for “Concept 1,” a Command-Line Interface (CLI) and Graphical User Interface (GUI) trading bot that channels actionable market auguries via curated cryptocurrency data streams. This first phase offers strategic insight only—manual execution ensures validation before automation.

---

🔮 1. Invocation of Market Insight

1.1. Project Overview
- CLI + GUI trading bot for analyzing market data from Coinbase.
- Monitors a curated asset list and delivers buy, sell, and stop-loss notifications.
- Manual trade execution in a sandbox environment to ensure strategic integrity.

1.2. The Mythos of Creation
- Reliable portal for cryptocurrency market surveillance.  
- Rule-based trading logic inspired by Fibonacci principles.  
- Notification system tuned to eliminate noise and redundant triggers.  
- Safe backtesting sandbox prior to live deployment.  
- Foundation for future evolution into autonomous trading.

---

⚙️ 2. Ritual Architecture

2.1. High-Level Glyph
Core components:
- Data Acquisition Augury
- Strategic Engine
- Notification Interface

Local data storage via SQLite ensures resilience and traceability.

2.2. Ritual Stack
| Layer | Tool |
|-------|------|
| Trading Platform | Coinbase |
| API | Coinbase Pro API |
| Language | Python |
| Database | SQLite |

---

📈 3. Strategic Divination

3.1. Monitored Assets
- Top 5 cryptocurrencies by market capitalization (dynamic).  
- BTC trades with distinct logic, compared to others.  
- All trades measured against USDT.

3.2. Time Frame
- One-hour candlestick analysis.

3.3. Fibonacci Triggers
| Event | Condition |
|-------|-----------|
| Buy Trigger | Price finds support at 61.8% retracement after upward swing. |
| Sell Trigger | Price hits 161.8% Fibonacci extension post-buy. |
| Stop-Loss | Trigger at -25% below buy price. |

3.4. Profit Allocation Ritual
- 10% of realized profits feed into an internal investment fund.  
- BTC “Buy Opportunity” alerts triggered at -5% from recent high.  
- Fund used to reinforce BTC positions.

---

🧪 4. Development Altar

4.1. Environment
- Sandbox deployment using trade-only API key.

4.2. Testing Methodology
- Simulated delayed data stream for time-travel backtesting.  
- Full logging of each trigger with timestamp, asset, price, and rule origin.

4.3. User Interface Ritual

CLI Features
- Start/stop commands  
- Status display  
- Trigger log

GUI Features
- Real-time asset prices  
- Position performance  
- Notification feed  
- Investment fund overview

---

🔐 5. Critical Components

5.1. Security Glyphs
- .env for secure credential storage (excluded via .gitignore).  
- 90-day API key rotation policy.  
- TLS/SSL encrypted communication.  
- Robust input validation.

5.2. Resilience & Error Handling
- Graceful retry logic on API failure  
- Emergency “kill switch” command  
- Heartbeat status monitor

5.3. Performance Metrics
- Net Profit/Loss  
- Drawdown  
- Win Rate  
- Average Position Duration  
- (⚡️ Suggested enhancement: Integrate KPI dashboard into GUI phase)

5.4. Legal Disclaimers
- “Tool for insight, not advisory” disclaimer  
- Tax responsibility & local compliance reminder

5.5. Configurability
- config.yaml for core parameter config  
- CLI override support for all settings  
- Built-in help command and command list

---

🌕 6. Recommended Enhancements

📜 Ritual Chronicle
- Add roadmap.md to track prophecy milestones and lunar cycles of development.  
- Include contributor lore scroll for portal expansion.

👁 Modular Contributor Signals
- Label core modules as glyphs in codebase:  
  - data_augury.py  
  - fibonacci_glyph.py  
  - notification_ritual.py  
- Add architecture diagram: ASCII sigil or SVG glyph representation.

🧭 Expanded Testing Framework
- Future addition: Full backtesting engine with strategy toggles and replay modes.  
- Optional integration: Real-time anomaly detection for unusual market activity.

---
