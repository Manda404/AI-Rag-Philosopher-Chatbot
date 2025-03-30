# Philosopher RAG Chatbot 🧠💬
RAG-based chatbot using PDF documents for contextual answers. Built with Streamlit and ChromaDB.

![Project Overview](assets/images/RAG.jpg)

## 📌 Auteur
**Nom :** Rostand Surel

## 🎯 Objectif du Projet
L'objectif de ce projet est de développer un chatbot basé sur la recherche augmentée par récupération (RAG) capable d'interagir avec des utilisateurs et de répondre à leurs questions en se basant sur des documents fournis par l'utilisateur. Ce chatbot vise à offrir une expérience interactive et intelligente pour explorer des contenus philosophiques.

## 🛠️ Solution Proposée
Le projet repose sur une architecture modulaire utilisant les technologies suivantes :
- **Streamlit** pour l'interface utilisateur interactive.
- **Modèles d'embedding** pour la vectorisation des textes.
- **Base de données vectorielle** pour la recherche efficace d'information.
- **Pipeline de preprocessing** pour nettoyer et structurer les données d'entrée.

## 🚀 Fonctionnalités Principales
- 📥 **Upload de fichiers PDF** pour l'analyse.
- 🔍 **Extraction et segmentation du contenu** en chunks optimisés.
- 🏛 **Stockage vectoriel** des embeddings pour une récupération rapide.
- 🤖 **Chat interactif** avec génération de réponses basées sur le contenu du document.

## 🏗️ Structure du Projet
```bash
📂 AI-Rag_Philosopher_Chatbot/
│── README.md               # Documentation principale
│── requirements.txt        # Liste des dépendances
│── .gitignore              # Fichiers à ignorer sur GitHub
│── main.py                 # Point d’entrée de l’application Streamlit
│
├── src/                    # Dossier contenant le cœur du projet
│   ├── __init__.py         # Rendre `src` un module Python
│   ├── ui/                 # Gestion de l’interface utilisateur
│   │   ├── __init__.py
│   │   ├── sidebar.py      # Affichage de la barre latérale
│   │   ├── chat_ui.py      # Interface du chatbot et historique des messages
│   │   ├── pdf_viewer.py   # Affichage des pages PDF avec zoom
│   │   ├── data_upload.py  # Formulaire pour uploader un fichier
│   │   ├── parameters.py   # Gestion des paramètres (chunk_size, modèle, etc.)
│   │
│   ├── data/               # Gestion des données
│   │   ├── __init__.py
│   │   ├── file_handler.py # Gestion du chargement et extraction des fichiers
│   │   ├── chunking.py     # Découpage du texte en morceaux
│   │   ├── embeddings.py   # Génération des embeddings
│   │   ├── vector_db.py    # Stockage et récupération dans ChromaDB
│   │
│   ├── chatbot/            # Gestion du chatbot et des requêtes RAG
│   │   ├── __init__.py
│   │   ├── response.py     # Génération de la réponse via RAG
│   │   ├── retrieval.py    # Recherche dans la base vectorielle
│   │
│   ├── config/             # Configuration générale du projet
│   │   ├── __init__.py
│   │   ├── settings.py     # Paramètres globaux (chemins, API, etc.)
│   │
│   ├── utils/              # Fonctions utilitaires
│   │   ├── __init__.py
│   │   ├── logger.py       # Gestion centralisée des logs
│   │   ├── validators.py   # Fonctions pour valider les entrées utilisateur
│   │   ├── helpers.py      # Fonctions génériques
│
├── tests/                  # Dossier des tests unitaires
│   ├── test_file_handler.py
│   ├── test_chunking.py
│   ├── test_embeddings.py
│   ├── test_vector_db.py
│   ├── test_response.py
│
└── assets/                 # Ressources pour le README et l’application
    ├── images/             # Images utilisées dans le projet
    │   ├── project_overview.png # Schéma explicatif du chatbot
    ├── pdf_samples/        # Échantillons de PDF pour test
├── logo.png                # Logo du projet
```

## 🔧 Installation et Utilisation
### 📌 Prérequis
Assurez-vous d'avoir **Python 3.8+** et **pip** installés.

### 📥 Installation
```bash
git clone https://github.com/Manda404/Philosopher_Chatbot.git
cd Philosopher_Chatbot
pip install -r requirements.txt
```

### 🚀 Lancer l'application
```bash
streamlit run app.py
```

## 📚 Exemples d'Utilisation
1. **Uploader un fichier PDF** via l'interface.
2. **Lancer le traitement des données** pour générer les embeddings.
3. **Poser des questions** et obtenir des réponses contextuelles basées sur le document.

## 📄 Licence
Ce projet est sous licence MIT. Libre à vous de l'utiliser et de l'améliorer !

## 🤝 Contribution
Les contributions sont les bienvenues ! Ouvrez une issue ou soumettez une pull request. 😊
