# Projet 6 Application d'avis gastronomiques - Eugène Carmona 
## Formation Openclassroom Developpeur 

Ceci est le backend du projet 6 pour la formation Developpeur. Pour faire fonctionner l'application totale vous devez avoir :
  - le frontend que vous trouverez ici https://github.com/OpenClassrooms-Student-Center/dwj-projet6
  - télécharger la partie backend et veiller à installer nodemon
  - depuis le dossier frontend, déclencher la commande 'ng serve' et depuis le dossier backend, la commande 'nodemon'


## Implantation de la sécurité en fonction des règles OWASP

  - A1 : injection problème 
    - sécurité des requètes avec HELMET 
    - sécurité des communications avec HELMET, maskdata, bcrypt et le middleware d'autentification 

  - A2 : Broken identification 
    - sécurisé avec le middleware d'authentification si le webtoken a plus de 24h il est détruit.
  
  - A3 : Sensitive data exposure 
    - sécurisé avec bcrypt et maskdata, les deux packages cryptent les datas envoyés au serveur
  
  - A4 : XML external entities 
    - réglé par la partie front

  - A5 : Broken access control 
    - Sécurisé un utilisateur peut mofifier uniquement ses propres données et non celles des autres
  
  - A6 : security misconfiguration 
    - problème non traité ici

  - A7 : Cross site scripting 
    - sécurisé par HELMET et le middleware d'authentification
  
  - A8 : insecure deserialization  
    - sécurisé par HELMET et le middleware d'authentification

