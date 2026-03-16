# 📝 Blog Application

Une application de blog complète développée avec Django, permettant aux utilisateurs de publier des articles, interagir via des commentaires, et bénéficier de recommandations personnalisées.

## ✨ Fonctionnalités

### 📄 Gestion des posts
- **Publication d'articles** : Interface intuitive pour créer et publier des posts
- **Pagination intelligente** : Limitation du nombre de posts par page pour une meilleure expérience utilisateur
- **Posts similaires** : Système de recommandation basé sur le contenu des articles

### 💬 Interaction utilisateur
- **Système de commentaires** : Les utilisateurs peuvent commenter les posts
- **Recommandation par email** : Partage de posts par email avec un destinataire

### 🎨 Interface
- Design responsive avec HTML/CSS personnalisé
- Templates Django optimisés

## 🛠️ Technologies utilisées

- **Backend** : Django (Python)
- **Base de données** : PostgreSQL
- **Frontend** : HTML5, CSS3
- **Email** : Système d'envoi d'emails intégré de Django

## 🚀 Installation

1. **Clone le dépôt**<br>
   git clone https://github.com/RFirmin/Blog.git<br>
   cd Blog

2. **Crée un environnement virtuel**<br>
   python -m venv venv<br>
   source venv/bin/activate  # Sur Windows : venv\Scripts\activate

3. Installe les dépendances<br>
   pip install -r requirements.txt

4. Configure la base de données PostgreSQL<br>
   Crée une base de données PostgreSQL<br>
   createdb blog_db

5. Configure les variables d'environnement<br>
Crée un fichier .env à la racine du projet :<br>
   env<br>
   DEBUG=True<br>
   SECRET_KEY=ta_clé_secrète<br>
   DATABASE_URL=postgresql://user:password@localhost/blog_db<br>
   EMAIL_HOST=smtp.gmail.com<br>
   EMAIL_PORT=587<br>
   EMAIL_HOST_USER=ton_email@gmail.com<br>
   EMAIL_HOST_PASSWORD=ton_mot_de_passe

6. Applique les migrations<br>
   python manage.py migrate

7. Crée un superutilisateur<br>
   python manage.py createsuperuser

8. Lance le serveur<br>
   python manage.py runserver

9. Accède à l'application<br>
   Site : http://localhost:8000<br>
   Admin : http://localhost:8000/admin<br>


# 📖 Utilisation
### Publier un article
Connecte-toi avec ton compte administrateur<br>
Accède à l'interface d'administration<br>
Clique sur "Posts" puis "Ajouter un post"<br>
Remplis le formulaire et publie

### Recommander un post par email
Sur la page d'un article, clique sur "Share this post"<br>
Entre l'adresse email du destinataire<br>
Un email avec le lien de l'article sera envoyé

### Commenter un post
Connecte-toi à ton compte<br>
Navigue vers un article<br>
Utilise le formulaire de commentaire en bas de la page

### Navigation avec pagination
Les posts sont automatiquement paginés (3 posts par page par défaut)<br>
Utilise les liens "Suivant" et "Précédent" pour naviguer

# 📁 Structure du projet
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

# 📫 Contact
Flins Raider - firmk21@gmail.com<br>
Lien du projet : https://github.com/RFirmin/Blog/

# 🙏 Remerciements
- Django pour son framework exceptionnel
