# Multilingual Corpus with Lexical, Syntactic, and Semantic Features

**Author:** Shunxin Yao  
**Affiliation:** Queensland University of Technology, Brisbane, Australia  
**Contact:** n12012416@qut.edu.au  
**Date:** 2026-10-03  
**Version:** 1.0

---

## 1. Description

This dataset contains 1,860 Wikipedia articles across five languages:

- English (391)
- Chinese (329)
- Spanish (384)
- French (384)
- German (372)

Each document is accompanied by:

- Lexical features (TTR, MTLD, entropy, hapax ratio)
- Syntactic features (mean dependency distance, tree height, POS and dependency distributions)
- Semantic features (LaBSE document embeddings, 768 dimensions)

The dataset is designed for reproducible cross-linguistic comparison and can be reused for typological, computational, and quantitative linguistic research.

---

## 2. File Structure

```text
.
├── data/
│   ├── corpus_meta_v6.csv
│   ├── corpus_text_v6.csv
│   ├── features_vocab_clean.parquet
│   ├── features_syntax_clean.parquet
│   ├── features_embed.parquet
│   ├── analysis_df.parquet
│   ├── embed_matrix.rds
│   └── mixed_model_results.csv
├── code/
│   ├── extract_features.py
│   ├── 01_prepare.R
│   ├── 02b_permanova_terms.R
│   ├── 03_cluster_mds.R
│   ├── 04_mantel.R
│   ├── 05_mixed_models.R
│   └── 06_all_figures.R
├── figures/
│   ├── fig_length_boxplot.png
│   ├── fig_distance_heatmap.png
│   ├── fig_pca.png
│   ├── fig_mds_language.png
│   ├── fig_dendrogram.png
│   ├── fig_silhouette.png
│   ├── fig_mantel_scatter.png
│   └── fig_mixed_forest.png
├── README.md
├── data_dictionary.md
├── LICENSE
├── LICENSE-CODE
└── LICENSE-DATA
