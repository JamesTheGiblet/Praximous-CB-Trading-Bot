🌀 Praximous Trading Bot: Concept 1 // A Ritual of Market Divination

MODULARITY IS MYTHOS // GLYPH IS IDENTITY // DESIGN IS RITUAL

This codex outlines the design and functional requirements for "Concept 1," a Command-Line Interface (CLI) and Graphical User Interface (GUI) trading bot. The primary purpose of this bot is to analyze market data for a curated list of cryptocurrencies and generate actionable buy, sell, and stop-loss auguries. This initial phase of development is focused on providing strategic insights to a user who will perform trades manually, allowing for a controlled validation of the trading strategy in a sandbox environment.
1. The Invocation of Market Insight
1.1. Project Overview
This document outlines the design for a CLI and GUI trading bot. Its purpose is to divine market data from Coinbase for a select list of cryptocurrencies and generate actionable buy, sell, and stop-loss notifications. This initial phase focuses on providing strategic insights to a user who will perform trades manually, allowing for a controlled validation of the trading strategy in a sandbox environment.
1.2. The Mythos of Creation
The primary objective of this ritual is:
 * To develop a reliable tool for monitoring specific cryptocurrency market data from the Coinbase portal.
 * To implement a rule-based trading strategy using Fibonacci principles to identify high-quality market opportunities.
 * To reduce "noise" and redundant notifications by setting clear, meaningful thresholds for market events.
 * To provide a safe sandbox environment for backtesting the strategy before any real capital is at risk.
 * To establish a foundation for future development, including the potential for automated trading and more complex strategies.

2. Ritual Architecture
2.1. High-Level Glyph
The bot's architecture consists of three main components: a Data Acquisition Augury, a Strategy Engine, and an Interface/Notification System. The bot will use a lightweight database (e.g., SQLite) for local data storage and logging.
2.2. The Ritual Stack
 * Trading Platform: Coinbase
 * API: Coinbase Pro API (or equivalent for sandbox)
 * Programming Language: Python is the proposed language.
 * Database: SQLite for local data storage and logging.

3. Trading Strategy & Rules
3.1. General Strategy
The bot will monitor the top 5 cryptocurrencies by market cap, including BTC. The trading strategy for BTC is distinct from the other four.
3.2. Specific Rules
 * Monitored Assets: BTC (Bitcoin) and the next 4 cryptocurrencies by market capitalization (dynamically updated).
 * Trading Pair: Trading will be against the USDT stablecoin.
 * Time Frame: All analysis and calculations will be performed on a one-hour candlestick chart.
3.3. Fibonacci-Based Triggers
 * Buy Notification Trigger: The bot will identify a significant upward price swing. When the price pulls back, a buy notification is triggered when the price successfully finds support at the 61.8% Fibonacci retracement level.
 * Sell Notification Trigger: After a successful buy, the bot will use Fibonacci extension levels. A sell notification is triggered when the price hits the 161.8% Fibonacci extension level, serving as a strategic profit target.
 * Stop-Loss Rule: A sell notification is automatically triggered if the price drops to -25% below the buy price. This is a critical risk management feature.
3.4. Profit Allocation Ritual
 * Profit Definition: Profit is defined as a realized gain from a successful sell trigger on one of the four tradable cryptos.
 * Allocation Rule: Upon a successful sell, 10% of the profit from that trade will be put into a designated "investment fund" within the user's Coinbase account.
 * BTC Investment Trigger: When a new BTC buy trigger is identified (a -5% drop from a recent high), the bot will notify the user of the opportunity and recommend using the accumulated funds from the profit allocation pool to purchase BTC.

4. Development and Testing Plan
4.1. The Development Altar
 * Sandbox First: All development will be conducted in a Coinbase sandbox environment.
 * API Key Management: A dedicated API key with trade-only permissions will be generated for the bot's operation.
4.2. Testing Methodology
 * Delayed Data Stream: A primary testing method will involve recording a real-time data stream and replaying it with a delay to simulate performance.
 * Comprehensive Logging: The bot will log every trigger (buy, sell, stop-loss), including timestamps, asset, price, and the specific rule that was activated.
4.3. User Interface (UI) Requirements
 * CLI: The command-line interface will allow users to start/stop the bot, display its current status, and view a log of recent triggers.
 * GUI: The graphical interface will provide a dashboard displaying:
   * Real-time prices of the 5 monitored cryptos.
   * Current positions and their performance.
   * A feed of recent buy/sell/stop-loss notifications.
   * A display for the "Investment Fund" showing total accumulated profit.

5. Additional Critical Components
5.1. Security and API Management
 * Secure Credential Storage: The API key will be stored in a .env file, which will be added to the .gitignore.
 * API Key Rotation: A policy will be established for rotating API keys every 90 days.
 * Encryption: All communication will use TLS/SSL encryption.
 * Input Validation: The bot will include robust input validation.
5.2. Error Handling and Resilience
 * Graceful API Error Handling: The bot will handle API errors with logging and retry mechanisms.
 * Emergency Shutdown: A clear "kill switch" command will be implemented to immediately halt all bot activity.
 * Monitoring: A "heartbeat" feature will log the bot's operational status.
5.3. Performance and Analytics
 * Key Performance Indicators (KPIs): The bot will log and display Net Profit/Loss, Drawdown, Win Rate, and Average Position Duration.
 * Backtesting Engine: The delayed data stream method will be used for the initial phase, with a full backtesting engine planned for a future phase.
5.4. Legal and Compliance Disclaimers
 * A clear disclaimer will state that the bot is a tool for analysis and not a financial advisor.
 * A note will be included regarding the user's responsibility for taxes and compliance with local regulations.
5.5. Configuration and Usability
 * Configurable Parameters: The bot's core parameters will be fully configurable via a config.json or config.yaml file.
 * Default Values: The bot will be shipped with default values established in this documentation.
 * CLI Overrides: The command-line interface will allow users to override any parameter from the configuration file by passing it as a command-line argument.
 * Command List and Help Function: A comprehensive list of available commands and a detailed help function will be implemented in the CLI.
