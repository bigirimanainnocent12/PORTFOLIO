# 📊 Data Scientist & Analyst Portfolio - Innocent BIGIRIMANA

Bienvenue sur le dépôt de mon portfolio professionnel. Ce projet présente mes compétences en Data Science, Data Engineering et Business Intelligence, ainsi que mes projets phares réalisés sur le cloud (GCP) et en local.

## 🚀 À propos de moi
Je suis **Innocent BIGIRIMANA**, un passionné de la donnée spécialisé dans la transformation d'écosystèmes complexes en leviers décisionnels stratégiques. Mon expertise couvre l'ensemble du cycle de vie de la donnée : de l'ingestion automatisée à la modélisation prédictive et la visualisation.

## 🛠️ Stack Technique
- **Languages**: Python (Pandas, PySpark, Scikit-Learn), SQL (PostgreSQL, SQL Server).
- **Cloud & Orchestration**: Google Cloud Platform (GCP), BigQuery, Cloud Composer (Apache Airflow), Google Cloud Storage.
- **Business Intelligence**: Power BI (DAX Advanced), Tableau, Data Storytelling.
- **Data Engineering**: Pipelines ETL/ELT industriels, Automatisation des flux.
- **Machine Learning**: Régression, Classification, BigQuery ML, MLOps.

## 📂 Structure du Projet
```text
Portfolio-Innocent/
├── assets/                 # Ressources multimédias (images des projets, logos)
├── index.html              # Page principale du portfolio (Structure HTML5)
├── style.css               # Design UI/UX, animations et responsive design
├── script.js               # Interactions dynamiques et effets de défilement
├── download_images.py      # Script Python pour la gestion des assets images
├── download_logo.py        # Script Python pour la récupération des logos
└── README.md               # Documentation et présentation du projet
```

## 📂 Projets Phares

### 1. Burundi RAG Chatbot
- **Description** : Dans ce projet, j'ai conçu et développé un chatbot intelligent basé sur une architecture RAG pour automatiser la recherche et la synthèse d'indicateurs socio-économiques complexes sur le Burundi. Cela permet aux décideurs d'accéder instantanément à des données vérifiées, réduisant de 80% le temps de recherche d'informations et améliorant la précision des analyses stratégiques.
- **Techniques** : Retrieval-Augmented Generation (RAG), recherche sémantique vectorielle, segmentation de texte (chunking), embeddings multilingues, prompt engineering.
- **Outils** : LangChain (LCEL), ChromaDB, sentence-transformers, Claude Haiku, FastAPI, Python, Pytest, Pydantic.
- **Fichiers & APIs** : Ingestion automatisée de rapports officiels au format **PDF** (Banque Mondiale, PNUD, OMS, INSBU, FMI) et intégration de l'**API Anthropic Claude**.
- **Fonctions Clés** : `PyPDFLoader`, `RecursiveCharacterTextSplitter`, `paraphrase-multilingual-MiniLM-L12-v2`, `Chroma.from_documents()`, endpoints FastAPI.

### 2. Prédiction du Risque d’Accident (Assurance) - Databricks
- **Description** : Dans ce projet, j'ai développé un pipeline d'ingestion et de transformation de données routières sur Databricks basé sur l'architecture Medallion pour estimer le risque d'accidents de la route. J'ai stocké les fichiers CSV historiques dans un dossier Databricks, puis créé un notebook d'ingestion et de traitement dédié pour chaque couche (Bronze, Silver, Gold), le tout orchestré par des pipelines et workflows Databricks. L'impact métier est de fournir un entrepôt Lakehouse structuré et performant pour l'analyse dynamique des sinistres d'assurance.
- **Techniques** : Architecture Lakehouse (Médaillon Bronze/Silver/Gold avec un notebook par couche), Ingestion/transformation massives distribuées (ETL), Feature Engineering avancé, orchestration.
- **Outils** : Databricks (Workflows, Notebooks), PySpark (Spark SQL), Delta Lake, Python, MLflow, XGBoost.
- **Fichiers & APIs** : Ingestion de fichiers historiques **CSV** stockés dans Databricks (Volumes/DBFS), croisés avec l'**API OpenWeather** (données météo) et l'**API OpenStreetMap** (données géospatiales).
- **Fonctions Clés** : `spark.read.csv()`, `DataFrame.join()`, `XGBoostClassifier`, `mlflow.log_metric()`.

