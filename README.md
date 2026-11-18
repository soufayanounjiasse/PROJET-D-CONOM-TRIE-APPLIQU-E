# Projet d'économétrie appliquée — Consommation d'énergie et rénovation thermique

Université Paris 1 Panthéon-Sorbonne · Sorbonne Data Analytics · 2026-2027
Travail en binôme · Rendu le **10 décembre 2026** : rapport écrit + présentation PPTX + notebook Python.

## Structure du dépôt

```
data/raw/          Données brutes (jamais modifiées)
data/processed/    Données nettoyées produites par les notebooks
notebooks/         Notebooks Python, un par bloc de tâches
outputs/figures/   Graphiques exportés
outputs/tables/    Tableaux exportés (CSV)
docs/              Énoncé (PDF/tex) et diagramme de Gantt
```

## Installation

```bash
python -m venv .venv
source .venv/bin/activate        # Windows : .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Les notebooks utilisent des chemins relatifs : ils s'exécutent depuis `notebooks/` ou depuis la racine.

## Organisation du travail (voir `docs/Gantt_projet_econometrie.xlsx`)

| Tâche | Contenu | Responsable | Statut |
|---|---|---|---|
| A1 | 1.1 Nettoyage de la feuille Logements | Membre 1 | Fait — `notebooks/01_nettoyage.ipynb` |
| A2 | 5.2 Préparation de la série mensuelle | Membre 2 | À faire |
| A3 | 1.2 Statistiques descriptives | Membre 1 | À faire |
| A4 | 1.3 Corrélations, rénové / non rénové | Membre 2 | À faire |

## Conventions Git

- Branche `main` : toujours exécutable. Une branche par tâche (`a1-nettoyage`, `a2-serie-mensuelle`, …), fusionnée ensuite.
- Un notebook = un responsable à la fois, pour éviter les conflits de fusion.
- Tous les notebooks lisent `data/processed/logements_propres.csv` (produit par A1) ; ne jamais modifier `data/raw/`.
- Avant chaque `git push` : `git pull --rebase`.
