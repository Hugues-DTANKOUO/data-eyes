# Data-eyes - Guide du Développeur

Ce document est destiné aux développeurs qui souhaitent contribuer au projet Data-eyes. Pour une présentation générale du projet, veuillez consulter le [README principal](../README.fr.md).

## Environnement de développement

### Configuration requise

- Python 3.10+
- Git
- Poetry 1.5+
- Un éditeur de code (VS Code recommandé)

### Configuration initiale

1. Cloner le dépôt et se positionner dans le répertoire du projet:
   ```bash
   git clone https://github.com/Hugues-DTANKOUO/data-eyes.git
   cd data-eyes
   ```

2. Installer les dépendances avec Poetry:
   ```bash
   poetry install
   ```

3. Activer l'environnement virtuel:
   ```bash
   poetry shell
   ```

## Structure du projet

La structure présentée ci-dessous est préliminaire et évoluera avec le développement du projet:

```
data-eyes/
├── src/                # Code source
│   └── data_eyes/      # Module principal
│       ├── interface.py    # Point d'entrée FastAPI
│       ├── processors/     # Traitement des formats de données
│       ├── static/         # Fichiers statiques (CSS, JS)
│       └── templates/      # Templates Jinja2
├── tests/              # Tests automatisés
├── docs/               # Documentation
│   └── architecture.md     # Documentation de l'architecture
└── README.md
```

## Environnement de développement VS Code

Si vous utilisez VS Code, voici la configuration recommandée pour ce projet. Créez un dossier `.vscode` et ajoutez-y un fichier `settings.json` avec le contenu suivant:

```json
{
    "python.linting.enabled": true,
    "python.linting.ruffEnabled": true,
    "editor.formatOnSave": true,
    "python.formatting.provider": "ruff",
    "python.testing.pytestEnabled": true,
    "plantuml.server": "http://www.plantuml.com/plantuml",
    "[python]": {
        "editor.defaultFormatter": "charliermarsh.ruff",
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true,
            "source.fixAll": true
        }
    }
}
```

## Scripts de développement

Ce projet inclura plusieurs scripts utilitaires pour faciliter le développement:

```bash
# Lancer le serveur de développement
poetry run server

# Exécuter les tests
poetry run tests

# Exécuter le linting et la vérification des types
poetry run lint

# Exécuter toutes les vérifications (lint + tests)
poetry run check
```

## Workflow de développement

1. **Créer une branche de fonctionnalité**:
   ```bash
   git checkout -b feature/nom-de-la-fonctionnalite
   ```

2. **Développer et tester localement**:
   ```bash
   # Lancer le serveur pour voir les changements
   poetry run server
   
   # Vérifier que les tests passent
   poetry run tests
   ```

3. **Committer les changements**:
   ```bash
   git add .
   git commit -m "Description claire des changements"
   ```

4. **Pousser la branche**:
   ```bash
   git push origin feature/nom-de-la-fonctionnalite
   ```

5. **Créer une Pull Request** sur GitHub.

## API envisagées

Voici les principaux points de terminaison prévus pour l'API:

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| GET | `/` | Page d'accueil |
| GET | `/upload` | Page d'upload |
| GET | `/schema` | Page de génération de schéma |
| POST | `/api/data/upload` | Upload d'un fichier |
| GET | `/api/data/preview` | Aperçu des données |
| POST | `/api/schema/generate` | Génération d'un schéma SQL |
| GET | `/api/schema/export` | Export du schéma |

## Standards de code

### Style de code

- Suivre PEP 8 pour le style Python
- Utiliser des annotations de type pour toutes les fonctions
- Documenter toutes les classes et méthodes avec des docstrings
- Nommer les variables et fonctions en snake_case
- Nommer les classes en PascalCase

### Docstrings

Utilisez le format suivant pour les docstrings:

```python
def function_name(param1: str, param2: int) -> bool:
    """
    Description claire de ce que fait la fonction.

    :param param1: Description du premier paramètre
    :param param2: Description du deuxième paramètre
    :return: Description de la valeur de retour
    """
```

### Tests

- Tous les modules doivent avoir des tests associés
- Utiliser pytest pour les tests
- Nommer les fichiers de test avec le préfixe `test_`

## Principes architecturaux

- **Modularité**: Séparer les responsabilités dans des modules distincts
- **Extensibilité**: Permettre l'ajout facile de nouveaux formats et fonctionnalités
- **Interface claire**: Définir des interfaces précises entre les composants
- **Tests unitaires**: Couvrir le code avec des tests automatisés
- **Documentation**: Documenter les API et les fonctionnalités

## Ressources de développement

- [Documentation FastAPI](https://fastapi.tiangolo.com/)
- [Documentation Jinja2](https://jinja.palletsprojects.com/)
- [Documentation Poetry](https://python-poetry.org/docs/)
- [Guide des types en Python](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

---

Pour toute question supplémentaire, n'hésitez pas à ouvrir une issue sur GitHub ou à contacter directement @Hugues-DTANKOUO.