### 3. Prédiction du Risque d’Accident (Assurance) - GCP
- **Description** : Dans ce projet, j'ai utilisé une API publique pour automatiser la collecte de fichiers de données routières au format CSV et les stocker dans un bucket Google Cloud Storage (GCS). J'ai ensuite développé des scripts d'ingestion et de transformation SQL pour structurer des données propres et prêtes à l'emploi dans BigQuery, et j'ai orchestré l'ensemble de ces flux de données à l'aide de Google Cloud Composer (Apache Airflow). L'impact métier est de fournir un entrepôt de données analytique centralisé et fiable pour l'évaluation en temps réel du risque routier en assurance.
- **Techniques** : Ingestion Cloud automatisée (ELT), stockage cloud, ingestion et transformation de données structurées, modélisation d'entrepôt, orchestration.
- **Outils** : Google Cloud Platform (GCP), Google Cloud Storage (GCS), BigQuery, Google Cloud Composer (Apache Airflow), Python.
- **Fichiers & APIs** : Ingestion automatisée de fichiers **CSV**, stockage dans **GCS**, entreposage dans **BigQuery** et intégration avec une **API publique**.
- **Fonctions Clés** : Requêtes SQL BigQuery (`MERGE`), `requests.get()`, DAGs Airflow (`GCSToBigQueryOperator`, `BigQueryInsertJobOperator`).

### 4. NYC Taxi Data Pipeline (150M+ lignes)
- **Description** : Dans ce projet, j'ai conçu et automatisé un pipeline de données ELT cloud à grande échelle pour analyser plus de 150 millions de trajets de taxis new-yorkais. J'ai téléchargé les fichiers de données d'origine au format Parquet, puis je les ai stockés dans un bucket Google Cloud Storage (GCS) avant de concevoir des scripts d'ingestion et de transformation dans BigQuery. L'impact métier est d'identifier les zones géographiques à forte valeur et les horaires critiques afin de permettre aux compagnies de transport d'optimiser le déploiement de leurs flottes, augmentant ainsi le taux d'occupation des véhicules et maximisant le chiffre d'affaires.
- **Techniques** : Pipeline ELT Cloud, traitement de données massives (Big Data), ingestion et partitionnement, orchestration de workflows, Machine Learning intégré en base de données (BigQuery ML).
- **Outils** : GCP (GCS, BigQuery), Cloud Composer (Airflow), BigQuery ML, Power BI, Python.
- **Fichiers & APIs** : Fichiers volumineux au format **Parquet** téléchargés de la NYC TLC et stockés dans **GCS** avant chargement dans **BigQuery**.
- **Fonctions Clés** : `GCSToBigQueryOperator`, `BigQueryCreateExternalTableOperator`, partitionnement SQL (`PARTITION BY Date`), requêtes BigQuery ML (`OPTIONS(model_type='linear_reg')`).

### 5. Pipeline Météo Automatisé
- **Description** : Dans ce projet, j'ai conçu et automatisé un pipeline d'ingestion et de transformation de données météo mondiales. J'ai développé un flux ETL complet pour extraire régulièrement les prévisions météorologiques mondiales, et j'ai orchestré l'ensemble du pipeline avec Apache Airflow. L'impact métier est de fournir au secteur logistique des prévisions fiables pour planifier à l'avance leurs itinéraires et éviter les retards du fait des intempéries, sécurisant ainsi la chaîne d'approvisionnement et réduisant les coûts opérationnels.
- **Techniques** : Pipeline ETL automatisé, planification de tâches (Scheduling), orchestration de workflows, modélisation de base de données relationnelle.
- **Outils** : Python, Apache Airflow, PostgreSQL, Power BI.
- **Fichiers & APIs** : Ingestion de flux au format **JSON** provenant de l'**API Open-Météo**, stockés dans PostgreSQL.
- **Fonctions Clés** : `requests.get()` pour interroger l'API Open-Météo, constructeur `DAG()` d'Airflow, `PythonOperator`, `PostgresOperator`, requêtes SQL d'upsert (`ON CONFLICT DO UPDATE`).

