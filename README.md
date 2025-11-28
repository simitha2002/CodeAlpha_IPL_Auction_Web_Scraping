# 🏏 IPL Auction 2025 - Web Scraping & Data Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)
![CodeAlpha](https://img.shields.io/badge/CodeAlpha-Internship-orange.svg)

**CodeAlpha Data Analytics Internship - Task 1: Web Scraping**

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Key Insights](#key-insights)
- [Challenges & Solutions](#challenges--solutions)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [Contact](#contact)

---

## 🎯 Overview

This project demonstrates **web scraping** techniques by extracting real-time data from the IPL 2025 auction website, performing comprehensive data cleaning and validation, and deriving meaningful insights about team spending patterns and player valuations.

### What This Project Does

✅ Scrapes player auction data from [IPLT20.com ](https://www.iplt20.com/) 

✅ Cleans and validates data (handles duplicates, null values)  

✅ Analyzes team spending patterns  

✅ Identifies most expensive players  

✅ Creates professional visualizations 
  

---

## ✨ Features

### 🌐 Web Scraping
- Automated data extraction from HTML tables
- Handles multiple currency formats (₹27 cr, 2,00,00,000)
- Robust error handling
- Respectful rate limiting

### 🧹 Data Cleaning
- Duplicate detection and removal
- Null value handling
- Data type conversions
- Quality validation reports

### 📊 Data Analysis
- Team-wise spending analysis
- Top 10 most expensive players

### 📈 Visualization
- Professional bar charts
- Customized styling
- Interactive insights

---

## 💻 Technologies Used

| Technology | Purpose |
|-----------|---------|
| **Python 3.8+** | Core programming language |
| **BeautifulSoup4** | HTML parsing and data extraction |
| **Requests** | HTTP requests to fetch web pages |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Data visualization |
| **Jupyter Notebook** | Interactive development environment |

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Jupyter Notebook

### Step 1: Clone the Repository
```bash
git clone https://github.com/simitha2002/CodeAlpha_IPL_Auction_Web_Scraping.git
cd CodeAlpha_IPL_Auction_Web_Scraping
```

### Step 2: Create Virtual Environment (Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 📖 Usage

### Option 1: Run Jupyter Notebook
```bash
jupyter notebook notebooks/ipl_auction_2025_analysis.ipynb
```

Then run all cells sequentially (Cell → Run All)

### Option 2: Quick Start
```python
# Import required libraries
import pandas as pd
import matplotlib.pyplot as plt

# Load cleaned data
df = pd.read_csv('data/ipl_auction_2025_players_cleaned.csv')

# View top 10 expensive players
top_players = df.nlargest(10, 'winning_bid_inr')
print(top_players[['player', 'team', 'winning_bid_raw']])

# Analyze team spending
team_spending = df.groupby('team')['winning_bid_inr'].sum().sort_values(ascending=False)
print(team_spending)
```


## 📁 Project Structure
---

```
CodeAlpha_IPL_Auction_Analysis_Web_Scraping/
│
├── notebooks/
│   └── ipl_auction_2025_analysis.ipynb    # Main analysis notebook
│
├── data/
│   ├── ipl_auction_2025_players (1).csv       # Raw scraped data
│   ├── ipl_auction_2025_players_cleaned.csv  # Cleaned dataset
│   └── ipl_auction_2025_summary (1).json.json      # Summary statistics
│
└── README.md                               # Project documentation
```

---


## 🔍 Key Insights

### 💰 Spending Analysis

- **Highest Spender:** Punjab Kings (₹110.15 Crores)
- **Lowest Spender:** Rajasthan Royals (₹40.70 Crores)

### 💎 Most Expensive Player

- **Player:** Rishabh Pant
- **Winning Bid:** ₹27 Crores
- **Team:** Lucknow Super Giants

---


## 🚧 Challenges & Solutions

### Challenge 1: Duplicate Player Entries

**Problem:** Same player appeared in multiple teams  
**Solution:** Implemented duplicate detection and removal logic using Pandas  

### Challenge 2: Multiple Currency Formats

**Problem:** Data in different formats ("27 cr", "2,00,00,000")  
**Solution:** Created robust `money_to_int()` function with regex  
**Impact:** 100% successful conversion rate

### Challenge 3: Dynamic HTML Structure

**Problem:** Website structure variations  
**Solution:** Used multiple selectors with fallback options  
**Result:** Extracted 202 player records successfully

---

## 🔮 Future Enhancements

- [ ] Add historical comparison (2024 vs 2025 auctions)
- [ ] Implement role-based analysis (batsman, bowler, all-rounder)
- [ ] Create interactive dashboard with Plotly
- [ ] Add automated email reports
- [ ] Include player performance metrics correlation
- [ ] Develop API for data access

---

## 🎓 Learning Outcomes

Through this project, I gained hands-on experience in:

✅ Web scraping with BeautifulSoup  
✅ Data cleaning and validation techniques  
✅ Pandas data manipulation  
✅ Statistical analysis  
✅ Data visualization best practices  
✅ Git version control  
✅ Professional documentation  

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📞 Contact

**[Simitha Ummer]**

- LinkedIn: [linkedin.com/in/simitha-ummer](http://www.linkedin.com/in/simitha-ummer-69a848350)
- GitHub: [github.com/simitha2002](https://github.com/simitha2002)
- Email: simithau@gmail.com

**Project Link:** [https://github.com/simitha2002/CodeAlpha_IPL_Auction_Web_Scraping](https://github.com/yourusername/CodeAlpha_IPL_Auction_Web_Scraping)

---

## 🙏 Acknowledgments

- **CodeAlpha** for the internship opportunity
- **IPLT20** for publicly accessible data
- **Python Community** for excellent libraries and documentation

---

## ⭐ Show Your Support

If you found this project helpful, please give it a ⭐️!

---
