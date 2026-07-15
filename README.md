# AI Development Platform

## Présentation

AI Development Platform est une plateforme d'assistance au développement logiciel basée sur l'intelligence artificielle.

L'objectif est de créer un environnement capable d'accompagner les différentes phases d'un projet informatique grâce à des agents IA spécialisés.

La plateforme simule une équipe technique complète composée de plusieurs profils experts : architecture, développement, DevOps, sécurité, qualité et documentation.

---

## Objectifs du projet

Cette plateforme permet de :

- structurer les connaissances d'un projet ;
- assister les équipes de développement ;
- améliorer la qualité du code ;
- accélérer l'analyse et la conception ;
- automatiser certaines tâches répétitives ;
- appliquer les bonnes pratiques d'ingénierie logicielle.

---

## Architecture globale

La solution repose sur :

- **Open WebUI** : interface utilisateur IA ;
- **Gestion des agents IA** : agents spécialisés par domaine ;
- **Base de connaissances projet** : stockage des informations métier, techniques et documentaires utilisées par les agents IA ;
- **Ollama** : moteur d'exécution local des modèles IA ;
- **Qwen2.5-Coder 14B** : modèle IA principal utilisé.

---

## Agents IA

La plateforme utilise une équipe de 9 agents spécialisés :

- Product Owner / Business Analyst Senior
- Research Analyst Senior
- Architecte Logiciel Senior
- Backend Developer Senior
- Frontend Developer Senior
- DevOps Engineer Senior
- QA Engineer Senior
- Security Engineer Senior
- Technical Writer / Documentation Engineer

---

## Projet démonstrateur

La plateforme est utilisée pour accompagner la conception d'un ERP PME.

Elle permet de gérer :

- l'architecture ;
- le développement ;
- la documentation ;
- les tests ;
- le déploiement ;
- les bonnes pratiques DevOps.

---

## Documentation

La documentation complète se trouve dans le dossier :

```
docs/
```

Documents disponibles :

- [Présentation](docs/presentation.md)
- [Architecture](docs/architecture.md)
- [Agents IA](docs/agents.md)
- [Pipeline DevOps](docs/pipeline-devops.md)
- [Installation](docs/installation.md)

---

## Technologies utilisées

| Domaine | Technologie |
|---|---|
| Interface IA | Open WebUI |
| Modèle IA | Qwen2.5-Coder 14B |
| Moteur IA | Ollama |
| Conteneurisation | Docker |
| Documentation | Markdown |
| IDE | IntelliJ IDEA |

---

## Statut du projet

Phase actuelle : prototype fonctionnel.

La plateforme locale est opérationnelle avec :

- Open WebUI comme interface IA ;
- Ollama comme moteur local ;
- Qwen2.5-Coder 14B comme modèle principal ;
- 9 agents IA spécialisés configurés ;
- 10 bases de connaissances créées dans l'espace de travail Open WebUI.

Les prochaines étapes concernent :
- la validation des agents ;
- l'amélioration des connaissances ;
- l'externalisation de la configuration ;
- l'intégration d'une base de connaissances évolutive ;
- la mise en place d'une architecture RAG complète.