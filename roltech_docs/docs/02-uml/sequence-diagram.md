# Diagramme de séquence — Signalement et résolution d'une panne

> Flux clé à valider ; sert à détecter les cas limites (ex. statut machine
> pendant une intervention en cours).

```mermaid
sequenceDiagram
  actor T as Technicien
  actor R as Responsable
  participant S as Système

  T->>S: Signale une panne (machine, description, gravité)
  S->>S: Met à jour statut machine = "en panne"
  S-->>R: Notifie la nouvelle panne
  R->>S: Assigne une intervention (technicien, type)
  S->>S: Met à jour statut machine = "en maintenance"
  T->>S: Clôture l'intervention (date fin, commentaire)
  S->>S: Met à jour statut machine = "en service"
  S-->>R: Notifie la clôture
```

## Cas limites à clarifier

- Que se passe-t-il si une machine a plusieurs pannes ouvertes simultanément ?
- Le responsable peut-il refuser/réassigner une intervention ?
- Y a-t-il une validation finale du responsable avant clôture définitive ?
