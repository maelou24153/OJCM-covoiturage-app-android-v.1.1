# OJCM Covoiturage – application Android

Petite application qui ouvre uniquement le site
https://ojcm-covoiturage-v-2.onrender.com/ avec le logo de l'OJCM et le titre « Covoiturage ».

- Toute navigation vers un autre site est bloquée.
- Tirer vers le bas pour actualiser, bouton retour pour revenir en arrière.
- Écran d'erreur avec bouton « Réessayer » (utile quand le site Render se réveille).

## Générer l'APK

1. Installer Android Studio (gratuit) : https://developer.android.com/studio
2. `File > Open` et choisir ce dossier, puis attendre la fin de la synchronisation Gradle.
3. Pour tester : brancher le téléphone (mode développeur + débogage USB) et cliquer sur ▶.
4. Pour obtenir un APK à installer : `Build > Build Bundle(s) / APK(s) > Build APK(s)`.
   Le fichier se trouve dans `app/build/outputs/apk/debug/app-debug.apk`.
   Pour une version signée à publier : `Build > Generate Signed Bundle / APK`.

## Personnaliser

- Adresse du site : `HOME_URL` et `ALLOWED_HOST` dans `app/src/main/java/fr/ojcm/covoiturage/MainActivity.kt`
- Logo du bandeau : `app/src/main/res/drawable-nodpi/logo.png`
- Icône de l'app : dossiers `app/src/main/res/mipmap-*`
- Couleurs : `res/values/themes.xml` et `res/layout/activity_main.xml`

`icone-play-store-512.png` est l'icône 512×512 si tu publies un jour sur le Play Store.

## Compiler avec GitHub (sans Android Studio)

1. Créer un dépôt GitHub et y envoyer tout le contenu de ce dossier (y compris le dossier `.github`).
2. Onglet **Actions** > « Compiler l'APK » > **Run workflow** (se lance aussi tout seul à chaque envoi).
3. Quand c'est vert (2 à 4 min), ouvrir l'exécution et télécharger **OJCM-Covoiturage-apk** en bas de page.
4. Décompresser, puis installer `app-debug.apk` sur le téléphone (autoriser les sources inconnues).
