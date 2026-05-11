✈️ Airline Sentiment Analysis - Twitter NLP
Ce projet vise à analyser et classifier automatiquement les sentiments (positif, neutre ou négatif) exprimés par les utilisateurs sur Twitter à l'égard de diverses compagnies aériennes. Le projet couvre l'ensemble du cycle de vie de la donnée : du prétraitement du texte (NLP) à l'entraînement de modèles de Deep Learning.

📝 Objectif
L'objectif principal est de construire un modèle capable de comprendre le langage naturel des tweets pour aider les compagnies aériennes à identifier rapidement l'insatisfaction client et à améliorer leurs services.

📊 Dataset
Le jeu de données contient des tweets adressés à des compagnies aériennes majeures.

Taille : ~14 640 tweets.

Classes : negative, neutral, positive.

Nettoyage : Seuls les tweets avec une confiance de sentiment supérieure à 0.5 ont été conservés pour garantir la qualité de l'apprentissage.

🛠️ Pipeline de Prétraitement
Une attention particulière a été portée à la préparation des données textuelles :

Ingénierie de caractéristiques (Feature Engineering) : Extraction de statistiques comme le nombre de mots, de hashtags, de mentions, d'URLs et de caractères spéciaux.

Nettoyage de texte (NLP) :

Suppression de la ponctuation et des caractères spéciaux.

Mise en minuscule.

Suppression des stopwords (mots vides).

Stemming : Réduction des mots à leur racine pour réduire la dimensionnalité.

Vectorisation : Utilisation de CountVectorizer pour transformer le texte en vecteurs numériques exploitables par les algorithmes.

🤖 Modèles Utilisés
Plusieurs approches ont été testées pour comparer les performances :

Modèles Classiques :

Multinomial Naive Bayes : Un modèle statistique robuste pour la classification de texte.

Logistic Regression : Utilisé comme baseline performante avec une optimisation par GridSearchCV.

Deep Learning :

Réseau de neurones dense (TensorFlow/Keras) : Un modèle multi-couches avec régularisation (Dropout) pour éviter le surapprentissage.

📈 Résultats
Précision Globale : Le modèle de Deep Learning atteint environ 77% d'accuracy sur l'ensemble de test après 5 époques.

Analyse : Les résultats montrent une forte capacité du modèle à identifier les tweets négatifs, qui constituent la majorité du dataset.
