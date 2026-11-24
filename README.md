# Zomato Restaurant Clustering and Sentiment Analysis

This project combines restaurant metadata and customer reviews to explore restaurant characteristics, analyze review sentiment, compare unsupervised clustering methods, and summarize business implications.

## Project files

Keep these files together in one folder:

- `Zomato_Restaurant_Clustering_Labmentix.ipynb` — executable notebook
- `Zomato Restaurant names and Metadata.csv` — restaurant metadata
- `Zomato Restaurant reviews.csv` — customer reviews

The notebook searches its current folder and an `outputs` subfolder for the datasets.

## Run locally

Use Python 3.10 or newer. Install the notebook dependencies, then open the notebook in Jupyter and choose **Restart Kernel and Run All**.

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn scipy vaderSentiment jupyter
jupyter notebook Zomato_Restaurant_Clustering_Labmentix.ipynb
```

The notebook was run end to end with the two supplied CSV files. It loaded 10,000 review rows and 105 metadata rows, matched 100 restaurants, completed the charts, sentiment analysis, hypothesis tests, and clustering comparisons, and selected K=3 from the tested candidate values using silhouette score. The corrected run reports silhouette score 0.4673 and final cluster sizes 24 / 74 / 2. Re-run the notebook to recalculate outputs for your environment.

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


