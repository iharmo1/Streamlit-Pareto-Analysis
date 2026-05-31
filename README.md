# 📊 Analyse Pareto – Application Streamlit

Bienvenue dans l'application **Analyse Pareto**, un outil interactif développé avec **Streamlit** pour identifier rapidement les causes principales d'un problème selon la loi de Pareto (règle des 80/20).

## 🚀 Fonctionnalités Principales

*   **Importation de données** : Chargez vos données facilement depuis un fichier `.csv` ou `.xlsx` (colonnes requises : `Cause` et `Occurrence`).
*   **Saisie manuelle** : Ajoutez ou supprimez des causes directement depuis la barre latérale.
*   **Calcul Automatique** : Tri décroissant automatique, calcul des pourcentages et pourcentages cumulés.
*   **Visualisation Graphique** : Génération instantanée du diagramme de Pareto (histogramme des occurrences + courbe des pourcentages cumulés).
*   **Identification Top 80%** : Mise en évidence visuelle des "Top Causes" qui représentent 80% du problème.
*   **Export Excel** : Téléchargez un rapport Excel complet incluant les données formatées et le graphique intégré.
*   **Export Word** : Générez un rapport textuel automatique `.docx` incluant un résumé analytique et l'image du graphique des top causes.

## 🏗️ Architecture et Technologies

L'application repose sur une pile 100% Python, conçue pour être légère et rapide :

*   **[Streamlit](https://streamlit.io/)** : Framework utilisé pour l'interface utilisateur web et le rendu interactif.
*   **[Pandas](https://pandas.pydata.org/) & Numpy** : Utilisés comme moteur de calcul backend pour nettoyer, trier et agréger les données, avec un système de cache (`@st.cache_data`) pour des performances optimales.
*   **[Matplotlib](https://matplotlib.org/)** : Utilisé pour générer le diagramme de Pareto (double axe Y).
*   **[OpenPyXL](https://openpyxl.readthedocs.io/)** : Permet la création du fichier Excel d'exportation avec mise en forme conditionnelle et insertion d'image.
*   **[python-docx](https://python-docx.readthedocs.io/)** : Génère le document Word final structuré.

## ⚙️ Installation et Déploiement en Local

Suivez ces étapes pour exécuter le projet sur votre propre machine :

### 1. Cloner le dépôt
```bash
git clone https://github.com/iharmo1/Streamlit-Pareto-Analysis.git
cd Streamlit-Pareto-Analysis
```

### 2. (Optionnel) Créer un environnement virtuel
Il est recommandé d'utiliser un environnement virtuel pour isoler les dépendances.
```bash
# Sur Windows
python -m venv venv
venv\Scripts\activate

# Sur macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Installer les dépendances
Installez toutes les librairies requises présentes dans le fichier `requirements.txt` :
```bash
pip install -r requirements.txt
```

### 4. Lancer l'application Streamlit
Exécutez la commande suivante pour démarrer le serveur local :
```bash
streamlit run Pareto.py
```
L'application s'ouvrira automatiquement dans votre navigateur web à l'adresse par défaut : `http://localhost:8501`.

## 📂 Structure du Projet

```text
Streamlit-Pareto-Analysis/
│
├── Pareto.py              # Code source principal de l'application web
├── requirements.txt       # Liste des dépendances Python nécessaires
├── .gitignore             # Fichiers ignorés par Git
└── README.md              # Documentation du projet (ce fichier)
```

## 📝 Format des fichiers d'import (CSV/Excel)

Si vous importez vos propres données, assurez-vous que votre fichier contient exactement ces deux en-têtes de colonnes :
1. `Cause` (Texte)
2. `Occurrence` (Nombre)

---
*Projet développé et maintenu pour faciliter l'analyse continue et l'amélioration de la qualité.*
