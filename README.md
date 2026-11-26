# Alif Ba – J'apprends l'arabe (5 ans)

Application Android pour apprendre les lettres arabes, les chiffres de 0 à 10 et du vocabulaire
sur 11 thèmes (animaux, mer, nature, espace, transports, famille, parc, fruits et légumes,
couleurs, maison, corps). Consignes vocales en français, mots en arabe standard.

Jeux : Écoute et touche · Je trace · Mémoire · Je compte · Autocollants à gagner (1 tous les 5 ⭐).
Espace parent : appui long (1,5 s) sur ⚙️ → prénom, affichage des chiffres, vitesse de la voix.

## Obtenir l'APK (sans rien installer, via GitHub)
1. Crée un dépôt **privé** sur github.com et envoie-y tout ce dossier (bouton « uploading an existing file » ou `git push`).
2. Onglet **Actions** → « Construire l'APK Android » se lance tout seul (≈ 5 min).
3. Ouvre l'exécution terminée → section **Artifacts** → télécharge `AlifBa-apk` (zip contenant `AlifBa.apk`).
4. Sur le téléphone : ouvre `AlifBa.apk`, autorise « Installer des applis inconnues » pour ce navigateur/gestionnaire de fichiers.

## Ou avec Android Studio
```
npm install
npx cap sync android
npx cap open android     # puis ▶ Run, ou Build > Build APK(s)
```

## Voix arabe
L'appli utilise la synthèse vocale du téléphone. Si l'arabe ne parle pas :
Paramètres › Système › Langues › Synthèse vocale › Moteur Google › Installer les données vocales › Arabe.

## Modifier le contenu
Tout le contenu (lettres, mots, thèmes) est en haut de `www/index.html` (tableaux `LETTERS`, `NUMBERS`, `THEMES`).
Ajouter un thème = ajouter un bloc `{id, fr, ar, ico, col, items:[[emoji, mot arabe, mot français], …]}`.
