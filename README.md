# Fantasy Basketball Analytics Engine 🏀 📊

A data engineering pipeline and analytics tool built to identify high-value NBA players for fantasy basketball leagues. This tool automates the retrieval of live statistics, normalizes performance using Z-Scores, and allows for dynamic "punt strategy" analysis.

## 🚀 Key Features

* **Automated Data Pipeline:** Fetches real-time player statistics using the [NBA API](https://github.com/swar/nba_api).
* **Custom Z-Score Algorithm:** Normalizes stats across 8 categories (PTS, REB, AST, STL, BLK, 3PM, FG%, FT%) to compare players on a single scale.
* **Dynamic "Punt" Analysis:** Allows users to exclude specific categories (e.g., "Punt Blocks") to recalculate rankings instantly based on team build.
* **SQL Persistence:** Warehouses historical data in a local SQLite database (`fantasy_history.db`) to track player value trends over time.

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Data Analysis:** Pandas, NumPy
* **Database:** SQLite3
* **API:** `nba_api` (National Basketball Association API)

## 📦 Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/fantasy-analytics.git](https://github.com/YOUR_USERNAME/fantasy-analytics.git)
    cd fantasy-analytics
    ```

2.  **Install dependencies**
    ```bash
    pip install pandas nba_api
    ```

## 💻 Usage

### 1. Run the Ranking Engine
This script fetches the last 7 days of data, calculates Z-Scores, and saves the top players to the database.

```bash
python main.py
