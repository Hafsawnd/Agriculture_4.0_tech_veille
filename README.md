
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




