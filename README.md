# Macro Planning

Application de macro-planning (Gantt) 100% statique — HTML/CSS/JS, sans backend.

Portée depuis le [Space Hugging Face `WillouDev/macroplanning`](https://huggingface.co/spaces/WillouDev/macroplanning) (qui exécutait cette même page via un wrapper Streamlit) vers un site statique déployable sur GitHub Pages.

## Fonctionnalités

- Vue Gantt et vue Données pour la gestion de phases, tâches et jalons
- Sauvegarde/chargement de plannings au format JSON
- Réglages d'affichage personnalisables (échelle de temps, tailles, couleurs, palette)
- Export du planning en image PNG
- Persistance locale via `localStorage` / `IndexedDB` (navigateur uniquement)
- Import de modèles de planning JSON (`models/`)
- Protection par code d'accès (vérification côté client)

## Développement

Aucune étape de build : `index.html` est la page complète, autonome. Ouvrez-le directement dans un navigateur ou servez le dossier avec n'importe quel serveur statique.

```
python3 -m http.server 8000
```

## Déploiement GitHub Pages

Le déploiement est automatisé via `.github/workflows/pages.yml` (GitHub Actions) sur push vers `main`.

Pour activer GitHub Pages sur ce dépôt (une seule fois) :

1. **Settings → Pages**
2. **Build and deployment → Source : GitHub Actions**

Le site sera ensuite disponible à l'URL fournie par GitHub Pages après le premier déploiement.
