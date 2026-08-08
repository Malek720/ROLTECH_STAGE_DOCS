# Cahier des charges

> Statut : 🟡 en cours de rédaction (S1)

## 1. Contexte et objectifs

*(à reformuler après la réunion de cadrage — voir [compte-rendu kickoff](../meetings/2026-08-kickoff.md))*

Entreprise de fabrication de machines industrielles. Le suivi de l'état des
équipements, des pannes et des interventions est aujourd'hui géré de façon
manuelle (papier, Excel), causant une perte de traçabilité et des retards de
décision.

## 2. Périmètre fonctionnel

Voir [objectifs.md](objectifs.md) pour le détail des exigences fonctionnelles
dérivées des 5 points du sujet.

## 3. Acteurs et rôles

| Rôle | Description | Actions principales |
|---|---|---|
| Technicien | Intervient sur les machines | Signaler une panne, saisir une intervention |
| Responsable | Supervise l'activité maintenance | Consulter le dashboard, assigner les interventions, gérer les utilisateurs |
| *(à confirmer)* Admin | Gestion technique de la plateforme | Gestion des comptes, paramétrage |

*(à confirmer en réunion — combien de rôles réels, et leurs permissions exactes)*

## 4. Contraintes techniques

- Backend : Symfony (PHP)
- Base de données : MySQL
- Versioning : Git
- Application **web** (confirmer s'il y a un besoin desktop/mobile en plus)

## 5. Périmètre exclu / hors scope

*(à définir — ex : gestion des stocks de pièces détachées, commande fournisseurs, etc.)*

## 6. Livrables par sprint

Voir planning dans [index général](../index.md#planning).

## Questions ouvertes

- [ ] Panne et Intervention : entités séparées ou intervention = clôture d'une panne ?
- [ ] Combien de machines dans le parc actuel ?
- [ ] Existe-t-il un fichier Excel/registre papier récupérable comme base de données de départ ?
- [ ] Définition exacte des indicateurs de disponibilité attendus (uptime %, MTBF, MTTR, fréquence de pannes)
- [ ] Rôles utilisateurs : liste exhaustive et permissions par rôle
