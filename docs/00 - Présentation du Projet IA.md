# AI Studio

## Présentation

AI Studio est une plateforme locale d'ingénierie logicielle assistée par intelligence artificielle.

L'objectif du projet est de créer un environnement capable d'accompagner les différentes phases de création d'un logiciel grâce à une équipe d'agents IA spécialisés.

La plateforme simule une équipe technique complète composée de plusieurs experts capables de collaborer autour d'un projet :

* analyse métier ;
* recherche technique ;
* architecture ;
* développement ;
* sécurité ;
* qualité ;
* déploiement ;
* documentation.

---

# Vision du projet

Le développement logiciel nécessite aujourd'hui de nombreuses compétences complémentaires.

AI Studio vise à créer un environnement dans lequel plusieurs agents IA spécialisés peuvent collaborer afin de reproduire le fonctionnement d'une équipe d'ingénierie logicielle.

Chaque agent possède :

* un rôle défini ;
* une expertise spécifique ;
* des connaissances adaptées à son domaine ;
* une capacité à collaborer avec les autres agents.

---

# Objectifs

AI Studio permet de :

* transformer une idée en projet structuré ;
* analyser les besoins utilisateurs ;
* concevoir une architecture logicielle ;
* accompagner les phases de développement ;
* améliorer la qualité du code ;
* appliquer les bonnes pratiques de sécurité ;
* automatiser certaines tâches techniques ;
* produire une documentation complète.

---

# Fonctionnement général

Le fonctionnement repose sur plusieurs éléments :

## Agents IA spécialisés

Chaque agent intervient selon son domaine d'expertise.

Exemple :

```text id="5a7u2c"
Besoin utilisateur

        │

        ▼

Product Owner

        │

        ▼

Architecte

        │

        ▼

Développeurs

        │

        ▼

QA / Sécurité

        │

        ▼

DevOps

        │

        ▼

Documentation
```

---

# Connaissances des agents

Les agents utilisent une base de connaissances commune regroupant les fondamentaux de l'ingénierie logicielle.

Elle comprend :

* Méthodologie Projet Logiciel ;
* Analyse Métier et Besoins ;
* Architecture ;
* Développement Backend ;
* Développement Frontend ;
* Bases de Données ;
* DevOps et Infrastructure ;
* Sécurité Applicative ;
* Tests et Qualité Logicielle ;
* Documentation Technique.

Ces connaissances permettent aux agents d'être polyvalents et de s'adapter à différents types de projets.

---

# Mémoire projet et évolution future

Chaque projet accompagné par AI Studio pourra disposer progressivement de sa propre mémoire.

Cette mémoire permettra de conserver :

* les besoins du projet ;
* les décisions techniques ;
* l'architecture choisie ;
* les modèles de données ;
* les documents produits ;
* l'historique des évolutions.

Cette évolution s'appuiera sur une architecture RAG permettant aux agents de retrouver les informations pertinentes au moment où elles sont nécessaires.

---

# Architecture technique actuelle

La plateforme utilise actuellement :

* Open WebUI comme interface utilisateur IA ;
* Ollama comme moteur local d'exécution ;
* Qwen2.5-Coder 14B comme modèle IA ;
* Docker pour l'environnement d'exécution.

---

# Évolutions prévues

Les prochaines étapes du projet comprennent :

* mise en place d'une base de données projet ;
* intégration d'une base vectorielle ;
* amélioration de la mémoire des agents ;
* orchestration de la collaboration entre agents ;
* automatisation des workflows ;
* intégration avec les outils de développement.

---

# Conclusion

AI Studio a pour ambition de devenir une plateforme locale permettant à une équipe d'agents IA spécialisés d'accompagner la conception et l'évolution de projets logiciels complets.

Le projet évolue progressivement vers un environnement d'ingénierie logicielle assistée par intelligence artificielle.
