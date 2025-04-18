# Movie Explorer – Projet Fullstack

Ce projet est une application web fullstack qui permet d'explorer une base de données de films, grâce à une API Flask connectée à MongoDB, et un frontend moderne construit avec React et TailwindCSS.

Pensée pour être simple à utiliser et à déployer, l'application permet d'explorer des films par genre, d'effectuer des recherches et d'afficher des statistiques.

---

## Objectif pédagogique

Ce projet a été réalisé dans le cadre d'un travail de groupe sur 3 jours. Il nous a permis de mettre en pratique l'ensemble de la chaîne de développement web :

- Construction d'une API REST avec Flask
- Utilisation de MongoDB et modélisation de documents
- Intégration frontend avec React / Vite / Tailwind
- Mise en place d'une architecture conteneurisée avec Docker
- Collaboration avec Git (et submodules)

---

## Déploiement

### 1. Cloner ce dépôt principal (structure globale)

```bash
git clone --recurse-submodules https://github.com/Linnaelle/tp-mongo.git
cd tp-mongo
```

> Si vous avez déjà cloné le repo sans `--recurse-submodules`, faites :
>
> ```bash
> git submodule update --init --recursive
> ```

### 2. Créer un fichier .env pour le backend

Créez un fichier .env à la racine du dossier tp-mongo-back avec le contenu suivant (valeurs à adapter) :

```bash
DB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/movie-app?retryWrites=true&w=majority
TMDB_API_KEY=your_tmdb_api_key
TMDB_BASE=https://api.themoviedb.org/3
```

Vous pouvez vous baser sur le fichier .env.example fourni.

### 3. Démarrer l'application avec Docker

```bash
docker-compose up --build
```

L'application sera disponible sur :

- Backend (API Flask) : [http://localhost:5000](http://localhost:5000)
- Frontend (interface web) : [http://localhost:8080](http://localhost:8080)

---

## Structure du projet

```bash
tp-mongo/                # Dépôt principal
├── docker-compose.yml   # Déploiement multi-services
├── .env                 # Variables d'environnement globales (ex : DB_URI)
├── tp-mongo-back/       # Sous-module backend (Flask + MongoDB)
└── tp-mongo-front/      # Sous-module frontend (React + Vite + Nginx)
```

---

## Membres du projet

- **Dashboard / Analytics** : Omomene IWELOMEN
- **Développement fullstack** : Paul SODE, Belem Gloire BEKOUTOU, Philippe Le Goff
- **Environnement, DevOps et structuration** : Clément PERRET

---

## Remarques

- L'ensemble du projet fonctionne avec Docker, mais chaque service peut être lancé indépendamment si besoin (voir README du front/back).
- Si vous utilisez Windows, pensez à activer l'intégration WSL2 dans Docker Desktop.
