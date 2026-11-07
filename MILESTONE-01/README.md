# IMDb Movies Analysis

**Milestone 1 – CIE:** Data Transformation, Null Value Handling, Insight Generation and Visualization using Python and Pandas.

## Overview
This project analyses an IMDb movies dataset (4,916 movies, 28 columns) with Pandas and Matplotlib. It covers reading a CSV file, understanding the data, transforming it, filling null values with **mean imputation**, generating insights and plotting them.

## Files
| File | Description |
|---|---|
| `movies_analysis.ipynb` | Python notebook with all the code, outputs, charts and insights |
| `imdb_movies.csv` | Dataset used for the analysis |
| `requirements.txt` | Libraries needed |

## Steps followed
1. **Dataset reading** – `pd.read_csv()`
2. **Data understanding** – `shape`, `info()`, `describe()`, duplicates
3. **Data transformation** – cleaned titles, dropped 8 unneeded columns, renamed columns, added `primary_genre`, `num_genres`, `score_category`
4. **Null values** – found 2,093 nulls with `isnull()`; numeric columns filled with the **column mean**, text columns with `"Unknown"`
5. **Insights** – 10 insights using `groupby`, `value_counts`, `corr`, `pd.cut`
6. **Visualization** – line, bar and scatter charts with Matplotlib

## Key findings
* Movies per year grew from about 28 (1980s) to about 206 (2000s); peak in 2009.
* Average IMDb score falls from 7.40 (1960s) to 6.25 (2010s).
* Most common genres: Comedy, Action, Drama; best rated: Documentary, Biography, Crime.
* Animation and Adventure are the most profitable genres.
* Budget and gross correlate at 0.64, but only 56.9% of USA movies made a profit.
* G-rated movies earn the most; longer movies score higher.

## How to run
```
pip install -r requirements.txt
jupyter notebook movies_analysis.ipynb
```
Keep `imdb_movies.csv` in the same folder as the notebook.
