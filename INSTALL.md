# Documentation Administrateur

## 1. Pré-requis techniques
Deux machines:
- Client : Une machine avec un système d'exploitation Ubuntu 22.04/24.04
- Serveur : Une machine avec un système d'exploitation Windows Server 2022 

## 2. Etapes d'installation et de configuration 

### Installation des postes serveur et client
Configuration poste client Ubuntu :
1) Changer le nom de votre hôte
   
       hostnamectl set-hostname CLININ01

2) Créer un nouvel utilisateur
       sudo su             
   Rentrer mot de passe de l'utilisateur actuel, puis :              
       adduser wilder               
   Rentrer le nouveau mot de passe du nouvel utilisateur puis le confirmer et appuyer sur entrée.             
   Vous pourrez ajouter plusieurs détails sur l'utilisateur, sinon appuyez sur entrée plusieurs fois, et confirmez en tapant "O".
   Fermer le terminal et fermer la session d'ubuntu.
   *capture d'écran*
   Se reconnecter avec le nouvel utilisateur wilder et son ùmot de passe.
   Ouvrir votre terminal.
       sudo su
   Entrer le mot de passe de wilder.
   Supprimer l'ancien utilisateur
       deluser ancien_utilisateur
   
     
 
4)  

Configuration poste serveur Windows :

1) Changer nom du serveur :
Aller dans Settings ---> puis About  ---> cliquez sur Rename this PC
   *Capture d'écran*

2) Changer nom de l'hôte
Aller dans Panneau de configuration : Control panel ---> System and Security ---> Administrative Tools ---> Computer Management            
*Capture d'écran*
Dérouler l'onglet Local Users and Groups puis cliquez sur Users.                                   
Clic droit sur le compte que vous souhaitez renommer puis cliquez sur Rename.                                  
*Capture d'écran*

3) Changer le mot de passe utilisateur

   

### Lier serveur et client 

### Installation du logiciel John The Ripper

**Etape 1. Vérifiez que John The Ripper n’est pas déjà installé.**  
   Ouvrez votre terminal :

       john --version

   Le terminal vous renvoie la commande a exécuter pour l’installer s’il n’est pas déjà présent sur votre système.

**Etape 2. Mettre à jour le système**
   Avant d'installer quoi que ce soit, il est toujours conseillé de mettre à jour votre système pour s'assurer que vous avez les derniers paquets disponibles. Tapez la commande : 
   
      sudo apt update
      sudo apt upgrade
  
Veuillez entrer « O » à la demande de confirmation.

**Etape 3. Installation de John The Ripper**
Tapez la commande dans votre terminal : 

    sudo snap install john-the-ripper

**Etape 4. Vérification de la bonne installation**
Tapez la commande dans votre terminal :

    john –version

Votre terminal vous confirme bien la version qui vient d’être installée.

## 3. FAQ : solutions aux problèmes connus et communs liés à l'installation et à la configuration
