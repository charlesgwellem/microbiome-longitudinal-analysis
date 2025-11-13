# Microbiome Longitudinal Analysis (Healthy vs T1D vs T2D)

Short, reproducible R analysis exploring microbiome differences across Healthy, Type 1 Diabetes (T1D), and Type 2 Diabetes (T2D).

## What’s inside
- **notebooks/script.Rmd** – end-to-end analysis (alpha/beta diversity, PCoA/NMDS, heatmaps, DESeq2, exports)
- **data/raw/** – original input (kept read-only)
- **data/processed/** – derived CSVs used for plots/results
- **results/figures/** – publication-ready images
- **results/tables/** – exported result tables (CSV/XLSX)

## Methods (high level)
- **Data**: Kraken2 → BIOM → `phyloseq`
- **Alpha diversity**: Observed, Chao1, Shannon
- **Beta diversity**: Bray–Curtis dissimilarity → NMDS & PCoA
- **Taxonomy**: Top phyla/genera bars, top-species heatmap
- **Differential abundance**: `DESeq2` (e.g., T2D vs Healthy), volcano plots
- **Exports**: Figures (PNG), tables (CSV/XLSX)

## Quickstart
1. **Requirements**: R ≥ 4.2, R packages:
   `tidyverse`, `phyloseq`, `vegan`, `ape`, `data.table`, `ggplot2`,
   `pheatmap`, `DESeq2`, `ggpubr`, `openxlsx`
2. Open `notebooks/script.Rmd` in RStudio and knit to HTML.
3. Outputs will be written under `results/`.

> Tip: to freeze package versions, initialize [`renv`](https://rstudio.github.io/renv/):
> ```r
> install.packages("renv"); renv::init(); renv::snapshot()
> ```

## Repo tree
````

Microbiome/
├─ notebooks/
│  └─ script.Rmd
├─ data/
│  ├─ raw/
│  └─ processed/
├─ results/
│  ├─ figures/
│  └─ tables/
├─ docs/
├─ Microbiome.Rproj
├─ .gitignore
└─ LICENSE

```


## Example figures
- `results/figures/longitudinal_plot_selected_taxon.png`
- `results/figures/pcoa_taxa_abundances_longitudinal.png`

## Reuse
- Open to reuse with attribution. See [LICENSE](./LICENSE).

## Contact
Maintainer: **Charles** — [charlesgwellem@yahoo.fr]
