<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Fa & Vodoun Connect

Application web moderne pour la connexion et l'apprentissage autour du Fa et du Vodoun.

## 🚀 Déploiement

### Sur GitHub

Le projet est déjà configuré avec le dépôt GitHub : https://github.com/BIDE27/fa-vodoun2

Pour pousser vos modifications vers GitHub :

```bash
git add .
git commit -m "Votre message de commit"
git push origin master
```

### Sur Cloudflare Pages

1. **Connecter votre dépôt GitHub à Cloudflare Pages :**
   - Allez sur [Cloudflare Dashboard](https://dash.cloudflare.com/)
   - Naviguez vers **Pages** dans le menu de gauche
   - Cliquez sur **Create a project**
   - Sélectionnez **Connect to Git**
   - Choisissez **GitHub** et autorisez l'accès
   - Sélectionnez le dépôt `BIDE27/fa-vodoun2`

2. **Configuration du build :**
   - **Framework preset :** Vite
   - **Build command :** `npm run build`
   - **Build output directory :** `dist`
   - **Root directory :** `/` (laisser vide)

3. **Variables d'environnement :**
   - Dans les paramètres du projet Cloudflare Pages, allez dans **Settings** > **Environment variables**
   - Ajoutez la variable `GEMINI_API_KEY` avec votre clé API Gemini
   - Assurez-vous qu'elle est disponible pour **Production**, **Preview** et **Branch previews**

4. **Déploiement :**
   - Cloudflare Pages va automatiquement déployer votre application à chaque push sur la branche `master`
   - Votre site sera disponible à l'adresse : `https://votre-projet.pages.dev`

## 💻 Développement Local

**Prérequis :** Node.js

1. Installer les dépendances :
   ```bash
   npm install
   ```

2. Créer un fichier `.env.local` à la racine du projet :
   ```
   GEMINI_API_KEY=votre_cle_api_gemini
   ```

3. Lancer l'application en mode développement :
   ```bash
   npm run dev
   ```

4. L'application sera accessible sur `http://localhost:3000`

## 📦 Scripts Disponibles

- `npm run dev` - Lance le serveur de développement
- `npm run build` - Construit l'application pour la production
- `npm run preview` - Prévisualise la version de production localement

## 🔧 Technologies Utilisées

- **React 19** - Bibliothèque UI
- **Vite** - Build tool et serveur de développement
- **TypeScript** - Typage statique
- **Tailwind CSS** - Framework CSS
- **Google Gemini AI** - API d'intelligence artificielle
- **Recharts** - Bibliothèque de graphiques
- **Lucide React** - Icônes

## 📝 Notes

- Le fichier `_redirects` dans le dossier `public` est nécessaire pour le routing SPA sur Cloudflare Pages
- Assurez-vous de ne jamais commiter votre fichier `.env.local` contenant votre clé API
