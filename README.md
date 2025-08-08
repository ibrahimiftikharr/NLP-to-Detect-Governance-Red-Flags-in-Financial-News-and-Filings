# FinWatchdog – A Framework for Detecting Governance Red Flags in Financial Texts  

**Author:** Muhammad Ibrahim  
**Affiliation:** Department of Computer Science, COMSATS University Islamabad  
**Email:** fa22-bcs-062@comsats.edu.pk  

## Overview  
**FinWatchdog** is a Natural Language Processing (NLP) framework designed to identify governance-related anomalies—such as fraud, mismanagement, and regulatory breaches—within unstructured financial text sources, including news articles and regulatory filings.  

The system employs:  
- **FinBERT embeddings** for domain-specific text representation  
- **UMAP** for dimensionality reduction  
- **HDBSCAN** for density-based clustering  

This approach enables the detection of thematic patterns without reliance on hardcoded keywords or predefined taxonomies.  

---

## Key Features  
- **Domain-Specific Text Representation**: Utilizes FinBERT to capture nuanced financial language semantics.  
- **Unsupervised Learning Approach**: Applies HDBSCAN to discover clusters of varying densities and automatically identify outliers.  
- **Dimensionality Reduction**: Leverages UMAP to generate interpretable low-dimensional projections of high-dimensional embeddings.  
- **Interpretability**: Implements TF-IDF to extract salient keywords for each cluster, facilitating thematic understanding.  
- **Comprehensive Evaluation**: Incorporates silhouette score, cosine similarity, and keyword coherence metrics.  
- **Fully Automated Pipeline**: End-to-end process from dataset loading to visualization, reproducible in Google Colab.  

---

## Methodology  
1. **Data Acquisition and Preprocessing**  
   - Dataset: **NIFTY-LM** (financial news).  
   - Cleaning: duplicate removal, stop word elimination, normalization.  

2. **Embedding Generation**  
   - FinBERT ([CLS] token) produces 768-dimensional embeddings.  

3. **Dimensionality Reduction**  
   - UMAP projects embeddings into 2D/3D space for improved clustering and interpretability.  

4. **Clustering**  
   - HDBSCAN identifies semantically coherent clusters and flags outliers.  

5. **Interpretation & Evaluation**  
   - TF-IDF to extract representative keywords per cluster.  
   - Evaluation metrics:  
     - Silhouette score: **0.83** (HDBSCAN) vs. **0.31** (KMeans baseline)  
     - Keyword coherence  
     - Cosine similarity matrices  

@article{ibrahim2025finwatchdog,
  title={Leveraging NLP to Detect Governance Red Flags in Financial News and Filings},
  author={Muhammad Ibrahim},
  year={2025}
}
