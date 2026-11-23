# ERA5 – De la ressource à la production et au risque (Maurice)

Travail pratique du **Master 2 Énergie (ENERGY-Lab, Université de La Réunion)**, réalisé seul.

## Objectif
Exploiter les réanalyses **ERA5** pour caractériser la ressource renouvelable sur le site de **Maurice**, passer de la ressource à une estimation de production, puis discuter du risque associé.

## Contenu
| Fichier | Description |
|---|---|
| [`ERA5_Maurice.ipynb`](ERA5_Maurice.ipynb) | Notebook Python : chargement des données NetCDF, traitements, figures |
| [`rapport_TP2_ERA5.pdf`](rapport_TP2_ERA5.pdf) | Rapport de 3 pages : 3 figures commentées (observation et interprétation) |

## Données
Les données utilisées sont dans le dossier [`data/`](data/) (moyennes mensuelles ERA5, format NetCDF) :

| Fichier(s) | Variable | Période |
|---|---|---|
| `ws100_mon_1991.nc` … `ws100_mon_2020.nc` (30 fichiers) | Vitesse du vent à 100 m | 1991–2020 |
| `mon_sl_ssrd_1979-2001.nc`, `mon_sl_ssrd_2002-2024.nc` | Rayonnement solaire descendant en surface (ssrd) | 1979–2024 |
| `mon_sl_t2m_1979-2001.nc`, `mon_sl_t2m_2002-2024.nc` | Température à 2 m (t2m) | 1979–2024 |
| `mon_sl_lsm_2000.nc` | Masque terre-mer (lsm) | 2000 |

**Source et licence :** Generated using Copernicus Climate Change Service information [2026]. Ni la Commission européenne ni l'ECMWF ne sont responsables de l'usage qui est fait de ces données.
Référence : Hersbach, H. et al. (2023). *ERA5 monthly averaged data on single levels from 1940 to present.* Copernicus Climate Change Service (C3S) Climate Data Store. DOI : [10.24381/cds.f17050d7](https://doi.org/10.24381/cds.f17050d7)

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
Dans le notebook, faire pointer la variable `DATA` vers le dossier [`data/`](data/).

## Auteur
Nicolas NOYON – nicolasnoyon.pro@gmail.com
