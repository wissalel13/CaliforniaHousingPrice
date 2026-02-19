# 🏠 California Housing Price Prediction

Projet de Machine Learning end-to-end pour prédire le prix médian des maisons par quartier en Californie, en utilisant le dataset California Housing issu du recensement américain de 1990.

---

## 📊 Dataset

- **Source** : `sklearn.datasets.fetch_california_housing`
- **Taille** : 20 640 observations, 8 features numériques
- **Cible** : `median_price` — prix médian en centaines de milliers de dollars

| Feature | Description |
|---|---|
| `MedInc` | Revenu médian du quartier |
| `HouseAge` | Âge médian des maisons |
| `AveRooms` | Nombre moyen de pièces par ménage |
| `AveBedrms` | Nombre moyen de chambres par ménage |
| `Population` | Population du block group |
| `AveOccup` | Nombre moyen d'occupants par ménage |
| `Latitude` / `Longitude` | Localisation géographique |

---

## 🔁 Pipeline

1. **Chargement** des données via scikit-learn
2. **Exploration** — statistiques descriptives, analyse des corrélations
3. **Préparation** — séparation features/target, train/test split (80/20, `random_state=45`)
4. **Entraînement** — pipelines avec `StandardScaler` + modèle
5. **Évaluation** — MSE et R² sur le jeu de test
6. **Prédiction** — test sur nouvelles données
7. **Sérialisation** — export avec `pickle`

---

## 🤖 Modèles & Résultats

| Modèle | MSE | R² |
|---|---|---|
| Linear Regression | 0.5209 | 0.607 |
| Ridge + GridSearchCV (cv=5) | 0.5209 | 0.608 |

> La Ridge Regression, avec optimisation de l'hyperparamètre `alpha` sur une grille log-uniforme (10⁻³ à 10³), offre une légère amélioration tout en régularisant le modèle.

---

## 🗂️ Structure du projet

```
.
├── notebook.ipynb       # Exploration, entraînement et évaluation
├── lin_pipeline.pkl     # Pipeline sérialisée (scaler + modèle)
└── README.md
```

---

## ⚙️ Installation

```bash
pip install scikit-learn pandas numpy matplotlib
```

---

## 🛠️ Stack

`Python 3.12` · `scikit-learn` · `pandas` · `NumPy` · `Matplotlib` · `Google Colab`

---
