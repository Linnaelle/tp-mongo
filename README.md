# Movie Explorer – Orchestrateur Docker

Ce dépôt permet de lancer l'application complète **Movie Explorer**, composée d'un frontend React et d'un backend Flask connectés à MongoDB.Tout est conteneurisé via Docker.

---

## Objectif de l'application

**Movie Explorer** est une application web permettant d'explorer et d'analyser une base de données de films. Elle propose :

- Un tableau de bord avec statistiques et graphiques
- Une exploration par genre, popularité, ou époque
- Un affichage interactif et responsive des données

Cette architecture vise à illustrer l'utilisation combinée d'un backend en Flask, d'une base de données MongoDB, et d'un frontend moderne en React, le tout orchestré via Docker.

---

## Contenu du projet

```
movie-explorer-deploy/
├── tp-mongo-back/        # Backend Flask
├── tp-mongo-front/       # Frontend React
└── docker-compose.yml    # Orchestration des services
```

---

## Déploiement

### 1. Cloner ce dépôt avec les submodules

```bash
git clone --recurse-submodules https://github.com/Linnaelle/tp-mongo.git
cd tp-mongo
```

> Si vous avez déjà cloné le dépôt sans `--recurse-submodules` :
```bash
git submodule update --init --recursive
```

### 2. Lancer les conteneurs

```bash
docker-compose up --build
```

---

## Accès aux services

| Service  | URL                                            |
| -------- | ---------------------------------------------- |
| Frontend | [http://localhost:8080](http://localhost:8080) |
| Backend  | [http://localhost:5000](http://localhost:5000) |

---

## Pré-requis

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/fr-fr/windows/wsl/install) pour les utilisateurs Windows

---

## Arborescence attendue

```
tp-mongo/
├── docker-compose.yml
├── tp-mongo-back/
│   └── app/
└── tp-mongo-front/
    └── src/
```

---

## Arrêter les conteneurs

```bash
docker-compose down
```
