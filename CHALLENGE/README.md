# 📩 Challenge – Prédiction du taux de conversion

## 📌 Contexte

Le site **DataScienceWeekly** souhaite mieux comprendre le comportement de ses visiteurs et prédire la probabilité qu’un utilisateur s’abonne à sa **newsletter**.
Un **défi d’apprentissage automatique** a été organisé, inspiré des compétitions Kaggle, afin de construire le meilleur modèle de prédiction.

---

## 🎯 Objectifs

* Analyser les données d’utilisateurs fournies (`data_train.csv` et `data_test.csv`)
* Mettre en place une EDA pour comprendre les variables et leur impact potentiel
* Entraîner plusieurs modèles de machine learning et comparer leurs performances
* Optimiser le meilleur modèle en maximisant le **F1-score**
* Soumettre les prédictions sur l’ensemble test pour classement

---

## 🛠️ Stack technique

* **Python** (pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost)
* **Jupyter Notebook** pour l’expérimentation et la documentation
* **Kaggle-like leaderboard** pour comparer les modèles

---

## 🔄 Pipeline analytique

1. **EDA & prétraitement**

   * Nettoyage des données et gestion des valeurs manquantes
   * Encodage des variables catégorielles
   * Standardisation des variables numériques
   * Analyse des corrélations

2. **Modèles entraînés**

   * **Régression logistique (baseline)**
   * **Arbre de décision**
   * **XGBoost Classifier**

3. **Optimisation**

   * Recherche d’hyperparamètres (`GridSearchCV`)
   * Comparaison des scores sur jeu d’entraînement et de test

4. **Évaluation**

   * **Matrice de confusion**
   * **Précision, Recall, F1-score**
   * Sélection du meilleur modèle (XGBoost dans notre cas)

---

## 📊 Résultats principaux

* Le **modèle baseline** (logistique simple) fournit un bon point de départ mais reste limité
* L’**arbre de décision** capte mieux les interactions mais souffre d’overfitting
* Le **XGBoost Classifier** obtient le **meilleur F1-score (~96%)**, équilibrant précision et rappel
* Les variables les plus influentes sont liées au **comportement utilisateur** sur le site

---

## 🚀 Recommandations

* Mettre en avant les **caractéristiques clés des utilisateurs** identifiées par le modèle (ex. durée de session, nombre de pages vues)
* Déployer le modèle pour scorer les nouveaux visiteurs en temps réel
* Expérimenter d’autres modèles avancés (LightGBM, Random Forest) pour affiner les prédictions

---


## 👨‍💻 Auteur

Projet réalisé dans le cadre du **Bootcamp Data Fullstack – Jedha**.
Auteur : MARC

---

