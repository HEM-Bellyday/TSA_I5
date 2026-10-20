# TP1 — Time Series Analysis (TSA)

Practical work 1 for the **Time Series Analysis** course at the Institute of Technology of Cambodia (ITC-AMS-FIE).
All code is written in **R** inside a **Quarto** document (`.qmd`), so the analysis, code and results are reproduced together in one rendered report.

> Reference: J. D. Cryer & K.-S. Chan, *Time Series Analysis: With Applications in R* (2nd ed.), Springer.

---

## Objectives

- Load and explore time series datasets in R (`ts` objects, frequency, start/end).
- Visualize series with time plots and lag plots to identify trend, seasonality and dependence.
- Simulate basic stochastic processes: **white noise**, **random walk**, **moving average**.
- Compute and interpret the **sample autocorrelation function (ACF)**.
- <add or remove objectives to match the TP statement>

---

## Repository structure

```
TP1/
├── TP1.qmd     # The whole TP: R code, explanations and results
└── README.md
```

Everything lives in `TP1.qmd`. Datasets are loaded directly from R packages (e.g. `TSA`), so no separate data files are needed. The rendered report (`TP1.html` or `TP1.pdf`) is generated when you render the file.

---

## Requirements

- **R** ≥ 4.2
- **Quarto CLI** ≥ 1.3 — <https://quarto.org/docs/get-started/>
- **RStudio** or **VS Code** with the Quarto extension (optional, for editing)

R packages:

```r
install.packages(c("TSA", "forecast", "ggplot2", "tseries", "knitr", "rmarkdown"))
```

| Package    | Used for                                            |
|------------|-----------------------------------------------------|
| `TSA`      | Datasets and functions from Cryer & Chan            |
| `forecast` | `autoplot`, `ggAcf`, utility functions              |
| `ggplot2`  | Plotting                                            |
| `tseries`  | Stationarity tests (e.g. `adf.test`)                |
| `knitr`, `rmarkdown` | Rendering R chunks in Quarto              |

---

## How to run

**Render the full report from the terminal:**

```bash
quarto render TP1.qmd            # HTML (default)
quarto render TP1.qmd --to pdf   # PDF (requires a LaTeX distribution, e.g. TinyTeX)
```

**Live preview while editing:**

```bash
quarto preview TP1.qmd
```

**In RStudio:** open `TP1.qmd` and click **Render** (or `Ctrl/Cmd + Shift + K`). Individual chunks can be run with `Ctrl/Cmd + Enter`.

If PDF output fails, install TinyTeX once:

```bash
quarto install tinytex
```

---

## Contents of `TP1.qmd`

| Section | Description |
|---------|-------------|
| 1. Setup | Load packages, set seed (`set.seed()`) for reproducibility |
| 2. Data exploration | Load datasets (e.g. `data(larain)`, `data(color)`), inspect and plot them |
| 3. Simulation | Generate white noise and a random walk; compare their behavior |
| 4. Autocorrelation | Plot and interpret sample ACFs |
| 5. Conclusion | Summary of findings |

<update the table to match the actual sections of your document>

---

## Reproducibility

- A fixed random seed is set at the top of the document so simulated series are identical on every render.
- Rendering the `.qmd` regenerates every figure and table; no results are hard-coded.

---

## Author

**HEM Bellyday** — Year 4, Financial Engineering (ITC-AMS-FIE)
Course: Time Series Analysis — <lecturer name>
Date: <submission date>
