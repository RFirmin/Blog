# Blog Application

C'est le repository d'une application de blog développée avec Django, permettant aux utilisateurs de publier des articles, interagir via des commentaires, et bénéficier de recommandations personnalisées.<br>0
Il contient tous les fichiers necessaires pour travailler sur le projet ainsi que la procedures d'installation pour executer le projet.

## Fonctionnalités
Dans cette rubrique, les fonctionnalites implementes dans l'application sont presentees

### La gestion des posts
- **La publication d'articles** : qui se fait depuis l'interface administrateur, ou chaque post est cree et rendue disponible en ligne
- **La pagination intelligente** : le nombre de posts par page est limite a 3 pour une meilleure expérience utilisateur
- **Recommendation de posts similaires** : les posts ont un systeme de tags qui aide a la recommandation articles similaires

### Interaction utilisateur
- **Mise en place d'un système de commentaires** : Les utilisateurs peuvent interagir en commentant les posts publies
- **Recommandation de post par email** : un systeme d'envoi d'email implemente dans l'application permet de partager les posts par email avec un destinataire

### Interface des pages
- Utilisation du HTML/CSS pour implementer les differentes interfaces ainsi que pour les rendre responsives 
- les templates Django 

## Technologies utilisées
- **Backend** : pour cette partie le code a ete entierement redige en utilisant Django (Python)
- **Base de données** : au debut j'ai commence avec la base de donnees par defaut de Django (SQLite) pour ensuite exporter les donnees et les importes dans une base de donnees PostgreSQL installe depuis un conteneur Docker.
- **Frontend** : utilisation des templates Django ainsi que du HTML et du CSS
- **Email** : le système d'envoi d'emails intégré de Django est celui qui m'a aide a implemente l'envoi d'email, il fonctionne plus facilement avec l'usage des adresses emails publiques.

## Installation
1. **Cloner le dépôt**<br>
Il faut commencer par cloner le projet depuis le repository a travers la commande : git clone https://github.com/RFirmin/Blog.git<br>

2. **Création de l'environnement virtuel**<br>
Necessaire pour isoler les dependances utilisees et necessaires pour le fonctionnement du projet avec, celle permet d'eviter des conflits de version avec une version de python installe sur le disque de l'ordinateur ou d'autres dependances.<br>
   python -m venv venv<br>
   source venv/bin/activate <br>
   Sur Windows : venv\Scripts\activate

4. **Installation des dépendances**<br>
   pip install -r requirements.txt

5. **Appliquer les migrations**<br>
   python manage.py migrate

6. **Creation du super user**
   python manage.py createsuperuser

7. **Lancement du serveur**<br>
   python manage.py runserver

8. **Accès à l'application**<br>
   Site : http://localhost:8000<br>
   Admin : http://localhost:8000/admin<br>

9. **Configuration de la base de données PostgreSQL**<br>
   Installation de Docker <br>
   Installation de PostgreSQL (de preference une version postgres:16.2 minimun)<br>
   Dump des donnees sur SQLite
   changer les configurations de la base donnees au niveau du projet
   charger les donnees dans la nouvelles base de donnees

10. **Configuration des variables d'environnement**<br>
Crée un fichier .env à la racine du projet et placer les variables suivantes :<br>
   env<br>
   DEBUG=True<br>
   SECRET_KEY=ta_clé_secrète<br>
   DATABASE_URL=postgresql://user:password@localhost/blog_db<br>
   EMAIL_HOST=smtp.gmail.com<br>
   EMAIL_PORT=587<br>
   EMAIL_HOST_USER=ton_email@gmail.com<br>
   EMAIL_HOST_PASSWORD=ton_mot_de_passe
   
11. **Lancement du serveur de nouveau pour verifier que les modifications de la base de donnees ne changent pas le contenu des pages**<br>
   python manage.py runserver

12. **Accès à l'application**<br>
   Site : http://localhost:8000<br>
   Admin : http://localhost:8000/admin<br>


# Utilisation de l'application
### Publication d'un post
Connexion au compte administrateur<br>
Accès à l'interface d'administration<br>
Faire un Clic sur "Posts" puis "Ajouter un post"<br>
Remplissage du formulaire et sauvegarde
Le post est affiche sur l'interface prevu

### Recommandation d'un post par email
Se diriger sur la page qui liste l'ensemble des posts crees
Acceder aux details d'un post, cliquer sur "Share this post"<br>
Remplisser les informations du formulaire<br>
Un email avec le lien de l'article sera envoyé

### Commenter un post
Connexion à un compte<br>
Se diriger sur la page qui liste l'ensemble des posts crees
Acceder aux details d'un post<br>
Utiliser le formulaire de commentaire en bas de la page

### Navigation avec pagination
Les posts sont automatiquement paginés (3 posts par page par défaut)<br>
Utiliser les liens "Suivant" et "Précédent" pour naviguer

# Structure du projet
BlogProjet/<br>
├── blog/                 # Application principale<br>
│   ├── migrations/       # Migrations de la base de données<br>
│   ├── static/           # Fichiers statiques (CSS, JS)<br>
│   ├── templates/        # Templates HTML<br>
│   ├── templatestags/        # Templates tags HTML<br>
│   ├── forms.py        # Formulaires des commentaires<br>
│   ├── models.py        # Modèles de données<br>
│   ├── views.py         # Logique des vues<br>
│   └── urls.py          # URLs de l'application<br>
├── manage.py            <br>
└── requirements.txt     # Dépendances Python<br>

# Contact
Flins Raider - firmk21@gmail.com<br>
Lien du projet : https://github.com/RFirmin/Blog/

# Remerciements
- Django pour son framework exceptionnel
