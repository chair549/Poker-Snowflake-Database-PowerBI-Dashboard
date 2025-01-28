# 🎲 Poker Data Dashboard – Snowflake & Power BI

## Overview

This project demonstrates how to **store, manipulate, and analyze poker gameplay data using Snowflake** as the data warehouse and **Power BI** for visualization.

### Key Technologies:

- **❄️ Snowflake** – Cloud-based SQL database for data storage & processing
- **📊 Power BI** – Interactive dashboard for data insights
- **🌟 SQL** – Data extraction & transformation
- **🛠 Data Modeling** – Structuring & optimizing poker data for analysis

## Features

- ✅ **Snowflake-powered data warehouse** for scalable storage and processing
- ✅ **Power BI dashboard** for real-time poker game insights
- ✅ **Win Rate Analysis** – Determines hand strength based on hole cards
- ✅ **Player Behavior Tracking** – Flop action distribution (check, call, raise, etc.)
- ✅ **Game Trends & Player Activity** – Track engagement over time

---

## 📁 Project Structure

### 1️⃣ **Snowflake Database & Data Generation**

- **📝 `CreatingPokerSchemaDatabase.txt`**
  - Defines the **Snowflake database schema**
  - Uses **Snowflake’s GENERATOR function** to **populate tables with random poker game data**
  - Tables include:
    - **Players** – Player profiles, winnings, and skill levels
    - **Games** – Poker stakes, blinds, and ante settings
    - **Hands** – Game outcomes, pot sizes, and winners
    - **PlayerHands** – Individual player hole cards & winnings
    - **Actions** – Player decisions (fold, bet, all-in, etc.)
    - **CommunityCards** – Flop, turn, and river cards

### 2️⃣ **Data Manipulation in Snowflake**
❌ **The randomly generated data falls victim to all the typical issues and biases that come with synthetic data. Some of these issues and challenges are listed below**
- Lack of Real-World Variability – Synthetic data often lacks the complexity and nuances of real-world data, making it less representative of actual scenarios.
- Data Quality & Validation – Unlike real-world data, synthetic data requires rigorous validation to ensure it reflects realistic patterns and distributions.
- Bias Introduction – If the data generation process is not carefully designed, biases can be unintentionally introduced, leading to misleading analysis or model outcomes.

✔️ **This Data Manipulation file aims to minimise and amend some of these issues with randomly generated synthetic data**

- **📝 `DataManipulation.txt`**
  - Adjusts **win rates dynamically based on hole cards**
  - Ensures **realistic action frequency** (e.g., fewer all-ins on the flop)
  - **Optimizes query performance** using **temporary tables and indexing**

### 3️⃣ **SQL Queries for Power BI**

- **📝 `SQLqueriesPowerBI.txt`**
  - Queries used to extract insights into Power BI, including:
    - **Win rate by hole card category**
    - **Player actions by street (flop, turn, river)**
    - **Total players and hands played**
    - **Active players trend over time**

### 4️⃣ **Power BI Dashboard**

- **🎨 `DashboardPreview.JPG`** – Preview of the **Power BI report**
- **📊 `PokerGraphWinrateByCard.pbix`** – Power BI file with interactive visualizations

---

## 🛠️ How It Works

1️⃣ **Create the Snowflake Database:**

- Run `CreatingPokerSchemaDatabase.txt` in **Snowflake** to set up tables and populate data.

2️⃣ **Process & Clean Data in Snowflake:**

- Use `DataManipulation.txt` to refine win rates and standardize action frequency.

3️⃣ **Extract Data for Power BI:**

- Run `SQLqueriesPowerBI.txt` to fetch structured data for visualization.

4️⃣ **Analyze in Power BI:**

- Load `PokerGraphWinrateByCard.pbix` in **Power BI** to explore trends and player behaviours.

---

## 📌 Key Insights

-🔹 **Aces (19.6%) and Kings (11.0%) have the highest win rates**
-🔹 **Most common action on the flop: CHECK (26.09%)**
-🔹 **All-in moves are rare, occurring <5% of the time**
-🔹 **Player trends fluctuate daily, peaking mid-year**

---

## 🚀 Future Improvements

-🔹 **Machine Learning Model** – Predict player strategies using Snowflake ML integration
-🔹 **Real-Time Data Streaming** – Use **Snowflake Snowpipe** to analyze live poker hands
-🔹 **Multi-Table Tournament Analysis** – Expand beyond cash games

---

## 📩 Contact

For questions or collaboration, feel free to reach out! 🚀

