# 🧠 NLP Sentiment Analysis : LSTM vs Transformers (CamemBERT)

Ce dépôt contient un projet complet d'analyse de sentiment (Natural Language Processing) implémentant et comparant deux architectures de Deep Learning avec PyTorch. Le projet explore l'évolution des techniques de NLP, d'un modèle récurrent classique (LSTM) jusqu'à l'état de l'art avec les Transformers (CamemBERT).

Ce projet a été développé dans le cadre du cursus d'ingénierie en Intelligence Artificielle à l'ESAIP.

## 🚀 Fonctionnalités et Approches

Le projet est divisé en deux expérimentations distinctes :

### 1. Approche "From Scratch" (LSTM)
* **Dataset :** Avis utilisateurs de l'application ChatGPT (Google Play Store).
* **Technique :** Sous-échantillonnage (Undersampling) pour équilibrer les classes (Positif, Négatif, Neutre), nettoyage textuel, et création d'un vocabulaire sur-mesure.
* **Architecture :** Modèle PyTorch intégrant une couche d'`Embedding`, suivie d'un réseau `LSTM` bidirectionnel, et d'une couche de classification linéaire (MLP).
* **Performance :** ~98.4% de précision sur le jeu de test anglophone.

### 2. État de l'Art et Transfer Learning (CamemBERT)
* **Dataset :** Critiques de films francophones (Allociné).
* **Technique :** Utilisation de l'écosystème Hugging Face (`datasets`, `transformers`) pour une tokenisation dynamique et optimisée.
* **Architecture :** Fine-tuning du modèle pré-entraîné `camembert-base` (développé par l'Inria et Meta) sur une tâche de classification binaire.
* **Performance :** ~92.6% de précision sur le jeu de test francophone, avec une forte capacité à comprendre les nuances et le contexte.

## 🛠️ Stack Technique

* **Langage :** Python 3
* **Deep Learning :** PyTorch, Hugging Face Transformers
* **Data Science :** Pandas, NumPy, Scikit-learn
* **Visualisation :** Matplotlib

## 📂 Structure du Projet

```text
📦 NLP-Sentiment-Analysis
 ┣ 📜 01_ChatGPT_Reviews_LSTM.ipynb      # Notebook de l'approche LSTM
 ┣ 📜 02_Allocine_CamemBERT.ipynb        # Notebook du Fine-Tuning CamemBERT
 ┗ 📜 README.md

```

*(Note : Les datasets étant volumineux, ils ont été exclus de ce dépôt via `.gitignore`.)*

## ⚙️ Comment exécuter le code ?

1. Clonez ce repository :
```bash
git clone [https://github.com/votre-nom-utilisateur/NLP-Sentiment-Analysis.git](https://github.com/votre-nom-utilisateur/NLP-Sentiment-Analysis.git)
cd NLP-Sentiment-Analysis

```


2. Installez les dépendances requises :
```bash
pip install torch pandas numpy scikit-learn matplotlib transformers datasets

```


3. Pour le Notebook `01_ChatGPT_Reviews_LSTM.ipynb`, téléchargez le dataset [ChatGPT App Reviews sur Kaggle](https://www.kaggle.com/datasets/ashishkumarak/chatgpt-reviews-daily-updated) et placez le fichier `chatgpt_reviews.csv` à la racine du projet.
4. Lancez Jupyter Notebook ou Jupyter Lab et exécutez les cellules !

## 👨‍💻 Auteur

Mathis Marsault / Axel Bonneau / Louis Maillet

```