### 6. Optimisation des Ventes
- **Description** : Dans ce projet, j'ai modélisé et mis en œuvre une solution d'analyse décisionnelle des performances commerciales. L'impact métier est d'offrir aux directions commerciale et financière une visibilité totale sur les indicateurs de rentabilité par produit, segment de clientèle et région, permettant de corriger les marges faibles et d'améliorer la fidélisation des clients grâce à une tarification ciblée.
- **Techniques** : Modélisation décisionnelle (Schéma en étoile), analyse multidimensionnelle, Data Storytelling, Business Intelligence.
- **Outils** : Power BI, SQL Server, Power Query, DAX (Data Analysis Expressions).
- **Fichiers & APIs** : Consolidation de données au format **CSV** et de bases relationnelles SQL Server.
- **Fonctions Clés** : Formules DAX `CALCULATE()`, `DIVIDE()`, `DATESYTD()`, `SAMEPERIODLASTYEAR()`, `USERELATIONSHIP()`.

### 7. Prédiction des Frais d'Assurance
- **Description** : Dans ce projet, j'ai développé et déployé une API de prédiction des coûts médicaux annuels des assurés. L'impact métier est d'automatiser à 95% l'estimation des dépenses de santé individuelles lors de la soumission d'une demande de souscription, garantissant des offres tarifaires adaptées au profil de risque de l'assuré (âge, statut fumeur, IMC) tout en limitant les pertes financières pour l'assureur.
- **Techniques** : Analyse Exploratoire des Données (EDA), Feature Engineering, Régression (Machine Learning), optimisation d'hyperparamètres, déploiement d'API REST.
- **Outils** : Python, Scikit-Learn, FastAPI, Render, Pandas, Seaborn, Matplotlib.
- **Fichiers & APIs** : Jeu de données historique au format **CSV** (`insurance.csv`).
- **Fonctions Clés** : `pd.read_csv()`, `train_test_split()`, `RandomForestRegressor()`, `StandardScaler`, `OneHotEncoder`, `joblib.load()`.

### 8. Analyses Inferentielles (ANOVA / Test-T)
- **Description** : Dans ce projet, j'ai conçu un protocole d'analyses statistiques inférentielles pour valider les décisions opérationnelles de production. L'impact métier est de fournir des preuves scientifiques indiscutables avant d'effectuer des modifications industrielles ou des lancements de produits coûteux, en garantissant avec un intervalle de confiance de 95% ou 99% que les différences de performance observées sont réelles et non dues à des variations aléatoires.
- **Techniques** : Tests d'hypothèses, validation des hypothèses (normalité, homoscédasticité), ANOVA, test de Student, test post-hoc.
- **Outils** : Python, SciPy (stats), Statsmodels, Matplotlib.
- **Fichiers & APIs** : Analyse expérimentale à partir de fichiers **CSV** importés dans des DataFrames.
- **Fonctions Clés** : `scipy.stats.shapiro()`, `scipy.stats.levene()`, `scipy.stats.f_oneway()`, `scipy.stats.ttest_ind()`, `pairwise_tukeyhsd()`.

## 🎨 Design du Portfolio
Le portfolio est conçu avec une esthétique moderne et premium :
- **Technologies** : HTML5, CSS3 (Vanilla), JavaScript.
- **Features** : Design responsive, animations d'apparition (Reveal JS), Glassmorphism, typographie Outfit/Inter.
- **Architecture** : Section projets avec numérotation stylisée et focus sur les stacks techniques.

## 📬 Contact
- **LinkedIn** : [innocent-bigirimana](https://www.linkedin.com/in/bigirimanainnocent12)
- **GitHub** : [bigirimanainnocent12](https://github.com/bigirimanainnocent12)
- **Email** : [innocentbigirimana@example.com]

---
*© 2026 Innocent BIGIRIMANA | Conçu avec passion.*
