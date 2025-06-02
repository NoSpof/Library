# Library

🚀 Fonctionnalités

- Authentification :

        Support Keycloak et Google OAuth
        Gestion des sessions sécurisée avec NextAuth.js
        Protection des routes API

- Intégration Google Drive :

        Parcours des dossiers Drive par ID
        Listage automatique des fichiers PDF
        Affichage des métadonnées (nom, auteur, date, taille)

- Visionneuse PDF :

        Lecteur PDF intégré avec react-pdf
        Navigation page par page
        Interface responsive et moderne
        Ouverture en mode plein écran

📦 Installation

Clonez et installez les dépendances :

```bash 
npm install
```

Configurez l'environnement (.env.local) :

```env
# Configuration NextAuth
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=votre-secret-nextauth

# Configuration Keycloak
KEYCLOAK_ISSUER=https://votre-keycloak.com/realms/votre-realm
KEYCLOAK_CLIENT_ID=votre-client-id
KEYCLOAK_CLIENT_SECRET=votre-client-secret

# Configuration Google
GOOGLE_CLIENT_ID=votre-google-client-id.googleusercontent.com
GOOGLE_CLIENT_SECRET=votre-google-client-secret

# Dossier par défaut (optionnel)
NEXT_PUBLIC_DEFAULT_FOLDER_ID=id-du-dossier-drive

```

Lancez l'application :

```bash 
npm run dev
```
🔧 Configuration requise

- Keycloak :

    Créez un client dans votre realm
    
    Configurez les URLs de redirection : http://localhost:3000/api/auth/callback/keycloak

- Google Cloud Console :

        Activez l'API Google Drive
        
        Configurez les URLs autorisées : http://localhost:3000/api/auth/callback/google

        Ajoutez les scopes : openid email profile https://www.googleapis.com/auth/drive.readonly

💡 Utilisation

- Connexion : Choisissez entre Keycloak ou Google
- Sélection du dossier : Entrez l'ID du dossier Google Drive contenant vos PDFs
- Navigation : Parcourez la liste des ebooks avec leurs métadonnées
- Lecture : Cliquez sur "Lisez-moi" pour ouvrir la visionneuse PDF

🎨 Interface

L'application utilise Tailwind CSS pour une interface moderne et responsive avec :

- Design épuré et professionnel
- Navigation intuitive
- Visionneuse PDF plein écran
- Indicateurs de chargement
- Gestion d'erreurs élégante