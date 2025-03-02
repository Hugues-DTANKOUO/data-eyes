# Guide de contribution à un dépôt GitHub

Ce guide explique comment contribuer à un dépôt public GitHub, avec et sans Visual Studio Code.

## Table des matières

- [Prérequis](#prérequis)
- [Contribuer sans VS Code](#contribuer-sans-vs-code)
  - [1. Forker le dépôt](#1-forker-le-dépôt)
  - [2. Cloner votre fork](#2-cloner-votre-fork)
  - [3. Créer une branche](#3-créer-une-branche)
  - [4. Apporter vos modifications](#4-apporter-vos-modifications)
  - [5. Ajouter et valider vos modifications](#5-ajouter-et-valider-vos-modifications)
  - [6. Pousser vos modifications](#6-pousser-vos-modifications)
  - [7. Créer une Pull Request](#7-créer-une-pull-request)
- [Contribuer avec VS Code](#contribuer-avec-vs-code)
  - [1. Forker le dépôt](#1-forker-le-dépôt-avec-vs-code)
  - [2. Cloner dans VS Code](#2-cloner-dans-vs-code)
  - [3. Créer une branche dans VS Code](#3-créer-une-branche-dans-vs-code)
  - [4. Apporter vos modifications dans VS Code](#4-apporter-vos-modifications-dans-vs-code)
  - [5. Gestion des changements avec l'interface Git de VS Code](#5-gestion-des-changements-avec-linterface-git-de-vs-code)
  - [6. Pousser vos modifications avec VS Code](#6-pousser-vos-modifications-avec-vs-code)
  - [7. Créer une Pull Request depuis VS Code](#7-créer-une-pull-request-depuis-vs-code)
- [Bonnes pratiques de contribution](#bonnes-pratiques-de-contribution)
- [Résoudre les conflits](#résoudre-les-conflits)

## Prérequis

Avant de commencer, assurez-vous d'avoir :

- Un compte GitHub
- Git installé sur votre machine ([télécharger Git](https://git-scm.com/downloads))
- Si vous utilisez VS Code, assurez-vous qu'il est installé ([télécharger VS Code](https://code.visualstudio.com/download))

## Contribuer sans VS Code

### 1. Forker le dépôt

1. Accédez au dépôt GitHub auquel vous souhaitez contribuer
2. Cliquez sur le bouton "Fork" en haut à droite de la page
3. Sélectionnez votre compte comme destination du fork

### 2. Cloner votre fork

```bash
# Remplacez USERNAME par votre nom d'utilisateur GitHub
# Remplacez REPOSITORY par le nom du dépôt
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
```

### 3. Créer une branche

```bash
# Assurez-vous d'être à jour avec le dépôt d'origine
git remote add upstream https://github.com/ORIGINAL_OWNER/REPOSITORY.git
git fetch upstream
git checkout main
git pull upstream main

# Créez une nouvelle branche pour votre contribution
git checkout -b nom-de-votre-branche
```

### 4. Apporter vos modifications

Modifiez les fichiers avec votre éditeur de texte préféré.

### 5. Ajouter et valider vos modifications

```bash
# Vérifiez quels fichiers ont été modifiés
git status

# Ajoutez les fichiers modifiés
git add chemin/vers/fichier-modifié
# Ou pour ajouter tous les fichiers modifiés
git add .

# Validez vos modifications avec un message descriptif
git commit -m "Description claire des modifications apportées"
```

### 6. Pousser vos modifications

```bash
git push origin nom-de-votre-branche
```

### 7. Créer une Pull Request

1. Retournez sur votre fork GitHub dans votre navigateur
2. Vous devriez voir un message suggérant de créer une Pull Request pour votre branche récemment poussée
3. Cliquez sur "Compare & pull request"
4. Ajoutez un titre et une description détaillée de vos modifications
5. Cliquez sur "Create pull request"

## Contribuer avec VS Code

### 1. Forker le dépôt avec VS Code

Cette étape se fait dans le navigateur, comme dans la méthode sans VS Code.

### 2. Cloner dans VS Code

1. Ouvrez VS Code
2. Appuyez sur `Ctrl+Shift+P` (ou `Cmd+Shift+P` sur Mac) pour ouvrir la palette de commandes
3. Tapez "Git: Clone" et sélectionnez cette option
4. Entrez l'URL de votre fork (`https://github.com/USERNAME/REPOSITORY.git`)
5. Sélectionnez un dossier local pour y cloner le dépôt
6. Cliquez sur "Ouvrir" lorsque vous y êtes invité

### 3. Créer une branche dans VS Code

1. Cliquez sur le nom de la branche actuelle dans la barre d'état en bas à gauche
2. Dans la palette qui s'ouvre, sélectionnez "+ Créer nouvelle branche"
3. Entrez le nom de votre nouvelle branche et appuyez sur Entrée

Avant cela, vous pouvez configurer le dépôt d'origine :

1. Ouvrez un terminal dans VS Code (`Ctrl+` ou Terminal > Nouveau terminal)
2. Exécutez :
   ```bash
   git remote add upstream https://github.com/ORIGINAL_OWNER/REPOSITORY.git
   git fetch upstream
   git pull upstream main
   ```

### 4. Apporter vos modifications dans VS Code

1. Naviguez dans l'explorateur de fichiers à gauche
2. Ouvrez et modifiez les fichiers selon vos besoins

### 5. Gestion des changements avec l'interface Git de VS Code

1. Cliquez sur l'icône "Contrôle de source" dans la barre latérale (ou appuyez sur `Ctrl+Shift+G`)
2. Vous verrez la liste des fichiers modifiés
3. Passez la souris sur un fichier et cliquez sur le "+" pour l'ajouter à la zone de staging
4. Pour ajouter tous les fichiers, cliquez sur le "+" à côté de "Changements"
5. Entrez un message de commit dans le champ en haut
6. Appuyez sur `Ctrl+Entrée` ou cliquez sur la coche pour valider votre commit

### 6. Pousser vos modifications avec VS Code

1. Cliquez sur les "..." (Plus d'actions) dans la vue Contrôle de source
2. Sélectionnez "Push"
3. S'il s'agit d'une nouvelle branche, VS Code vous demandera si vous souhaitez publier la branche - cliquez sur "OK"

### 7. Créer une Pull Request depuis VS Code

Vous pouvez le faire directement depuis VS Code avec l'extension GitHub Pull Requests :

1. Installez l'extension "GitHub Pull Requests and Issues"
2. Une fois installée, cliquez sur l'icône GitHub dans la barre latérale
3. Sous "Pull Requests", cliquez sur "Create Pull Request"
4. Remplissez les détails de votre PR
5. Cliquez sur "Create"

Alternativement, vous pouvez créer la PR via l'interface web comme dans la méthode sans VS Code.

## Bonnes pratiques de contribution

1. **Nommez clairement votre branche** : utilisez un préfixe comme `feature/`, `bugfix/`, `docs/` suivi d'une description concise.
2. **Faites des commits atomiques** : chaque commit devrait représenter une seule modification logique.
3. **Écrivez des messages de commit clairs** : utilisez l'impératif présent et expliquez le "pourquoi" des changements.
4. **Testez vos modifications** : assurez-vous que vos changements fonctionnent comme prévu.
5. **Suivez les directives de style du projet** : respectez les conventions de code du projet.
6. **Gardez votre PR focalisée** : une PR devrait aborder un seul problème ou fonctionnalité.
7. **Restez à jour** : synchronisez régulièrement votre fork avec le dépôt d'origine.
8. **Répondez aux commentaires** : soyez réactif lors de la revue de code.

## Résoudre les conflits

Si des conflits apparaissent lors de votre contribution, voici comment les résoudre :

### Sans VS Code

```bash
# Mettez à jour votre branche avec la dernière version de main
git fetch upstream
git checkout nom-de-votre-branche
git merge upstream/main

# S'il y a des conflits, Git vous les signalera
# Ouvrez les fichiers concernés et résolvez les conflits manuellement
# Les conflits sont indiqués par <<<<<<< HEAD ... ======= ... >>>>>>> upstream/main

# Une fois les conflits résolus
git add .
git commit -m "Résoudre les conflits de fusion"
git push origin nom-de-votre-branche
```

### Avec VS Code

1. Suivez les mêmes étapes pour mettre à jour votre branche
2. VS Code affichera les conflits avec une interface visuelle
3. Cliquez sur "Accept Current Change", "Accept Incoming Change", "Accept Both Changes" ou modifiez manuellement
4. Une fois tous les conflits résolus, effectuez un commit comme d'habitude

---

Nous apprécions votre intérêt à contribuer à ce projet. Si vous avez des questions ou besoin d'aide, n'hésitez pas à ouvrir une issue ou à contacter les mainteneurs du projet.