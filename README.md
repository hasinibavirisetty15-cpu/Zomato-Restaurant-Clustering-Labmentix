# Zomato Restaurant Clustering and Sentiment Analysis

This project combines restaurant metadata and customer reviews to explore restaurant characteristics, analyze review sentiment, compare unsupervised clustering methods, and summarize business implications.

## Project files

Keep these files together in one folder:

- `Zomato_Restaurant_Clustering_Labmentix.ipynb` — executable notebook
- `Zomato Restaurant names and Metadata.csv` — restaurant metadata
- `Zomato Restaurant reviews.csv` — customer reviews
- `Zomato_Restaurant_Clustering_Report.pdf` — formatted project report

The notebook searches its current folder and an `outputs` subfolder for the datasets.

## Run locally

Use Python 3.10 or newer. Install the notebook dependencies, then open the notebook in Jupyter and choose **Restart Kernel and Run All**.

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn scipy vaderSentiment jupyter
jupyter notebook Zomato_Restaurant_Clustering_Labmentix.ipynb
```

The delivered notebook includes saved outputs and charts from a complete run with the two supplied CSV files. All 56 code cells completed successfully: the run loaded 10,000 review rows and 105 metadata rows, matched 100 restaurants, and completed the charts, sentiment analysis, hypothesis tests, and clustering comparisons. It selected K=3 from the tested candidate values, with a silhouette score of 0.4673 and cluster sizes 24 / 74 / 2. Choose **Restart Kernel and Run All** to recalculate outputs in your environment.

## Interpreting the clusters

K-Means does not balance cluster sizes. The two-restaurant cluster is a small, distinct profile in this sample, not evidence of a broad market segment. The final run uses only the three original input features and reports a 24 / 74 / 2 split. A prior exploratory rerun included earlier cluster labels by mistake; that leakage has been removed. Treat the smallest group as exploratory and validate it with more data before making business decisions.

## Limitations

- The restaurant-level clustering dataset contains 100 matched restaurants.
- Review count is close to constant for most restaurants and contributes limited separation.
- DBSCAN metrics exclude points labeled as noise and therefore are not directly comparable with metrics calculated over all observations.
- VADER may not interpret sarcasm, mixed-language writing, or local expressions accurately.
- These analyses describe associations in the supplied data; they do not establish causation or predict business outcomes.

## Repository

[GitHub repository](https://github.com/hasinibavirisetty15-cpu/Zomato-Restaurant-Clustering-Labmentix)

## Video presentation

[Watch the project presentation](https://drive.google.com/file/d/1MH-p1jvdEL5eyrj9_YGB6KJKWB1R4KWW/view?usp=sharing)
