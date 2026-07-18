# Architecture de la plateforme AI Studio

## Présentation

AI Studio repose sur une architecture locale permettant d'exécuter une équipe d'agents IA spécialisés pour accompagner le développement de projets logiciels.

La plateforme sépare :

* l'interface utilisateur ;
* le moteur d'intelligence artificielle ;
* les agents spécialisés ;
* les connaissances générales ;
* la mémoire propre à chaque projet.

Cette séparation permet de construire une plateforme évolutive capable de s'adapter à différents types de projets.

---

# Architecture générale

```text
Utilisateur

    |

    v

Navigateur Web

    |

    v

Open WebUI
Interface IA

    |

    v

Orchestration des Agents IA

    |

    +------------------------------+
    |                              |
    v                              v

Agents IA spécialisés        Base de connaissances

    |                              |
    |                              |
    +--------------+---------------+

                   |

                   v

          Mémoire projet (future)

                   |

                   v

          Base de données projet
          Base vectorielle (RAG)

                   |

                   v

               Ollama

                   |

                   v

          Modèle IA local
          Qwen2.5-Coder 14B
```

---

# Composants principaux

## Open WebUI

Open WebUI constitue l'interface utilisateur de la plateforme.

Il permet :

* d'interagir avec les agents IA ;
* de gérer les conversations ;
* d'accéder aux connaissances ;
* de configurer les espaces de travail.

---

## Agents IA spécialisés

Les agents représentent les différents rôles d'une équipe de développement :

* Product Owner ;
* Research Analyst ;
* Architecte ;
* Backend Developer ;
* Frontend Developer ;
* DevOps ;
* QA ;
* Security Engineer ;
* Technical Writer.

Chaque agent possède des responsabilités et des connaissances adaptées à son domaine.

---

## Base de connaissances

La base de connaissances contient les savoirs généraux utilisés par les agents.

Elle comprend notamment :

* méthodologie projet ;
* analyse métier ;
* architecture ;
* développement ;
* bases de données ;
* DevOps ;
* sécurité ;
* tests ;
* documentation.

Ces connaissances sont indépendantes des projets.

---

## Mémoire projet

La mémoire projet permettra de conserver les informations spécifiques à chaque application développée.

Elle pourra contenir :

* besoins utilisateurs ;
* décisions techniques ;
* architecture choisie ;
* documentation ;
* historique des évolutions.

Contrairement aux connaissances générales, cette mémoire sera propre à chaque projet.

---

## Architecture RAG

L'architecture RAG permettra aux agents de retrouver les informations pertinentes au moment où elles sont nécessaires.

Fonctionnement :

1. Les documents sont analysés.
2. Les informations sont transformées en vecteurs.
3. Les vecteurs sont stockés dans une base vectorielle.
4. L'agent recherche les informations utiles.
5. Le modèle IA utilise ces informations pour répondre.

---

## Moteur IA local

La plateforme utilise :

* Ollama comme moteur d'exécution ;
* Qwen2.5-Coder 14B comme modèle principal.

L'exécution locale permet :

* la confidentialité des données ;
* l'indépendance vis-à-vis des services externes ;
* le contrôle de l'environnement.

---

# Évolution prévue

L'architecture évoluera progressivement avec :

* une base PostgreSQL pour les données structurées ;
* une base vectorielle pour le RAG ;
* une mémoire projet persistante ;
* une orchestration avancée entre agents ;
* une intégration avec les outils de développement.
