# Projet de Monitoring avec Prometheus et Grafana

## Contexte
Ce projet a été réalisé dans le cadre d’une montée en compétences en DevOps, Cloud et Cybersécurité.
L’objectif est de mettre en place une solution de monitoring similaire à celles utilisées en entreprise,
afin de superviser une application et les ressources système associées.

## Objectifs du projet
- Comprendre le fonctionnement d’une solution de monitoring moderne
- Collecter des métriques système (CPU, mémoire, disque, réseau)
- Visualiser les métriques en temps réel
- Observer le comportement d’un système sous charge
- Documenter une architecture technique de manière professionnelle

## Architecture de la solution
La solution repose sur les composants suivants :
- Nginx : application web servant de service à surveiller
- Node Exporter : collecte des métriques système de la machine hôte
- Prometheus : collecte, stockage et interrogation des métriques
- Grafana : visualisation des métriques sous forme de tableaux de bord
L’ensemble des services est déployé et orchestré avec Docker Compose.

## Technologies utilisées
- Docker
- Docker Compose
- Prometheus
- Grafana
- Node Exporter
- Nginx
- Environnement Linux (WSL)

## Déploiement du projet
Lancer la stack :
```bash
docker compose up -d

## Vérifier les conteneurs
docker ps

## Accès aux services 
Application Nginx : http://localhost:8080
Prometheus : http://localhost:9090
Grafana : http://localhost:3000
Identifiants Grafana :
utilisateur : admin
mot de passe : admin

## Visualisation métrique
Un dashboard Grafana a été importé afin de visualiser les métriques système.
Dashboard utilisé :
Node Exporter Full
ID : 1860
Métriques observées :
CPU
Mémoire RAM
Disque
Réseau

## Tests et Observations
Des tests de charge ont été réalisés afin d’observer le comportement du système.
Les variations de consommation CPU et mémoire sont visibles en temps réel dans Grafana,
ce qui valide la bonne collecte des métriques par Prometheus.

## Améliorations possibles
Ajout d’Alertmanager pour la gestion des alertes
Mise en place de notifications (email, Slack)
Supervision applicative avancée
Déploiement sur un environnement Cloud (Azure ou AWS)

