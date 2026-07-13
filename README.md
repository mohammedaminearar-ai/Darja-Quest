# Darija Quest — Apprends la Darija

Application web tout-en-un (HTML/CSS/JS, sans backend) pour s'entraîner en darija marocaine : vocabulaire, conjugaison, quiz mixtes, suivi de progression avec graphiques.

## 🚀 Publier sur GitHub Pages

1. Crée un nouveau dépôt sur GitHub (ex. `darija-quest`).
2. Ajoute ce fichier `index.html` (et ce `README.md`) à la racine du dépôt, puis pousse (`git add .`, `git commit`, `git push`).
3. Va dans **Settings > Pages** du dépôt.
4. Dans **Source**, choisis la branche `main` et le dossier `/ (root)`, puis **Save**.
5. Après une minute ou deux, ton site sera en ligne à l'adresse :
   `https://<ton-nom-utilisateur>.github.io/<nom-du-depot>/`

Aucune configuration serveur n'est nécessaire : tout tourne côté navigateur.

## 🔐 Comptes utilisateurs & stockage

- Les comptes (inscription/connexion classique) et la progression sont stockés dans le `localStorage` du navigateur de chaque visiteur — donc **local à chaque appareil/navigateur**, pas de base de données partagée.
- Si tu veux que les utilisateurs retrouvent leur compte sur plusieurs appareils, il faudrait ajouter un vrai backend (hors du périmètre d'une page statique GitHub Pages).

## 🔑 Connexion avec Google (optionnel)

Le bouton "Continuer avec Google" ne fonctionnera pas tel quel : il utilise un identifiant client factice (`YOUR_GOOGLE_CLIENT_ID.apps.googleusercontent.com`). Pour l'activer :

1. Va sur [Google Cloud Console](https://console.cloud.google.com/) > APIs & Services > Identifiants.
2. Crée un **ID client OAuth 2.0** de type "Application Web".
3. Ajoute l'URL de ton site GitHub Pages (ex. `https://tonpseudo.github.io`) dans les **origines JavaScript autorisées**.
4. Copie le nouvel identifiant client dans le fichier `index.html`, ligne où est défini `GOOGLE_CLIENT_ID`.

Si tu ne configures pas cette étape, la connexion classique (email/nom d'utilisateur + mot de passe) fonctionne normalement sans rien changer.

## ⚠️ Note sécurité

Le système de mot de passe utilisé ici est un simple hash non-cryptographique (à usage local uniquement) — **ce n'est pas un système d'authentification sécurisé** pour des données sensibles. Convient pour un usage pédagogique/personnel, pas pour stocker des informations confidentielles.
