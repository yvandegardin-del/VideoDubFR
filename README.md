# 🎬 VidéoDubFR — Doublage gratuit en français

**100% gratuit · Aucune clé API · Fonctionne depuis votre téléphone**

---

## 🚀 OBTENIR L'APK EN 5 ÉTAPES (depuis votre téléphone)

### Étape 1 — Créer un compte GitHub gratuit
1. Ouvrez **github.com** dans votre navigateur
2. Cliquez **Sign up** → entrez votre email → créez un mot de passe
3. Confirmez votre email

### Étape 2 — Créer le dépôt et uploader le code
1. Cliquez sur **+** en haut à droite → **New repository**
2. Nom : `VideoDubFR` → **Create repository**
3. Cliquez **uploading an existing file**
4. Glissez/déposez **tous les fichiers** du ZIP téléchargé
5. Cliquez **Commit changes**

### Étape 3 — La compilation démarre automatiquement !
1. Allez dans l'onglet **Actions** de votre dépôt
2. Vous verrez **Build APK** en cours (icône jaune ⏳)
3. Attendez ~5 minutes que ça devienne vert ✅

### Étape 4 — Télécharger l'APK
1. Cliquez sur le workflow **Build APK** vert
2. En bas de page, cliquez sur **VideoDubFR-debug**
3. Téléchargez le ZIP → extrayez **app-debug.apk**

### Étape 5 — Installer sur votre téléphone
1. Sur Android : **Paramètres** → **Sécurité** → activez **Sources inconnues**
2. Ouvrez le fichier `app-debug.apk` téléchargé
3. Appuyez **Installer** → l'app apparaît sur votre écran !

---

## ✨ Services gratuits utilisés

| Étape | Service | Coût |
|-------|---------|------|
| Transcription | Whisper (Hugging Face Spaces) | Gratuit |
| Traduction | MyMemory API + LibreTranslate | Gratuit |
| Voix française | TTS Android natif (hors-ligne) | Gratuit |
| Export vidéo | MediaMuxer Android | Gratuit |

---

## 📱 Comment utiliser l'application

1. **Choisir une vidéo** : appuyez sur la zone bleue pour sélectionner un fichier MP4/MKV/AVI, ou collez un lien URL direct
2. **Doubler** : appuyez sur **DOUBLER EN FRANÇAIS** et attendez (~2–5 min selon la longueur)
3. **Sauvegarder** : appuyez **Enregistrer dans Vidéos** → disponible dans votre galerie

---

## ⚙️ Limites à connaître

- **Transcription** : nécessite une connexion internet (serveurs Whisper Hugging Face)
- **Traduction** : MyMemory gratuit = 5 000 mots/jour ; au-delà LibreTranslate prend le relais
- **Voix** : utilise la voix TTS installée sur votre téléphone (française féminine si disponible)
- **Vidéos longues** : le découpage en morceaux est automatique mais peut prendre plusieurs minutes

---

## 🔧 Structure du projet

```
VideoDubFR/
├── .github/workflows/build.yml   ← Compilation automatique GitHub Actions
├── app/src/main/
│   ├── java/com/videodubfr/
│   │   ├── MainActivity.java      ← Interface utilisateur
│   │   ├── DubbingPipeline.java   ← Pipeline IA complet (gratuit)
│   │   └── UriHelper.java         ← Utilitaires
│   ├── res/layout/activity_main.xml
│   └── AndroidManifest.xml
└── README.md                      ← Ce fichier
```
