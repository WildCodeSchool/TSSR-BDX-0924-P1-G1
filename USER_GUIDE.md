# Documentation Utilisateur : Mode d'emploi

## 1. Utilisation simple : comment effectuer une attaque pour tester la robustesse du mot de passe d'un fichier zippé chiffré sur un serveur  
### >- Localiser le fichier que l’on veut tester  
D’abord vous allez devoir ouvrir le dossier contenant votre archive zip dans un terminal.
Pour celà, ouvrez l’explorateur de fichiers présent dans la barre de gauche de votre écran.  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen1.png" width=600></P>  

Selectionnez le dossier qui contient le fameux fichier en faisant un clic droit dessus et sélectionnez “Ouvrir dans un terminal”.  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen2.png" width=600></P>   

Vous aurez alors un écran pour y saisir des commandes qui ressemble à ca :  

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_USERGUIDE/screen3.png" width=600></P>  

Ensuite, il ne vous restera plus qu'à taper les commandes suivantes :  

    zip2john archive.zip > ZipHash.txt
      
Ici nous supposons que votre fichier s'appelle archive.zip, s'il s'agit d'un autre fichier il faudra bien entendu remplacer archive.zip par votre fichier.
Le logiciel John The Ripper va alors sortir le Hash du mot de passe de ce fichier et c'est avec ce hash que nous essaierons de décrypter le mot de passe du fichier archive.  
  
Une fois cette commande exécutée, il ne vous restera plus qu'à exécuter la commande suivante :  

    john  --wordlist=/usr/share/wordlists/rockyou.txt ZipHash.txt  

Cette commande peut mettre un certain temps à s'exécuter mais devrait aboutir si le mot de passe est bien dans le dictonnaire que l'on a fourni à John.  


#### Autre méthode alternative, l'attaque en brute de force (mode incrémental)  

L'**attaque par dictionnaire** est simple et rapide mais elle présente un gros inconvénient : elle n'aboutira au mot de passe que si que si celui-ci est présent dans la liste qu'on lui a fourni.  
Pour être certain d'aboutir à un résultat et donc de découvrir le mot de passe, il existe une autre méthode qui consiste à utiliser toutes les combinaisons possibles de caractères. Cette méthode est appelée attaque en **"brute de force"**. Cette méthode est plus longue car elle essaie absolument toutes les combinaisons et pas seulement celles d'une liste.
Elle peut être cependant très longue, dans ce cas vous pourrez la stopper à l'aide des commandes `CTRL` + `C`.  

Pour lancer l'attaque en mode incrémental, entrez la commande suivante : 


     john archive.zip


## 2. FAQ : Solutions aux problèmes connus et communs liés à l'utilisation

***Question : Après plusieurs minutes/heures, John The Ripper ne trouve toujours pas le mot de passe, comment faire ?***

Réponse : Si l'attaque avec le dictionnaire RockYou ne fonctionne pas, il est toujours possible de télécharger une autre wordlist et relancer une attaque. John The Ripper dispose aussi de trois autres modes d'actions, le mode simple, le mode incrémental et le mode Markov. Vous trouverez les principes généraux de leur fonctionnement dans le README.md. Encore une fois pour terminer un processus trop long de John, tapez `CTRL` + `C`.  

***Question : Où trouver des dictionnaires (des Wordlists)?***  

Vous trouverez une large gamme de wordlists dans [Github](https://github.com). Utiliser d'autres wordlists peut être intéressant car elles sont différentes en fonction de leur utilisation.  


  
  
  




  
