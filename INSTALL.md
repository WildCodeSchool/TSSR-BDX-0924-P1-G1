# Documentation Administrateur

## 1. Pré-requis techniques
Deux machines:
- Client : Une machine avec un système d'exploitation Ubuntu 22.04/24.04
- Serveur : Une machine avec un système d'exploitation Windows Server 2022 

## 2. Etapes d'installation et de configuration 

### Installation des postes serveur et client

**Résumé :**                 

*Client Ubuntu*                   
- Nom : CLIWIN01
- Compte utilisateur : wilder
- Mot de passe : Azerty1*
- Adresse IP fixe : 172.16.10.20/24
                                  
*Serveur Windows*                                      
- Nom : SERVWIN01
- Compte utilisateur : Administrator
- Mot de passe : Azerty1*
- Adresse IP fixe : 172.16.10.10/24

**Configuration poste client Ubuntu :**
1) Changer le nom de votre hôte
   
         hostnamectl set-hostname CLININ01

2) Créer un nouvel utilisateur
   
         sudo su             
   Rentrer mot de passe de l'utilisateur actuel, puis :
                                        
         adduser wilder               
   Rentrer le nouveau mot de passe du nouvel utilisateur puis le confirmer et appuyer sur entrée.                                     
   Vous pourrez ajouter plusieurs détails sur l'utilisateur, sinon appuyez sur entrée plusieurs fois, et confirmez en tapant "O".              
   Fermer le terminal et fermer la session d'ubuntu.  
                    
   <P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Install_adduser.png" width=600></P>  
   Se reconnecter avec le nouvel utilisateur wilder et son mot de passe.  
   Ouvrir votre terminal.  
   
                                                                      
            sudo su                                    
   Entrer le mot de passe de wilder.                                   
   Supprimer l'ancien utilisateur  
                                                                       
            deluser ancien_utilisateur  

4) Changer le mot de passe utilisateur  
      

**Configuration poste serveur Windows :**  

1) Changer nom du serveur :                                
Aller dans Settings ---> puis About  ---> cliquez sur Rename this PC                                     
  
   <P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-16%20151234.png" width=600></P>      <P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-16%20151434.png" width=600></P>

2) Changer nom de l'hôte
Aller dans Panneau de configuration : Control panel ---> System and Security ---> Administrative Tools ---> Computer Management
          
  <P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-16%20155218.png" width=600></P>              
  
Dérouler l'onglet Local Users and Groups puis cliquez sur Users.                                   
Clic droit sur le compte que vous souhaitez renommer puis cliquez sur **Rename**.                

  <P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-17%20082657.png" width=600></P>

3) Changer le mot de passe utilisateur                                           
Aller dans Panneau de configuration : Control panel ---> System and Security ---> Administrative Tools ---> Computer Management
Dérouler l'onglet Local Users and Groups puis cliquez sur Users.                                    
Clic droit sur le compte concerné par le changement de mot de passe et cliquez sur **Set Password...**

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-16%20161200.png" width=600></P>

Rentrer votre nouveau mot de passe puis cliquez sur OK.                              

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-16%20161409.png" width=600></P>


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

    sudo apt-get install john-the-ripper  

Création d'un alias pour la commande zip2john :   

    sudo snap alias john-the-ripper.zip2john zip2john

**Etape 4. Vérification de la bonne installation**
Tapez la commande dans votre terminal :

    john –version

Votre terminal vous confirme bien la version qui vient d’être installée.

**Etape 5. Installation des librairies de John The Ripper**

    sudo apt install ocl-icd-opencl-dev -y

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/Capture%20d'%C3%A9cran%202024-10-17%20081754.png" width=600></P>

**Etape 6. Télechargement de la wordList Rockyou**

Cliquez sur ce lien pour téléchargement : [RockYou](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt)

Puis ajoutez le fichier téléchargé à votre Dossier personnel.

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/bibli2.jpg" width=600></P>

<P ALIGN="center"><IMG src="https://github.com/WildCodeSchool/TSSR-BDX-0924-P1-G1/blob/main/IMG_INSTALL/bibli3.jpg" width=600></P>

## 3. FAQ : solutions aux problèmes connus et communs liés à l'installation et à la configuration

***Question : Mes deux machines ne communiquent pas. Que dois-je faire ?***

Réponse : Pour résoudre ce problème, suivez ces étapes :

- Vérifiez si elles sont sur la même plage d'IP : Assurez-vous que les deux machines sont configurées avec des adresses IP dans la même plage. Vous pouvez le vérifier en exécutant ipconfig sous Windows ou ip a sous Ubuntu pour connaître leur adresse IP actuelle.                                  

- Effectuez un test ping : Utilisez la commande ping suivi de l'adresse IP de l'autre machine pour vérifier s'il y a une réponse. Cela indique si les deux machines peuvent communiquer entre elles.

***Question : Pourquoi l'utilisateur que j'ai créé sur la machine Ubuntu ne peut-il pas utiliser les commandes sudo ?***

Réponse : 
Si l'utilisateur que vous avez créé sur Ubuntu ne peut pas exécuter de commandes avec sudo, voici quelques étapes pour résoudre ce problème :

Vérifiez si l'utilisateur appartient au groupe sudo :                                            
Pour qu'un utilisateur puisse utiliser les privilèges administratifs, il doit appartenir au groupe sudo. Vérifiez avec la commande suivante dans votre terminal :                

    groups wilder             

Si le groupe sudo n'apparaît pas, cela signifie que l'utilisateur n'a pas les droits nécessaires.                      

Ajoutez l'utilisateur au groupe sudo :                                       
Si l'utilisateur n'est pas dans le groupe, vous pouvez l'ajouter en utilisant la commande suivante en tant qu'utilisateur root ou un autre administrateur :                  

    sudo usermod -aG sudo wilder                                             

Déconnectez-vous et reconnectez-vous :                                         
Après avoir ajouté l'utilisateur au groupe sudo, déconnectez-vous de la session et reconnectez-vous pour que les modifications prennent effet.                            

Vérifiez les permissions sudo :                                    
Vous pouvez tester en exécutant une commande avec sudo :                                                                        

    sudo apt update                                 

Si l'utilisateur est maintenant dans le groupe sudo, il pourra exécuter cette commande avec succès.
