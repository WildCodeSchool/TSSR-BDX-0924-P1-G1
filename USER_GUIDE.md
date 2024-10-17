# Documentation Utilisateur : Mode d'emploi

## 1. Utilisation simple : comment effectuer une attaque pour tester la robustesse du mot de passe d'un fichier zippé chiffré sur un serveur  
### >- Localiser le fichier que l’on veut tester  
D’abord vous allez devoir ouvrir le dossier contenant votre archive zip dans un terminal.
Pour celà ouvrez l’explorateur de fichiers présents dans la barre de gauche de votre écran.  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen1.png" width=600></P>  

Selectionnez le dossier qui contient le fameux fichier en faisant un clic droit dessus et selectionnez “Ouvrir dans un terminal”  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen2.png" width=600></P>   

Vous aurez alors un écran pour y saisir des commandes qui ressemble à ca :  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen3.png" width=600></P>  

Ensuite il ne vous restera plus qu'à taper les commandes suivantes :  

    zip2john archive.zip > ZipHash.txt
      
ici nous supposons que votre fichier s'appelle archive.zip, s'il s'agit d'un autre fichier il faudra bien entendu remplacer archive.zip par votre fichier.
Le logiciel John The riper va alors sortir le Hash du mot de passe de ce fichier et c'est avec ce hash que nous essaierons de décrypter le mot de passe du fichier archive.  
  
Une fois cette commande exécutée, il ne vous restera plus qu'à exécuter la commande suivante :  

    john  




## 2. Utilisation avancée : comment effectuer une attaque sur un compte local du serveur

## 3. FAQ : Solutions aux problèmes connus et communs liés à l'utilisation

***Question : Après plusieurs minutes/heures, John The Ripper ne trouve toujours pas le mot de passe, comment faire ?***

Réponse : Si l'attaque avec le dictionnaire RockYou ne fonctionne pas, il est toujours possible de télécharger une autre wordlist et relancer une attaque. John The Ripper dispose aussi de trois autres modes d'actions, le mode simple, le mode incrémental et le mode Markov.
