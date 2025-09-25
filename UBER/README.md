# 🚖 Projet UBER – Détection des zones chaudes à New York

## 📌 Contexte

Uber est une des plus grandes plateformes mondiales de transport.
Un problème récurrent est l’**indisponibilité des chauffeurs dans certaines zones** au moment où les clients en ont besoin.
L’objectif de ce projet est de construire un algorithme permettant d’identifier les **zones chaudes** (hotspots) de la ville de **New York**, afin de recommander aux chauffeurs où se positionner pour réduire le temps d’attente des passagers.

---

## 🎯 Objectifs

* Analyser les données de trajets Uber à New York
* Appliquer des **algorithmes de clustering** pour détecter les zones de forte demande
* Comparer différents modèles non supervisés (**KMeans** et **DBSCAN**)
* Visualiser les résultats sur une carte interactive (Plotly)

---

## 🛠️ Stack technique

* **Python** (pandas, numpy, scikit-learn, matplotlib, seaborn, plotly)
* **Algorithmes de clustering** :

  * KMeans (partitionnement par centroïdes)
  * DBSCAN (clustering par densité)
* **Visualisation** : cartes interactives avec Plotly

---

## 🔄 Pipeline analytique

1. **EDA (Exploration des données)**

   * Analyse des pick-up par jour et par heure
   * Distribution géographique des points de départ

2. **Clustering**

   * **KMeans** : choix du nombre de clusters via la méthode du coude & score silhouette
   * **DBSCAN** : ajustement des paramètres (`eps`, `min_samples`) pour détecter les zones denses et identifier les outliers

3. **Comparaison des modèles**

   * KMeans : rapide, robuste, tous les points sont affectés à un cluster
   * DBSCAN : meilleure détection des anomalies, mais sensible aux hyperparamètres

4. **Visualisation**

   * Carte des clusters par algorithme
   * Comparaison des zones chaudes détectées par KMeans vs DBSCAN

---

## 📊 Résultats principaux

* **KMeans** capte efficacement les zones de forte demande et offre une **interprétation simple via les centroïdes**
* **DBSCAN** identifie mieux les anomalies (outliers) mais produit parfois des clusters instables selon le réglage
* Conclusion : **KMeans est privilégié** car il est plus lisible, rapide et exploitable opérationnellement pour Uber

---

## 🚀 Recommandations

* Utiliser KMeans en production pour fournir une **recommandation en temps réel aux chauffeurs**
* Ajuster les clusters par **tranches horaires** afin d’adapter les zones chaudes selon l’heure de la journée
* Étendre l’analyse à d’autres villes après validation à New York

---

## 👨‍💻 Auteur

Projet réalisé dans le cadre du **Bootcamp Data Fullstack – Jedha**.
Auteur : MARC


