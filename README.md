# churn-analysis-ecommerce
Ce projet consiste à évaluer les pratiques contribuant au churn des clients d'une société e-commerce.

## Contexte métier
### Type d’entreprise

Entreprise E-commerce B2C spécialisée dans la vente de produits grand public (mode, accessoires et produits lifestyle) via une plateforme en ligne.

### Problème rencontré

L’entreprise constate une augmentation du taux de churn (clients inactifs ou ne revenant plus acheter), impactant directement :

Le chiffre d’affaires récurrent

Le coût d’acquisition client (CAC)

La rentabilité long terme

L’équipe marketing souhaite comprendre pourquoi les clients partent et identifier les profils à risque afin de mettre en place des actions de rétention ciblées.

## Objectif du projet
### Problématique

Quels sont les facteurs qui influencent le churn client et comment prédire les clients à risque afin de réduire la perte de revenus ?

Objectifs opérationnels

Identifier les variables les plus explicatives du churn

Segmenter les clients selon leur niveau de risque

Proposer des actions concrètes pour améliorer la rétention

## Données utilisées
### Source

Base de données interne de l’entreprise (CRM + historique de commandes).

### Période

Données collectées sur 24 mois d’activité.

### Variables clés

Données démographiques (âge, localisation)

Nombre de commandes

Montant total dépensé

Panier moyen

Fréquence d’achat

Dernière date d’achat

Type de produits achetés

Utilisation de promotions

Service client contacté (oui/non)

Statut churn (variable cible)

## Méthodologie
### 1. Analyse exploratoire (EDA)

Analyse des distributions

Détection des valeurs manquantes et outliers

Analyse des corrélations

Comparaison churn vs non churn

### 2. Feature Engineering

Création de variables RFM (Récence, Fréquence, Montant)

Encodage des variables catégorielles

Normalisation des variables numériques

### 3. Modélisation

Séparation train/test (80/20)

Modèles testés :

Régression logistique

Random Forest

Gradient Boosting

### 4. Évaluation

Accuracy

Precision / Recall

F1-score

ROC-AUC

Importance des variables

## Résultats clés
### Performance du modèle

Le modèle Random Forest obtient les meilleures performances :

Accuracy : 87%

ROC-AUC : 0.91

Recall (churn) : 82%

### Insights majeurs

La récence d’achat est le facteur le plus déterminant.

Les clients ayant effectué moins de 3 commandes ont un risque de churn 2x plus élevé.

Les clients attirés uniquement par les promotions churnent davantage.

Un panier moyen élevé réduit significativement la probabilité de churn.

L’absence d’interaction post-achat (email, fidélité) augmente le risque de départ.

## Recommandations business
### 1. Mettre en place un système d’alertes prédictives

Déployer le modèle en production pour identifier automatiquement les clients à risque et déclencher des campagnes ciblées.

### 2. Lancer un programme de fidélité personnalisé

Offres spécifiques pour les clients à faible fréquence

Récompenses progressives après 3 commandes

### 3. Automatiser des campagnes de réactivation

Email de relance après 60 jours d’inactivité

Code promotionnel limité dans le temps

Recommandations personnalisées basées sur l’historique d’achat

## Stack technique

Python (Pandas, NumPy, Scikit-learn)

Matplotlib / Seaborn

Jupyter Notebook

Git / GitHub

## Impact Business Potentiel

Si le modèle permet de réduire le churn de seulement 5%, cela pourrait générer :

+8 à 12% d’augmentation du revenu annuel

Réduction du coût d’acquisition

Amélioration de la Customer Lifetime Value (CLV)

## Conclusion

Ce projet démontre la capacité à :

Traduire un problème business en problématique data

Construire un pipeline complet d’analyse et de modélisation

Générer des recommandations concrètes et actionnables
