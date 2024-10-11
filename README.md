# Documentation Générale

## 1. Présentation du contexte

Se créer un mot de passe sécurisé, c’est notre première ligne de défense. Les mots faibles et répétitifs sont l’une des principales failles exploitées par les cyber criminels pour accéder à nos données en ligne ou sur nos machines.  
Et si l’on regardait d’où l’on vient, pour analyser votre problématique passée et mieux comprendre l’actuelle. Vos données sur vos machines n’étaient pas forcément archivées et prenaient beaucoup de place sur vos disques durs. Vous avez donc mis en place des fichiers zip afin de les compresser et qu’elles deviennent moins invasives sur vos disques.  
L’époque actuelle laisse la part belle aux cyberattaques en tous genres et la priorité devient de sécuriser les données de votre entreprise stockées dans ces dossiers zip. L’opportunité de mettre en place un mot de passe sur ces dossiers permet une meilleure sécurisation des données, mais la robustesse de ce mot de passe est primordiale pour éviter toute fuite.

## 2. Présentation des objectifs

- *Objectif principal* : Effectuer une attaque par dictionnaire pour tester la robustesse du mot de passe d’un fichier zip chiffré sur un serveur.
- *Objectif secondaire* : Effectuer une attaque sur un compte local du serveur.

**Client** : Ubuntu 22.04/24.04 LTS  
**Serveur** : Windows Server 2022

## 3. Présentation de l’équipe et rôles

Le projet a suivi un processus de création selon la méthode **AGILE**. Cette méthode permet de rester flexible et de s’adapter aux changements. L’environnement de travail **SCRUM** a été utilisé pour cadrer et structurer le travail en équipe.  

Notre organisation se basait sur une planification de sprint d’une semaine, durant laquelle un membre de l’équipe occupait l’un des deux rôles principaux : 

- **Scrum Master** : Il facilite le processus SCRUM en aidant à identifier et éliminer les obstacles, afin de maintenir la productivité de l’équipe. Il anime tous les matins les *daily*, qui permettent à chacun de s’exprimer librement sur des problématiques, l’avancée de leur travail, ou tout autre sujet pertinent dans le cadre du projet. Il anime aussi une rétrospective à la fin de la semaine pour faire un bilan du sprint.
- **Product Owner** : Il se concentre sur la gestion du contenu produit. Il priorise les besoins du client et décide des nouvelles fonctionnalités à développer par sprint. C’est lui qui remplit le *Trello* par sprint et affecte les différents tickets.

### Membres de l’équipe :

- *Julien Normand* : Semaine 1 Scrum Master / Semaine 2 Product Owner
- *Frédérique Druet* : Semaine 1 Product Owner / Semaine 2 Scrum Master


## Choix techniques : présentation des outils et logiciels, systèmes d'exploitation, versions

- ### **John The Ripper**              
JTR ou John est un logiciel libre de cassage de mot de passe, utilisé notamment pour tester la sécurité d’un mot de passe. C’est l’un des logiciel de cassage de mot de passe les plus populaires car il inclut l’autodétection des fonctions de hachage utilisées pour stocker des mots de passe, l’implémentation d’un grand nombre d’algorithmes de cassage.            
John dispose de plusieurs modes d'actions, le mode simple, l'attaque par dictionnaire, le mode incrémental.               
**Mode simple** : John effectue quelques transformations sur le nom d'utilisateur, pour casser les mots de passe les plus faibles. Pour l'utilisateur toto, il essayerait "ToTo, toto123, ToTo123, etc.". Ce mode est le plus rapide à effectuer, un mot de passe qui serait cassé par cette méthode serait un mauvais mot de passe.          
**Attaque par dictionnaire** : John essaye un à un tous les mots d'une liste de mots de passe potentiels, en leur appliquant les mêmes transformations que dans le mode précédent.           
Exemple du dictionnaire **Rock You** :               
RockYou est une wordlist (*un dictionnaire*) qui contient des millions de mots de passe réels qui ont été exposés lors de diverses violations de données. Elle est utilisée pour les tests de pénétration et le cracking de mots de passe.          
**Mode incrémental** (*attaque par brute de force*) : John va essayer toutes les combinaisons de caractères possibles, jusqu'à trouver le mot de passe. Tous les caractères étant testés, ce mode est techniquement infaillible, bien que la robustesse du mot de passe influe grandement sur le temps de calcul nécessaire à le trouver.              
Afin d'augmenter la pertinence de l'algorithme, John implémente la recherche des caractères par fréquence d'utilisation, pour rechercher d'abord les caractères les plus utilisés statistiquement.

- ### **Systèmes d’exploitations et leur version**

**Windows Server 2022** est le système d'exploitation de Microsoft pour serveurs, sorti en août 2021.
Il propose une sécurité multicouche, des fonctionnalités hybrides et une plateforme flexible. Le serveur utilise Windows Defender System Guard et la sécurité basée sur la virtualisation pour réduire les risques.
La version inclut une gestion des machines virtuelles améliorée, et des fonctionnalités avancées dans Windows Admin Center. Les conteneurs Windows ont des tailles d’images réduites pour un téléchargement plus rapide.
**Ubuntu 24.4 LTS** est un système d’exploitation sous Linux fondée sur Debian avec une interface simple, intuitive, et sécurisée.
Certaines des versions sont qualifiées de LTS (*long terme support*), ce qui signifie qu'elles sont plus particulièrement optimisées, stables, et seront maintenues durant cinq ans.



## Difficultés rencontrées / Solutions trouvées 

## Axes d'améliorations

## Conclusion
