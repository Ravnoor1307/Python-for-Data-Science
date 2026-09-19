# Data for the Plotly sales explorer

Raw data is deliberately not committed to this repository. Download it from the links below into this folder, then run the notebooks.

| Dataset | Source |
| --- | --- |
| Superstore retail sales | [https://www.kaggle.com/datasets/vivek468/superstore-dataset-final](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) |
| Zomato Bangalore Restaurants | [https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants) |

## Expected layout

```text
data/
  raw/        # downloaded files, git-ignored
  processed/  # outputs of the preprocessing notebook
```

## Reproducibility notes

- Record the download date and file hash in your notes; public datasets change.
- Never edit a raw file in place. Write derived files to `processed/`.
- If a link breaks, search the dataset name on Kaggle or the UCI repository.

The notebook generates synthetic sales data so it runs offline. Swap in the Superstore CSV to work with real records.
