# Data-eyes

Bienvenue dans le dépôt **Data-eyes** ! Ce projet fait partie d'un parcours d'apprentissage en Python, conçu pour vous aider à maîtriser la manipulation de données tout en créant un outil pratique pour gérer des données tabulaires. Ici, vous allez construire une interface web pour travailler avec des fichiers de données structurées et générer des requêtes SQL, tout en gardant les choses simples et utiles.

---

## 📚 **Aperçu du Projet**

**Data-eyes** vous permet de :  
- Charger et explorer des données tabulaires à partir de fichiers CSV et JSON.  
- Filtrer, trier et analyser les données via une interface web intuitive.  
- Générer des requêtes SQL basées sur vos actions, exportables pour une utilisation réelle.  

C'est un projet pratique pour renforcer vos compétences en Python et fournir une alternative légère aux outils d'intelligence d'affaires coûteux, particulièrement précieuse dans les environnements à ressources limitées.

---

## ⚙️ **Implémentation Actuelle**

1. **Gestion des Données :**  
   - Traite les fichiers CSV et JSON en utilisant les modules intégrés de Python.  
   - Affiche les données dans un format tabulaire avec des capacités basiques de filtrage et de tri.  

2. **Interface Web :**  
   - Construite avec FastAPI pour le backend et les templates Jinja2 pour le rendu HTML.  
   - Descriptions en Markdown rendues avec Markdown-it sur le frontend.  

3. **Génération SQL :**  
   - Traduit les actions utilisateur en requêtes SQL, stockées pour export ou réutilisation.  

---

## 🛠 **Stack Technologique**

- **Backend :**  
  - Python 3.10+  
  - FastAPI comme framework web  
  - Modules Python intégrés (`csv`, `json`) pour le traitement des données  

- **Frontend :**  
  - HTML/CSS pour la mise en page et le style  
  - Jinja2 pour le templating  
  - Markdown-it pour rendre le contenu Markdown  

- **Outils de Développement :**  
  - Poetry pour la gestion des dépendances  
  - Ruff pour le linting  
  - MyPy pour la vérification des types  

---

## 📂 **Fonctionnalités Clés**

- **Chargement de Données :** Importez sans effort des fichiers CSV et JSON pour commencer à travailler avec vos données.  
- **Interface Interactive :** Visualisez vos données dans un tableau, appliquez des filtres et triez les colonnes en quelques clics.  
- **Export SQL :** Transformez vos actions en requêtes SQL, parfaites pour une utilisation dans des bases de données ou pour partager avec d'autres.  

---

## 🤝 **Contribuer**

Vos idées et efforts sont chaleureusement accueillis ! Jetez un œil à notre [Guide de Contribution](CONTRIBUTING.fr.md) pour voir comment vous pouvez :  
- Configurer le projet sur votre propre système  
- Suivre notre flux de développement  
- Respecter nos directives de style de code  
- Ajouter de nouvelles fonctionnalités ou améliorer ce qui existe déjà  

Voici quelques façons dont vous pourriez aider :  
- Ajouter plus d'options de filtrage pour rendre l'exploration de données encore plus riche.  
- Améliorer le générateur SQL pour des requêtes plus complexes.  
- Prendre en charge des formats de fichiers supplémentaires si vous vous sentez inspiré.  
- Polir l'interface pour la rendre encore plus conviviale.  

---

## 🧑‍💻 **À Propos de l'Auteur**

Ce projet vous est proposé par **Hugues Dtankouo**, un Développeur Full Stack Senior qui croit au pouvoir de Python pour résoudre de vrais problèmes et inspirer la croissance.  

📧 **Contact :** [huguesdtankouo@gmail.com](mailto:huguesdtankouo@gmail.com)  
🔗 **LinkedIn :** [Hugues Dtankouo](https://www.linkedin.com/in/dtankouo)  
🔗 **GitHub :** [Hugues-DTANKOUO](https://github.com/Hugues-DTANKOUO)  

---

## 📄 **Licence & Documentation**

- **Licence :** [Licence MIT](LICENSE) – n'hésitez pas à utiliser, adapter et partager ce travail.  
- **Journal des Modifications :** [CHANGELOG.md](CHANGELOG.md) – un registre de notre progression commune.  

---

## 🚧 **État du Projet**

*Data-eyes* en est à ses débuts, avec les éléments fondamentaux déjà en place. Dans l'avenir, nous pourrions :  
- Ajouter des outils pour résumer les données (comme des totaux ou des moyennes).  
- Améliorer la manière dont nous exportons les requêtes et les résultats.  
- Rendre l'interface encore plus fluide et accueillante.  

Vos réflexions aideront à guider la direction que nous prendrons ensuite !

---

## 🎯 **Focus Actuel**

En ce moment, nous nous concentrons sur :  
1. S'assurer que le chargement et l'affichage des données fonctionnent parfaitement.  
2. Perfectionner la génération SQL pour qu'elle soit précise et utile.  
3. Rédiger une documentation claire pour soutenir votre apprentissage.  
4. Tester avec des données réelles pour s'assurer que cela répond à vos besoins.  

---

Merci de faire partie de ce voyage ! Construisons ensemble un outil qui fait travailler les données pour tout le monde – j'ai hâte de voir ce que nous créerons ensemble.