# Diagramme de classes

> Brouillon initial — hypothèse de modèle, à valider en réunion
> (notamment la relation Panne ↔ Intervention).

```mermaid
classDiagram
  class Machine {
    +int id
    +string nom
    +string modele
    +string numeroSerie
    +date dateInstallation
    +string categorie
    +string emplacement
    +string statut
  }

  class Panne {
    +int id
    +date dateSignalement
    +string description
    +string gravite
    +string statut
  }

  class Intervention {
    +int id
    +string type
    +date dateDebut
    +date dateFin
    +string statut
    +string commentaire
  }

  class User {
    +int id
    +string nom
    +string email
    +string motDePasseHash
    +string role
  }

  Machine "1" --> "*" Panne : subit
  Panne "1" --> "1..*" Intervention : résolue par
  User "1" --> "*" Intervention : réalise
  User "1" --> "*" Panne : signale
```

## Notes / hypothèses à confirmer

- Une panne peut-elle avoir plusieurs interventions (ex. intervention
  partielle puis complémentaire) ou est-ce toujours 1↔1 ?
- Le champ `statut` de `Machine` doit-il être dérivé automatiquement du
  statut des pannes/interventions en cours, ou géré manuellement ?
- Faut-il une entité `Atelier`/`Site` séparée si plusieurs emplacements physiques ?
