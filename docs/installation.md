# Installation de la plateforme IA locale

## Présentation

Ce document décrit l'installation de la plateforme AI Development Platform basée sur une architecture IA locale.

La solution utilise :

- Docker pour l'environnement d'exécution
- Open WebUI comme interface utilisateur IA
- Ollama comme moteur d'exécution des modèles
- Qwen2.5-Coder 14B comme modèle de langage

---

# Prérequis

## Système

- Windows 10/11
- Docker Desktop installé
- Ollama installé
- Git installé

## Ressources recommandées

L'utilisation d'un modèle local nécessite des ressources matérielles suffisantes.

Recommandations :

- Processeur récent
- Mémoire RAM adaptée au modèle utilisé
- GPU recommandé pour de meilleures performances

---

# Installation de Docker

Installer Docker Desktop puis vérifier son fonctionnement :

```bash
docker --version
```

Vérifier que Docker fonctionne :

```bash
docker ps
```

---

# Installation d'Ollama

Installer Ollama puis vérifier l'installation :

```bash
ollama --version
```

---

# Installation du modèle IA

Le modèle utilisé par la plateforme est :

```text
Qwen2.5-Coder 14B
```

Téléchargement du modèle :

```bash
ollama pull qwen2.5-coder:14b
```

Vérification des modèles installés :

```bash
ollama list
```

Exemple :

```text
NAME
qwen2.5-coder:14b
```

---

# Installation d'Open WebUI

Le lancement d'Open WebUI utilise Docker.

Créer le dossier du service :

```text
services/open-webui
```

Démarrer le service :

```bash
docker compose up -d
```

Vérifier le conteneur :

```bash
docker ps
```

Exemple :

```text
open-webui
PORT 3000->8080
STATUS healthy
```

---

# Accès à l'interface

Une fois le service démarré, accéder à :

```text
http://localhost:3000
```

Open WebUI fournit l'interface conversationnelle permettant d'utiliser les modèles IA locaux.

---

# Vérification du fonctionnement

Vérifier les modèles disponibles :

```bash
ollama list
```

Vérifier les modèles actifs :

```bash
ollama ps
```

Tester une requête :

```bash
ollama run qwen2.5-coder:14b
```

---

# Structure du projet

```text
AI-Development-Platform

├── README.md
│
├── diagrams
│   ├── Architecture-Plateforme-IA.drawio
│   ├── Organisation-Agents-IA.drawio
│   └── Pipeline-DevOps.drawio
│
├── docs
│   ├── presentation.md
│   ├── agents.md
│   ├── architecture.md
│   ├── pipeline-devops.md
│   └── installation.md
```

---

# Résultat attendu

Après installation :

- Open WebUI est accessible localement
- Ollama exécute le modèle IA
- Qwen2.5-Coder 14B répond aux demandes
- L'environnement est prêt pour l'intégration des agents IA spécialisés

---

# Objectif

Cette installation permet d'obtenir une plateforme IA locale, autonome et reproductible pour accompagner des projets de développement logiciel.