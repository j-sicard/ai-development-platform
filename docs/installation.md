# Installation de AI Studio

## Présentation

Ce document décrit l'installation de AI Studio, une plateforme locale d'agents IA spécialisés basée sur une architecture IA locale.

La plateforme permet d'exécuter des modèles IA localement et de configurer une équipe d'agents spécialisés capables d'accompagner des projets de développement logiciel.

La plateforme utilise :

- Docker pour l'environnement d'exécution ;
- Open WebUI comme interface utilisateur IA ;
- Ollama comme moteur d'exécution local des modèles ;
- Qwen2.5-Coder 14B comme modèle IA principal ;
- des agents IA spécialisés configurés dans Open WebUI.

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

- Processeur récent ;
- Mémoire RAM adaptée au modèle utilisé ;
- GPU recommandé pour de meilleures performances.

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
# Installation d'Ollama

Installer Ollama puis vérifier l'installation :
```bash
ollama --version
```
Installation du modèle IA

Le modèle utilisé actuellement par la plateforme est :
```bash
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
```bash
NAME

qwen2.5-coder:14b
```
# Installation d'Open WebUI

Le lancement d'Open WebUI utilise Docker.

Le service est situé dans :
```bash
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
```bash
open-webui
PORT 3000->8080
STATUS healthy
```
# Accès à l'interface

Une fois le service démarré, accéder à :
```bash
http://localhost:3000
```
Open WebUI fournit l'interface conversationnelle permettant d'utiliser les modèles IA locaux.

## Configuration des agents IA

Les agents IA sont actuellement configurés directement dans Open WebUI.

Chaque agent possède :

un rôle spécialisé ;
des instructions propres ;
des connaissances associées.

Les agents disponibles sont :

Product Owner / Business Analyst Senior ;
Research Analyst Senior ;
Architecte Logiciel Senior ;
Backend Developer Senior ;
Frontend Developer Senior ;
DevOps Engineer Senior ;
QA Engineer Senior ;
Security Engineer Senior ;
Technical Writer / Documentation Engineer.

Ces agents utilisent une base de connaissances commune couvrant les principaux domaines de l'ingénierie logicielle.

## Vérification du fonctionnement

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
## Structure du projet
AI-Studio
```bash
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
│
└── services
    └── open-webui
```
## Résultat attendu

Après installation :

Open WebUI est accessible localement ;
Ollama exécute le modèle IA ;
Qwen2.5-Coder 14B répond aux demandes ;
les agents IA spécialisés peuvent être utilisés dans l'environnement local ;
la plateforme est prête pour accompagner des projets logiciels.
## Évolutions futures

AI Studio évoluera progressivement avec l'ajout de nouveaux composants :

base PostgreSQL pour les données structurées ;
base vectorielle pour la recherche documentaire ;
architecture RAG ;
mémoire projet persistante ;
amélioration de la collaboration entre agents ;
intégration avec les outils de développement.
## Objectif

Cette installation permet d'obtenir une plateforme IA locale, autonome et reproductible permettant d'accompagner la conception, le développement et l'évolution de projets logiciels grâce à une équipe d'agents IA spécialisés.


