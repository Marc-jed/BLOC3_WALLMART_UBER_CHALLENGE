# 🛒 Projet Walmart – Prédiction des ventes hebdomadaires

## 📌 Contexte

**Walmart Inc.** est l’une des plus grandes chaînes de distribution au monde.
Le service marketing souhaite un outil capable de **prédire les ventes hebdomadaires** de ses magasins afin de mieux anticiper la demande et d’optimiser ses campagnes marketing.

---

## 🎯 Objectifs

* Explorer et analyser les données de ventes hebdomadaires des magasins Walmart
* Préparer et nettoyer les données pour le Machine Learning
* Construire un **modèle de régression linéaire** comme baseline
* Améliorer les performances avec des modèles **régularisés (Ridge, Lasso)** afin de réduire le surapprentissage
* Identifier les variables explicatives les plus influentes

---

## 🛠️ Stack technique

* **Python** (pandas, numpy, matplotlib, seaborn)
* **scikit-learn** :

  * Régression linéaire
  * Régression Ridge et Lasso
  * GridSearchCV pour l’optimisation des hyperparamètres
* **Jupyter Notebook** pour l’expérimentation et la documentation

---

## 🔄 Pipeline analytique

1. **EDA & Prétraitement**

   * Suppression des lignes où la variable cible (`Ventes_Hebdomadaires`) est manquante
   * Création de nouvelles variables à partir de la colonne `Date` : année, mois, jour, jour de la semaine
   * Détection et suppression des valeurs aberrantes (hors de l’intervalle [µ−3σ ; µ+3σ]) pour les colonnes numériques (`Température`, `Prix du carburant`, `IPC`, `Chômage`)
   * Encodage des variables catégorielles (`Store`, `Holiday_Flag`)
   * Standardisation des variables numériques

2. **Modèle baseline : Régression linéaire**

   * Entraînement et évaluation avec **RMSE** et **R²**
   * Analyse des coefficients pour identifier les variables influentes

3. **Régression régularisée**

   * **Ridge** : pénalisation L2 → réduit l’impact des variables collinéaires
   * **Lasso** : pénalisation L1 → supprime les variables les moins pertinentes
   * Optimisation de l’hyperparamètre `alpha` avec GridSearchCV

4. **Comparaison des performances**

   * Régression linéaire vs Ridge vs Lasso
   * Impact de la régularisation sur la précision et la robustesse du modèle

---

## 📊 Résultats principaux

* La **régression linéaire simple** donne un premier modèle correct mais sensible au surapprentissage
* La **régression Ridge** améliore la stabilité du modèle en limitant l’impact des variables corrélées
* La **régression Lasso** permet d’identifier un **sous-ensemble optimal de variables** en éliminant celles moins pertinentes
* Les variables liées au **taux de chômage** et au **prix du carburant** ont un impact significatif sur les ventes

---

## 🚀 Recommandations

* Déployer un modèle **Ridge** ou **Lasso** pour obtenir des prédictions plus robustes
* Mettre en place une surveillance continue du modèle pour adapter les paramètres aux nouvelles données
* Intégrer des données externes (événements économiques, météo, etc.) afin d’améliorer la prédiction des ventes

---

## 👨‍💻 Auteur

Projet réalisé dans le cadre du **Bootcamp Data Fullstack – Jedha**.
Auteur : MARC



