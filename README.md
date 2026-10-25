# Data Analysis Notebooks

Jupyter notebooks from my early data work with pandas, SQL and APIs.

| Notebook | What it does |
| --- | --- |
| [`student-performance-analysis/StudentsAnalysis.ipynb`](student-performance-analysis/StudentsAnalysis.ipynb) | Exploratory analysis of the UCI Student Performance (maths) dataset with pandas: loading the data, summary statistics and missing-value checks. `data/Key Features.pdf` describes the dataset's attributes. |
| [`twitter-scraper/Scraper.ipynb`](twitter-scraper/Scraper.ipynb) | Looks up a Twitter/X user through the API with `tweepy`, then stores their profile and public metrics (followers, following, tweet count) in a SQL Server table through SQLAlchemy, skipping users already saved. |

## Running

```bash
python -m venv .venv
.venv\Scripts\activate          # macOS/Linux: source .venv/bin/activate
pip install jupyter pandas numpy tweepy sqlalchemy pyodbc python-dotenv
jupyter notebook
```

The Twitter notebook reads its settings from a `.env` file next to it (see [`twitter-scraper/.env.example`](twitter-scraper/.env.example)). It connects to SQL Server with Windows authentication through ODBC Driver 17.

## Data

The student dataset is from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance) (Cortez & Silva, 2008), licensed CC BY 4.0.
