# Documentation Administrateur

## 1. Pré-requis techniques

## 2. Etapes d'installation et de configuration 

### Installation des postes serveur et client

### Lier serveur et client 

### Installation du logiciel John The Ripper

**Etape 1. Vérifiez que John The Ripper n’est pas déjà installé.**  
   Ouvrez votre terminal et tapez la commande :

   *john --version*

   Le terminal vous renvoie la commande a exécuter pour l’installer s’il n’est pas déjà présent sur votre système.

**Etape 2. Mettre à jour le système**
   Avant d'installer quoi que ce soit, il est toujours conseillé de mettre à jour votre système pour s'assurer que vous avez les derniers paquets disponibles. Tapez la commande : 
   
  *sudo apt update*
  *sudo apt upgrade*
  
Veuillez entrer « O » à la demande de confirmation.

**Etape 3. Installation de John The Ripper**
Tapez la commande dans votre terminal : 

*sudo snap install john-the-ripper*

**Etape 4. Vérification de la bonne installation**
Tapez la commande dans votre terminal :

*john –version*

Votre terminal vous confirme bien la version qui vient d’être installée.

## 3. FAQ : solutions aux problèmes connus et communs liés à l'installation et à la configuration
