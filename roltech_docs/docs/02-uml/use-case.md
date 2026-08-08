# Diagramme de cas d'utilisation

> Brouillon initial — à valider après la réunion de cadrage.

```mermaid
graph LR
  Technicien((Technicien))
  Responsable((Responsable))

  Technicien --> UC1[Signaler une panne]
  Technicien --> UC2[Saisir une intervention]
  Technicien --> UC3[Consulter historique machine]

  Responsable --> UC4[Consulter dashboard]
  Responsable --> UC5[Assigner une intervention]
  Responsable --> UC6[Gérer les utilisateurs]
  Responsable --> UC7[Gérer le parc machines]
  Responsable --> UC3
```

## Notes

- Confirmer si le technicien peut aussi créer/modifier une fiche machine
  ou si c'est réservé au responsable.
- Confirmer l'existence d'un rôle admin distinct.
