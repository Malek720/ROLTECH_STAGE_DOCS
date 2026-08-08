# Exigences fonctionnelles détaillées

Chaque objectif du sujet est décliné en exigences fonctionnelles avec
critères d'acceptation. À affiner après la visite terrain.

## OBJ-1 — Recensement du parc machines

| ID | Exigence | Critère d'acceptation |
|---|---|---|
| F1.1 | Créer/modifier/supprimer une fiche machine | Champs : nom, modèle, n° de série, date d'installation, catégorie, atelier/emplacement |
| F1.2 | Consulter l'historique d'une machine | Liste chronologique des pannes/interventions liées |
| F1.3 | Rechercher/filtrer les machines | Par catégorie, statut, atelier |

## OBJ-2 — Pannes et interventions

| ID | Exigence | Critère d'acceptation |
|---|---|---|
| F2.1 | Déclarer une panne | Machine, date, description, gravité |
| F2.2 | Enregistrer une intervention | Type (préventive/curative), technicien assigné, date début/fin, statut |
| F2.3 | Lier une intervention à une panne | *(dépend de la réponse à la question ouverte sur le modèle Panne/Intervention)* |

## OBJ-3 — Suivi de l'état des machines

| ID | Exigence | Critère d'acceptation |
|---|---|---|
| F3.1 | Statut machine en temps réel | En service / en panne / en maintenance |
| F3.2 | Historique des changements de statut | Traçabilité des transitions avec horodatage |

## OBJ-4 — Tableaux de bord

| ID | Exigence | Critère d'acceptation |
|---|---|---|
| F4.1 | Indicateur de disponibilité | *(formule à confirmer : ex. temps en service / temps total)* |
| F4.2 | Fréquence des pannes | Par machine, par période |
| F4.3 | Vue synthétique | Dashboard responsable avec filtres date/atelier |

## OBJ-5 — Gestion des utilisateurs

| ID | Exigence | Critère d'acceptation |
|---|---|---|
| F5.1 | Authentification | Login sécurisé (Symfony Security) |
| F5.2 | Gestion des rôles | Technicien / Responsable (+ rôles à confirmer) |
| F5.3 | Contrôle d'accès | Restriction des actions/pages selon le rôle |
