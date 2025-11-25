🌾 Veille Agricole 4.0 – Plateforme de Web Scraping et Tableau de Bord Interactif

Ce projet met en place un système automatisé pour collecter, analyser et visualiser des contenus liés à l’Agriculture 4.0. Il s’appuie sur plusieurs web scrapers personnalisés, une base de données MongoDB et un tableau de bord interactif développé avec Streamlit. Les données collectées sont évaluées en termes de crédibilité avant d’être affichées.
📁 Architecture du Projet
.
├── scrape_google_alert.py                   # Fetches Google Alerts via Gmail API
├── scrape_google_scholar.py                 # Queries Google Scholar via SerpAPI
├── scrape_ieee.py                           # Scrapes IEEE Xplore articles
├── scrape_springer.py                       # Scrapes SpringerLink
├── scrape_wiley.py                          # Scrapes Wiley Online Library
├── scrape_talkwalker/
│   ├── auto_save_to_talkwalkerfolder.py     # Saves Talkwalker emails via IMAP
│   └── extract_informations_from_talkwalker.py  # Extracts articles from saved Talkwalker
├── credibility_test.py                      # Filters out non-credible publications
├── app.py                                   # Streamlit dashboard for data visualization
├── daily_scraper_scheduler.py               # Central scheduler for daily automation
├── requirements.txt                         # Clean dependency list
├── .env                                     # Secret config (excluded)
├── .gitignore                               # Git exclusion rules
├── token.json                               # Gmail token (excluded)
└── README.md                                # This file


⚙️ Instructions d’Installation
1. Installation des dépendances
pip install -r requirements.txt

2. Configuration des accès confidentiels

Créer un fichier .env à la racine :

GMAIL_TOKEN_PATH=token.json
GMAIL_CREDENTIALS_PATH=client_secret_XXXX.json
SERPAPI_KEY=your-serpapi-key
IMAP_EMAIL=youremail@example.com
IMAP_PASSWORD=your-imap-password


Le fichier .env reste protégé grâce au .gitignore.

🚀 Extraction & Traitement Automatisés
Lancer les scrapers individuellement :
python scrape_google_alert.py
python scrape_google_scholar.py
python scrape_ieee.py
python scrape_springer.py
python scrape_wiley.py
python scrape_talkwalker/auto_save_to_talkwalkerfolder.py
python scrape_talkwalker/extract_informations_from_talkwalker.py

Planification quotidienne :
python daily_scraper_scheduler.py

Application du filtre de crédibilité :
python credibility_test.py

📊 Tableau de Bord Streamlit

Lancement du dashboard :

streamlit run app.py


Il permet d’explorer :

📈 Les tendances globales & l’évolution des publications

🌍 Une cartographie des sources

📰 Les contenus récents et pertinents

🔝 Les domaines scientifiques les plus actifs

☁️ Des word clouds informatifs

📅 Des séries temporelles des publications

