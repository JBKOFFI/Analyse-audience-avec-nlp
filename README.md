# Analyse d'Audience et des Réactions pour un Programme Télé : Cas de Squid Game

## Contexte
Projet réalisé par :  
- Alexandra ANVOH  
- Jean-Baptiste KOFFI  
- Prosper KOUASSI  

L’objectif est d’analyser l’audience et les réactions autour de la série *Squid Game* à partir de commentaires et notes d’internautes (source : [AlloCiné](https://www.allocine.fr/series/ficheserie-29898/critiques/)). Le projet mobilise le Traitement Automatique du Langage Naturel (TALN) pour extraire des insights sur le sentiment et les thèmes dominants.

## Données
- Fichier : `allocine_squidgame_reviews.csv`  
- 918 commentaires, avec les colonnes principales :  
  - `rating` : note attribuée par l’utilisateur  
  - `content` : texte du commentaire  

## Méthodologie
1. **Exploration et préparation des données** : nettoyage des commentaires, gestion des valeurs manquantes, création d’une variable `feeling` (positif / négatif).  
2. **Analyse visuelle** : nuages de mots (positifs, négatifs, adjectifs, verbes) et distribution des sentiments.  
3. **Modélisation** : entraînement de plusieurs modèles de classification de texte :  
   - Multinomial Naive Bayes (accuracy 71.7%)  
   - Random Forest Classifier (accuracy 79.9%) – modèle retenu  
   - XGBoost (accuracy 75%)  
   - Gradient Boosting (accuracy 76%)  
   - BERT (accuracy 67.4%)  

## Résultats
- Majorité des commentaires positifs (≈59%) mais une fraction significative de commentaires critiques.  
- Nuages de mots montrent les termes les plus fréquents, révélant les points forts et critiques de la série.  
- Random Forest Classifier retenu pour ses bonnes performances et sa capacité à prédire le sentiment sur de nouveaux commentaires.

## Conclusion
L’étude combine analyse exploratoire et modèles de NLP pour comprendre les réactions des spectateurs. Elle permet non seulement d’identifier les tendances générales, mais aussi d’automatiser la classification de nouveaux commentaires pour un suivi en temps réel.

## Technologies utilisées
- Python : pandas, numpy, matplotlib, seaborn, nltk, spacy  
- Modèles de ML : scikit-learn, xgboost, transformers (BERT)  
- Traitement NLP : TF-IDF, tokenization, lemmatisation, wordcloud
