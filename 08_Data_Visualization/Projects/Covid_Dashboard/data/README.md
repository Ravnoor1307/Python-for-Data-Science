# Data for the Covid dashboard

Raw data is deliberately not committed to this repository. Download it from the links below into this folder, then run the notebooks.

| Dataset | Source |
| --- | --- |
| Covid-19 time series | [https://github.com/CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19) |

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

The notebook generates a synthetic stand-in so it runs offline. Replace the loader cell with a read of the real CSV once downloaded.
