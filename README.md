# ROLTECH_STAGE_DOCS

Documentation du stage réalisé chez **Roller Technology Systems Industry** —
projet **GMAO Simplifiée** (supervision et maintenance des machines industrielles).

Site généré avec [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

## Contenu

- Cahier des charges
- Modélisation UML (cas d'utilisation, classes, séquence)
- Comptes-rendus de réunion
- Journal de stage
- Démonstration vidéo du prototype

## Dépôt de code

Le code source de l'application (Symfony + MySQL) se trouve dans un dépôt séparé :

[GitHub — Malek720/ROLTECH_GMAO](https://github.com/Malek720/ROLTECH_GMAO)

## Aperçu local

```bash
python -m venv .venv
.venv\Scripts\activate      # Linux/macOS : source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Ouvre ensuite `http://127.0.0.1:8000` (ou le port indiqué).

## Déploiement

Un push sur `main` déclenche automatiquement le déploiement sur GitHub Pages
via `.github/workflows/deploy.yml`.