![dash1](https://github.com/user-attachments/assets/9fc5fabe-5107-4f7a-a5b2-667bb6b429d4)

![dash2](https://github.com/user-attachments/assets/c09ddcb0-2e80-4d5a-8b0e-4c2cbc7d864e)
![dash3](https://github.com/user-attachments/assets/d38da935-996b-43b6-a647-2ab15e30c04f)
📦 Collections MongoDB

google_alerts_Agriculture4.0

talkwalker_alerts_Agriculture4.0

ieee_agriculture_4_0_newest / relevant

wiley_agriculture_4_0_newest / relevant

springer_agriculture_4_0_newest / relevant

scholar_agriculture_4_0_newest / relevant

🧠 Fonctionnalités Principales

✅ Scraping automatisé avec comportement anti-bot
✅ Gestion sécurisée des identifiants
✅ Exécution planifiée quotidienne
✅ Déduplication intelligente dans MongoDB
✅ Score de crédibilité pour filtrage avancé
✅ Dashboard Streamlit riche Voici une **version propre, concise et professionnelle**, parfaitement adaptée pour un **README GitHub**.
Elle est structurée, claire, sans emojis (ou avec quelques-uns si tu veux), et optimisée pour GitHub.

---

# 🌾 Veille Agricole 4.0 – Web Scraping & Streamlit Dashboard

Ce projet propose une solution complète de veille technologique sur **l’Agriculture 4.0**, intégrant du web scraping automatisé, un filtrage de crédibilité des sources, une base de données MongoDB et un tableau de bord interactif construit avec **Streamlit**.
L’objectif est de collecter, analyser et visualiser des articles scientifiques, alertes et contenus pertinents provenant de plusieurs plateformes académiques.

---

## 📂 Structure du Projet

```
.
├── scrape_google_alert.py                   # Extraction des Google Alerts via Gmail API
├── scrape_google_scholar.py                 # Requêtes Google Scholar via SerpAPI
├── scrape_ieee.py                           # Scraper IEEE Xplore
├── scrape_springer.py                       # Scraper SpringerLink
├── scrape_wiley.py                          # Scraper Wiley Online Library
├── scrape_talkwalker/
│   ├── auto_save_to_talkwalkerfolder.py     # Sauvegarde des emails Talkwalker via IMAP
│   └── extract_informations_from_talkwalker.py  # Extraction des articles Talkwalker
├── credibility_test.py                      # Score de crédibilité des publications
├── app.py                                   # Tableau de bord Streamlit
├── daily_scraper_scheduler.py               # Planification d’exécution quotidienne
├── requirements.txt                         # Dépendances
├── .env                                     # Variables sensibles (non versionné)
├── .gitignore                               # Règles d’exclusion
└── README.md                                # Documentation
```

---

## ⚙️ Installation

### 1. Installer les dépendances

```bash
pip install -r requirements.txt
```

ou manuellement :

```bash
pip install selenium webdriver-manager pymongo schedule requests beautifulsoup4 python-dotenv streamlit
```

---

## 🔐 Configuration

Créer un fichier `.env` :

```
GMAIL_TOKEN_PATH=token.json
GMAIL_CREDENTIALS_PATH=client_secret_XXXX.json
SERPAPI_KEY=your-serpapi-key
IMAP_EMAIL=youremail@example.com
IMAP_PASSWORD=your-imap-password
```

> Le fichier `.env` est ignoré par Git.

---

## 🚀 Exécution des Scrapers

### Lancer un scraper spécifique :

```bash
python scrape_google_alert.py
python scrape_google_scholar.py
python scrape_ieee.py
python scrape_springer.py
python scrape_wiley.py
python scrape_talkwalker/auto_save_to_talkwalkerfolder.py
python scrape_talkwalker/extract_informations_from_talkwalker.py
```

### Lancer l’ensemble des scrapers quotidiennement :

```bash
python daily_scraper_scheduler.py
```

### Appliquer le filtre de crédibilité :

```bash
python credibility_test.py
```

---

## 📊 Tableau de Bord Streamlit

Lancer l’application :

```bash
streamlit run app.py
```

### Le dashboard inclut :

* Évolution et tendances globales
* Répartition géographique des sources
* Articles récents et pertinents
* Classement des domaines scientifiques
* Word clouds
* Séries temporelles
![dash1](https://github.com/user-attachments/assets/9fc5fabe-5107-4f7a-a5b2-667bb6b429d4)

![dash2](https://github.com/user-attachments/assets/c09ddcb0-2e80-4d5a-8b0e-4c2cbc7d864e)
![dash3](https://github.com/user-attachments/assets/d38da935-996b-43b6-a647-2ab15e30c04f)
---

## 🗄️ Collections MongoDB

* `google_alerts_Agriculture4.0`
* `talkwalker_alerts_Agriculture4.0`
* `ieee_agriculture_4_0_newest`, `ieee_agriculture_4_0_relevant`
* `wiley_agriculture_4_0_newest`, `wiley_agriculture_4_0_relevant`
* `springer_agriculture_4_0_newest`, `springer_agriculture_4_0_relevant`
* `scholar_agriculture_4_0_newest`, `scholar_agriculture_4_0_relevant`

---

## 🧠 Fonctionnalités

* Scraping automatisé
* Gestion sécurisée des identifiants
* Planification quotidienne
* Déduplication intelligente
* Système de crédibilité des sources
* Dashboard interactif

---

## 🎓 Projet Académique

Projet réalisé dans le cadre d’un module de **Veille Technologique – Agriculture 4.0** par une équipe d’étudiants en ingénierie data.

---



🎓 Projet académique – Veille Technologique Agriculture 4.0

Développé par une équipe d’étudiants en ingénierie data.




