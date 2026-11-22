# ERA5 – De la ressource à la production et au risque (Maurice)

Travail pratique du **Master 2 Énergie (ENERGY-Lab, Université de La Réunion)**, réalisé seul.

## Objectif
Exploiter les réanalyses **ERA5** pour caractériser la ressource renouvelable sur le site de **Maurice**, passer de la ressource à une estimation de production, puis discuter du risque associé.

## Contenu
| Fichier | Description |
|---|---|
| [`ERA5_Maurice.ipynb`](ERA5_Maurice.ipynb) | Notebook Python : chargement des données NetCDF, traitements, figures |
| [`rapport_TP2_ERA5.pdf`](rapport_TP2_ERA5.pdf) | Rapport de 3 pages : 3 figures commentées (observation et interprétation) |

## Méthode
1. Lecture des fichiers ERA5 (NetCDF) avec **xarray**
2. Extraction des séries au point de grille du site, mise en forme avec **pandas**
3. Passage de la ressource à la production
4. Cartes saisonnières (Matplotlib, Cartopy), facteur de charge PV, P50/P90 et coefficient de variation interannuel

## Lancer le notebook
```bash
pip install numpy pandas xarray netCDF4 matplotlib cartopy jupyter
jupyter notebook ERA5_Maurice.ipynb
```
Les données ERA5 ne sont pas incluses (trop volumineuses) : elles se téléchargent sur le [Copernicus Climate Data Store](https://cds.climate.copernicus.eu/).

## Auteur
Nicolas NOYON – nicolasnoyon.pro@gmail.com
