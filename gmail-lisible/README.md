# Mail lisible

PWA pour iPhone qui affiche Gmail de façon plus lisible : lecture, envoi, réponse, transfert, classement par libellés, archivage, corbeille, recherche.

Toutes les actions passent par l'API Gmail : ce que tu fais ici se retrouve à l'identique dans Gmail, et inversement.

Aucun identifiant ne se trouve dans ce dépôt. Le Client ID Google se saisit dans les Réglages de l'appli et reste stocké sur l'iPhone.

## Mise en ligne (GitHub Pages)

Dépôt `masuel254/claude`, dossier `gmail-lisible`. Settings › Pages › Source : branche `main`, dossier `/ (root)`. Adresse : `https://masuel254.github.io/claude/gmail-lisible/`

## Configuration Google (une seule fois)

1. Aller sur https://console.cloud.google.com, créer un projet « Mail lisible ».
2. API et services › Bibliothèque › activer **Gmail API**.
3. Écran de consentement OAuth › type **Externe** › ajouter son adresse Gmail dans **Utilisateurs test**.
4. Identifiants › Créer des identifiants › **ID client OAuth** › type **Application Web**.
   - Origine JavaScript autorisée : `https://masuel254.github.io`
   - URI de redirection autorisé : `https://masuel254.github.io/claude/gmail-lisible/`
5. Copier l'ID client (`…apps.googleusercontent.com`) et le coller dans l'appli, Réglages › Identifiant Google.

## Installation sur l'iPhone

Ouvrir l'adresse dans Safari › Partager › **Sur l'écran d'accueil**.

## Limites V1

- La connexion Google dure 1 heure, puis l'appli te renvoie vers l'écran Google : un simple appui suffit.
- Les mails sont envoyés en texte simple, sans mise en forme.
- Boîte Free : V2, avec un relais IMAP sur le VPS.
