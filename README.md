# 420-C74-SF — Techniques d'apprentissage automatique

Ateliers (travaux pratiques) du cours **420-C74-SF**, programme *Spécialiste en solutions d'intelligence artificielle*.

## Organisation du dépôt

| Répertoire | Contenu |
|---|---|
| `nbs/` | Ateliers, un répertoire par chapitre (énoncé + version `-solution`) |
| `data/` | Jeux de données, référencés depuis les notebooks par `../../data/` |
| `evals/` | Évaluations, examens et projets |
| `materials/` | Diapositives des chapitres (PDF) |
| `docker/` | Image de l'environnement de travail |
| `.devcontainer/` | Configuration Dev Container (VS Code) |

## Chapitres et ateliers

| # | Chapitre | Atelier |
|---|---|---|
| 01 | Introduction à l'apprentissage automatique | — |
| 02 | Régression linéaire simple | `nbs/02-regression-lineaire-simple/` |
| 03 | Algorithme du gradient | `nbs/03-algorithme-gradient/` |
| 04 | Régression linéaire multiple et polynomiale | `nbs/04-regression-lineaire-multiple/` |
| 05 | Équation normale | `nbs/05-equation-normale/` |
| 06 | Métriques et évaluation des modèles de régression | `nbs/06-metriques/` |
| 07 | Régression logistique | `nbs/07-regression-logistique/` |
| 08 | Variables qualitatives | `nbs/08-variables-qualitatives/` |
| 09 | Introduction à scikit-learn | `nbs/09-intro-scikit-learn/` *(à venir)* |
| 10 | Dilemme biais-variance | `nbs/10-dilemme-biais-variance/` *(à venir)* |
| 11 | Validation croisée | `nbs/11-validation-croisee/` |
| 12 | Techniques de régularisation | `nbs/12-regularisation/` |
| 13 | Algorithme des K plus proches voisins | `nbs/13-algorithme-knn/` |
| 14 | Arbres de décision | `nbs/14-arbres-de-decision/` |
| 15 | Bagging, forêts aléatoires et boosting | `nbs/15-bagging-forets-aleatoires-boosting/` |
| 16 | Machines à vecteurs de support | `nbs/16-svm/` |
| 17 | Métriques et évaluation des modèles de classification | `nbs/17-evaluation-models-classification/` |
| 18 | Optimisation des hyperparamètres | `nbs/18-optimisation-des-hyperparametres-101/` |
| 19 | Apprentissage ensembliste | `nbs/19-ensembles/` |
| 20 | Introduction au partitionnement de données | — |
| 21 | Partitionnement en K-moyennes | `nbs/21-partitionnement-k-moyennes/` |
| 22 | Regroupement hiérarchique | `nbs/22-regroupement-hierarchique/` |
| 23 | Validation du partitionnement | `nbs/23-validation-partitionnement/` |
| 24 | DBSCAN et HDBSCAN | `nbs/24-dbscan/` |
| 25 | Considérations pratiques sur le partitionnement | — |
| 26 | Méthodes de partitionnement avancées | — |
| 27 | Partitionnement : exemples d'application | — |
| 28 | Analyse en composantes principales | — |
| 29 | t-SNE | — |
| 30 | Algorithme des plus proches voisins | `nbs/30-recherche-documents/` |
| 31 | Métriques de distance | — |
| 32 | Locality-Sensitive Hashing | `nbs/32-locality-sensitive-hashing/` |
| 33 | Algorithme Apriori et règles d'association | `nbs/33-regles-association/` |
| 34 | Détection d'anomalies | — |
| 35 | Modèles de mélange (Gaussian Mixture Models) | — |

## Environnement de travail

Python 3.13 ; les versions des bibliothèques sont épinglées dans
[docker/requirements.txt](docker/requirements.txt).

### Avec VS Code (recommandé)

Ouvrir le dépôt dans VS Code, puis **Reopen in Container** : le Dev Container construit l'image
et installe les extensions Python / Jupyter.

### Avec Docker seul

Depuis la racine du dépôt :

```bash
docker build -t 420-c74-sf docker/
docker run --rm -it -p 8888:8888 -v $(pwd):/notebooks 420-c74-sf
```

Puis ouvrir http://localhost:8888. Voir [docker/README.md](docker/README.md) pour les détails.
