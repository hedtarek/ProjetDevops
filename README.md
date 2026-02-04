# ProjetDevops
ProjetDevops
🎯 En une phrase (vision globale)

AudioProthèse+ est un projet de modernisation complète d’une infrastructure informatique de santé, basé sur une approche DevSecOps, visant à héberger et sécuriser une application médicale (OpenMRS) tout en respectant les exigences RGPD et données de santé, avec un haut niveau de sécurité, automatisation, résilience et observabilité.

🏥 Contexte métier (le “pourquoi”)

AudioProthèse+ est un réseau national de centres d’audioprothèse qui :

manipule des données médicales sensibles

utilise des équipements médicaux connectés

est exposé à des risques cyber élevés

doit respecter des réglementations strictes (RGPD, HDS)

👉 L’infrastructure historique n’est plus suffisante face :

à l’augmentation des cyberattaques dans la santé

aux exigences de disponibilité

à la nécessité d’audits, de traçabilité et de conformité

🧠 Objectif principal du projet

Mettre en place une infrastructure IT moderne, capable de :

🔐 Sécuriser les données médicales

🚀 Automatiser les déploiements applicatifs

👀 Offrir une visibilité complète (logs, métriques, alertes)

🔄 Garantir la haute disponibilité et la résilience

📜 Être conforme aux normes santé et RGPD

💰 Optimiser les coûts sur le long terme

🧩 Application cœur du projet : OpenMRS

OpenMRS est utilisée comme application de référence :

Dossier Médical Électronique (EMR)

Open source

Représentative d’un vrai SI de santé

Forte contrainte de sécurité et de disponibilité

👉 Elle sert de cas d’usage concret pour démontrer l’architecture DevSecOps
👉 L’architecture est réutilisable pour d’autres applications médicales

🏗️ Les 3 scénarios d’architecture

Le projet n’impose pas une seule solution : il compare 3 modèles.

1️⃣ On-Premise

Tout est hébergé dans le datacenter interne.

Idéal si :

contrôle total des données

exigences réglementaires très fortes

faible dépendance au cloud

2️⃣ Hybride (le plus réaliste)

Données médicales critiques on-premise

Outils transverses dans le cloud

Exemples cloud :

observabilité

CI/CD

sauvegardes

PRA

👉 Excellent compromis sécurité / coût / flexibilité

3️⃣ Full Cloud

Tout est hébergé dans le cloud (Kubernetes managé, DB managée).

Avantages :

scalabilité

haute disponibilité

moins d’exploitation

⚠️ Attention forte à la conformité HDS / RGPD

🔐 Sécurité : pilier central du projet

La sécurité n’est pas ajoutée après, elle est intégrée partout (DevSecOps).

Principes clés

Chiffrement partout (TLS 1.3, AES-256)

Zero Trust / segmentation réseau

mTLS entre services

Gestion sécurisée des secrets

Journalisation complète et immuable

Scans de vulnérabilités automatisés

👉 Chaque déploiement est contrôlé automatiquement avant d’arriver en production.

🔁 DevSecOps & automatisation

L’infrastructure est décrite entièrement en code.

Infrastructure as Code

Terraform → infra

Ansible → configuration

Helm → applications Kubernetes

GitOps → déploiements contrôlés via Git

👉 Résultat :

reproductible

traçable

auditable

rapide à restaurer

🔍 Observabilité (voir avant que ça casse)

Le projet met en place une supervision centralisée :

📊 Métriques : Prometheus + Grafana

📜 Logs : Loki / ELK

🔗 Traces : Jaeger / Tempo

🚨 Alertes : Alertmanager, Slack, PagerDuty

👉 Objectif :
détecter un incident avant que le personnel médical ne le ressente

🧯 Résilience & continuité de service

Le projet prévoit :

haute disponibilité multi-zones

sauvegardes automatisées

PRA / PCA

tests de résilience (chaos engineering)

👉 Le système doit continuer à fonctionner même en cas de panne

📜 Conformité réglementaire (point clé santé)

Le projet couvre :

RGPD (consentement, traçabilité, droit à l’oubli)

Hébergement Données de Santé (HDS)

ISO 27001

audits et journaux immuables

👉 La conformité est automatisée dans les pipelines CI/CD.

📦 Livrables finaux

À la fin du projet, on obtient :

une plateforme DevSecOps fonctionnelle

une infra Kubernetes sécurisée

des pipelines CI/CD automatisés

une supervision complète

une documentation exploitable

un MVP démontrable

👉 Projet prêt pour exploitation réelle ou démonstration professionnelle
