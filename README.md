# Spatial Transcriptomics Brain Analysis (Scanpy Mini-Project)

## Compétences techniques mobilisées

| Domaine | Outils & Méthodes |
|--------|-------------------|
| Analyse transcriptomique spatiale | Scanpy, AnnData, capture areas |
| Pré-traitement | Filtrage spots, PCA, normalisation, HVGs |
| Réduction de dimension | UMAP, t-SNE |
| Clustering | Graph k-NN, Leiden |
| Analyse différentielles | Test de Wilcoxon |
| Visualisations biologiques | Expression génique in situ, heatmaps, UMAP colorés |

---

## Contexte

Ce mini-projet constitue une vitrine de compétences en **analyse de données de transcriptomique spatiale** appliquée au cerveau, en utilisant **Scanpy** dans un environnement Python.  
Les données proviennent de l’étude de *Yu et al., 2023* (bioRxiv, doi:10.1101/2023.11.01.565161), portant sur les effets de la **greffe de cellules souches neurales humaines (hNSC)** dans un modèle murin **5XFAD** de la maladie d’Alzheimer.  
L’objectif de la publication est d’étudier, à l’échelle spatiale, comment la transplantation cellulaire module l’expression génique cérébrale dans différentes **zones anatomiques** et **conditions expérimentales** (*WT*, *5XFAD*, *Vehicle*, *hNSC*).

Ici, le but est de reproduire un **workflow complet et structuré**, depuis l’importation des données brutes (*10X Genomics Visium*) jusqu’à l’identification de signatures moléculaires spécifiques aux **régions corticales**, aux **phénotypes pathologiques**, et à l’impact de la **transplantation thérapeutique**.

---

## Structure du dépôt

- `st_5xfad_scanpy_miniproject.ipynb` → Notebook d’analyse (commenté et reproductible)
- `data/` → Données d’entrée (AnnData / matrices brutes)
- `figures/` → Visualisations générées (UMAP, distribution génique, cartes spatiales)

---

## Pipeline d’analyse

1. **Chargement des données spatiales** (*AnnData .h5ad* ou `filtered_feature_bc_matrix`)
2. **Filtrage par zone anatomique / “capture_area”**
3. **Contrôle qualité** (taux MT, ribosomal, Hb…)
4. **Normalisation & détection des gènes hautement variables (HVGs)**
5. **Réduction de dimension (PCA ↦ UMAP)**
6. **Construction du graphe k-NN & clustering Leiden**
7. **Analyse différentielle** par cluster et par condition
8. **Visualisations spatialisées** des gènes d’intérêt

---

## Résultats

- Séparation nette des **zones corticales vs subcorticales** sur les projections UMAP.
- Mise en évidence d’un patron d’expression génique.
- Cartographie spatiale fine de gènes comme *GFAP*, *MBP*, *TREM2*, révélant des signatures typiques de la **microglie réactive**.
- Identification de clusters distincts reflétant des populations **neurales et gliales** différentes selon les contextes (*WT*, pathologie, traitement cellulaire).

---

## Objectif du projet

Ce dépôt vise à illustrer ma capacité à :

- mettre en œuvre un **workflow analytique robuste** sur données omiques spatialisées,
- **interpréter biologiquement** les patterns observés dans un cadre neuro-dégénératif,
- produire des **figures claires et exploitables** pour un rapport scientifique ou portfolio.

---

## 📬 Contact

*Adam Boussif — Master 2 Bioinformatique (Université Claude Bernard Lyon 1)*  
**Mail :** adam.boussif@etu.univ-lyon1.fr | **GitHub :** `adboussif`
