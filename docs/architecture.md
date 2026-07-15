# Architecture de la plateforme IA

## Présentation

La plateforme AI Development Platform est une solution IA locale basée sur Open WebUI, Ollama et un modèle de langage spécialisé.

L'objectif est de fournir un environnement d'assistance au développement logiciel utilisant des agents IA spécialisés, une base de connaissances métier et un moteur IA local.

---

## Vue globale de l'architecture

```text
+----------------------+
|      Utilisateur     |
+----------------------+
           |
           v
+----------------------+
|   Navigateur Web     |
+----------------------+
           |
           v
+----------------------+
|      Open WebUI      |
|     Interface IA     |
+----------------------+
           |
           v
+----------------------+
| Gestion des Agents IA|
+----------------------+
       |          |
       v          v
+------------+  +----------------------+
| Agents IA  |  | Base de connaissances |
+------------+  +----------------------+
       |
       v
+----------------------+
|        Ollama        |
+----------------------+
           |
           v
+----------------------+
| Qwen2.5-Coder 14B    |
|     Modèle IA        |
+----------------------+
```


---

# Composants de la plateforme

## 1. Utilisateur

L'utilisateur interagit avec la plateforme depuis un navigateur web.

Il peut :
- Poser des questions
- Demander une analyse
- Solliciter un agent spécialisé
- Obtenir une assistance au développement

---

## 2. Open WebUI

Open WebUI constitue l'interface utilisateur de la plateforme.

Rôle :

- Fournir une interface conversationnelle
- Communiquer avec le moteur IA
- Permettre l'utilisation des agents IA

---

## 3. Gestion des Agents IA

Cette couche organise les différents agents spécialisés.

Elle permet :

- La séparation des responsabilités
- L'utilisation d'agents adaptés aux besoins
- L'organisation du travail comme une équipe projet

Les agents utilisent les capacités du modèle IA pour produire leurs analyses et recommandations.

---

## 4. Base de connaissances

La base de connaissances contient les informations nécessaires au contexte du projet.

Elle permet :

- Conservation des informations métier
- Références techniques
- Documentation projet
- Capitalisation des connaissances

Elle améliore la pertinence des réponses fournies par les agents.

---

## 5. Ollama

Ollama est le moteur d'exécution local des modèles IA.

Rôle :

- Gestion des modèles de langage
- Exécution locale des requêtes IA
- Communication avec Open WebUI

Avantages :

- Fonctionnement local
- Confidentialité des données
- Maîtrise de l'environnement

---

## 6. Modèle IA Qwen2.5-Coder 14B

Qwen2.5-Coder 14B est le modèle de langage utilisé par la plateforme.

Il fournit les capacités :

- Génération de code
- Analyse technique
- Explication de concepts
- Assistance au développement logiciel

---

## 7. Docker

Docker fournit l'environnement d'exécution des services.

Rôle :

- Isolation des composants
- Déploiement simplifié
- Gestion des services
- Reproductibilité de l'environnement

---

# Flux de fonctionnement

## Exemple d'une demande utilisateur

1. L'utilisateur envoie une demande via Open WebUI.
2. La demande est orientée vers l'agent spécialisé.
3. L'agent utilise le modèle Qwen2.5-Coder via Ollama.
4. L'agent consulte les connaissances disponibles.
5. Une réponse adaptée est générée.

---

# Objectifs de l'architecture

Cette architecture permet :

- Une IA locale et maîtrisée
- Une organisation multi-agents
- Une séparation claire des responsabilités
- Une meilleure adaptation aux projets logiciels
- Une base évolutive pour de futurs développements