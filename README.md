A hybrid recommender-system project for handling cold‑start in movie recommendations using the MovieLens 20M dataset. We implement:

Content‑Based Filtering (CBF) via the Tag Genome

Collaborative Filtering (CF) via item–item cosine similarity

Hybrid Model that blends CBF + CF

Evaluation (Precision@K, Recall@K, NDCG@K) and parameter tuning

# Repository Structure

```
bash
Copy
Edit
COLDSTARTMOVIE/
├── ml-20m/                        # Raw MovieLens 20M files
│   ├── genome-scores.csv
│   ├── genome-tags.csv
│   ├── links.csv
│   ├── movies.csv
│   ├── ratings.csv
│   └── tags.csv
├── data_processing.ipynb         # Subsetting & building tag‑matrix
├── content_based_filtering.ipynb # CBF pipeline & metrics
├── hybrid_CBF.ipynb              # Hybrid model implementation
├── evaluation.ipynb              # Precision/Recall/NDCG & visualizations
├── predictions/                  # Saved Top-10 recommendation lists
│   ├── cbf_top10_subset.json
│   └── hybrid_top10_subset.json
├── subset_ratings.csv
├── subset_movies.csv
├── subset_links.csv
├── subset_movie_tag_matrix.csv
└── README.md                     # ← You are here
```

# Evaluation

1. Read through what we already had in `evaluation.ipynb`
2. Do Hyper‑Parameter Sweeps A. Hybrid Blend Weight(Change in Parameter) B. CBF Normalization(L2‑norm vs. no normalization vs. MinMax)
3. Ask GPT for any futher evaluation can be done
4. Visualization.
