# Pokedex_exec

Partie 1 
   1. Créez un dépôt sur votre compte GitHub
   2. A l'aide du didacticiel sur les GitHub Actions. Ajoutez l'action en exemple dans votre projet
   3. Ajoutez une commande Linux de votre choix à votre fichier d'Actions et observez le résultat dans GitHub

Partie 2
   1. Remplacez le contenu du dépôt crée précédemment par un projet npm (commande npm init --y).
   2. Installez les dépendances suivantes :
    release-it
        Pensez à sélectionner ".release-it.json" lors de l'installation avec la commande npm init release-it, sinon créez vous-même le fichier à la racine en vous aidant de la documentation
    @release-it/conventional-changelog
   3. Testez la tâche de release depuis la ligne de commandes, elle a été ajoutée dans votre fichier package.json.
   4. Editez le fichier de pipeline crée précédemment ou créez-en un nouveau pour effectuer une release de votre projet. Pour ce faire voici les tâches que doit accomplir votre pipeline :
      1. Cloner le projet : actions/checkout@v4. C'est une action prédéfinie, il faudra utiliser la clé "uses" à la place de "run"
      2. Installer des dépendances : npm ci ("ci" fait un "clean install")
      3. Définir l'utilisateur git : git config user.email / user.name
      4. Définir une version de node supérieure ou égale à la version 20 grâce à l'action "setup-node"
      5. Mettre à jour la version : npm run release --ci 
