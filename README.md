# devops

# Pour la 1ere partie : 

1- a -Pour sécuriser nos communications avec des dépôts Git distants, commencez par générer une clé SSH.
En utilisant la commande suivante :ssh-keygen -t rsa -b 4096 -C waad.houij@gmail.com.

b- Après avoir généré clé SSH, affichez la clé publique à l'écran avec la commande suivante :cat ~/.ssh/id_rsa.pub
  => Copiez cette clé publique, car nous en aurons besoin pour la prochaine étape.

c. Ajout de la clé publique SSH sur le dépôt distant
Connectons-nous à notre compte sur le dépôt distant, par exemple GitHub, et accédons aux paramètres de notre compte. 
Nous trouverons une section pour ajouter des clés SSH. 
Collons-y la clé publique que nous avons copiée précédemment. Cela permettra à Git d'authentifier notre machine auprès du dépôt distant

2. Configuration de Git
Maintenant que nous avons configuré notre clé SSH, il est temps de configurer notre nom et notre adresse e-mail pour que nos commits soient correctement identifiés. 
Utilisez les commandes suivantes 
git config --global user.name "Waad"
git config --global user.email waad.houij@gmail.com


3. Connexion SSH aux dépôts distants
Pour tester notre connexion SSH et pour assurer que tout fonctionne correctement, on utilise la commande 
suivante :
ssh -T git@github.com
Cela devrait afficher un message de confirmation de la connexion réussie.




# Préparation de l'environnement Git - Partie 2: Création d'un nouveau projet

Cette partie de notre guide se concentre sur la création d'un nouveau projet Git. 
Vous apprendrez comment configurer votre projet sur GitHub, 
cloner ce projet sur notre machine locale, et accéder au répertoire du projet pour commencer à travailler.

# Préparation de l'environnement Git - Partie 3 : Concepts de base de Git


1 - nous allons créer un fichier nommé index.html dans le répertoire de notre projet et y ajouter du contenu. Voici comment procéder :# Créez le fichier index.html
touch index.html

# Ajoutez du contenu au fichier
echo "Contenu de votre fichier" > index.html

Ensuite, pour enregistrer ces modifications, nous utilisons les commandes suivantes :
# Ajoutez le fichier index.html à l'index (staging)
git add index.html

# Validez vos modifications en effectuant un commit
git commit -m "Premier commit : ajout de index.html"

==> Cela crée un commit qui enregistre les changements que nous avons effectués.


2. Historique des commits:

Utilisez la commande suivante pour visualiser l'historique des commits :
git log

De plus, si nous souhaitons comparer les différences entre deux commits spécifiques,
 nous pouvons utiliser la commande suivante en remplaçant commit_id_1 et commit_id_2 par les identifiants des commits que nous souhaitons comparer :

git diff commit_id_1 commit_id_2








