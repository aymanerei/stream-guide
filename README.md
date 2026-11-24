<div align="center">

<img src="app/assets/logo_256.png" alt="Logo StreamGuide" width="128" height="128">

# StreamGuide

**Le lecteur IPTV pour Mac, Android et Android TV.**
TV en direct, films, séries, guide des programmes et enregistrement, dans une seule application.

![Version](https://img.shields.io/badge/version-0.1.0-38bdf8)
![Plateformes](https://img.shields.io/badge/plateformes-macOS%20%7C%20Android%20%7C%20Android%20TV-0f172a)
![Écrit en Rust](https://img.shields.io/badge/écrit%20en-Rust-b7410e)

</div>

---

## 📥 Télécharger

### Android TV, Fire TV, box Android — avec Downloader

Ouvrez l'application **Downloader** sur votre téléviseur ou votre box et saisissez ce code :

<div align="center">

# `5925112`

</div>

1. Installez **Downloader** (by AFTVnews) depuis la boutique d'applications de votre appareil.
2. Ouvrez Downloader et tapez le code **`5925112`** dans le champ de saisie, puis validez.
3. Une fois le téléchargement terminé, choisissez **Installer**.
4. Si l'appareil le demande, autorisez Downloader à installer des applications inconnues
   (Paramètres → Applications → Sources inconnues).

### Téléphone et tablette Android

Téléchargez `StreamGuide-0.1.0-android-arm64.apk` depuis la page
[Releases](https://github.com/aymanerei/tivimate/releases), ouvrez le fichier et acceptez l'installation.

### Mac (Apple Silicon)

Téléchargez `StreamGuide-0.1.0-macos-arm64.dmg` depuis la page
[Releases](https://github.com/aymanerei/tivimate/releases), ouvrez-le et glissez StreamGuide dans
Applications. [VLC](https://www.videolan.org/vlc/) doit être installé : StreamGuide s'en sert pour
décoder la vidéo.

---

## ✨ Fonctions

| | |
|---|---|
| 📺 **TV en direct** | Listes Xtream Codes et M3U, guide des programmes, logos des chaînes, qualité vidéo réelle affichée. |
| 🎬 **Films et séries** | Catalogue complet, reprise de lecture là où vous vous êtes arrêté, « Ma liste ». |
| 🎭 **Fiches détaillées** | Synopsis, acteurs avec photos, titres similaires, bande-annonce. |
| ⚽ **Sport** | Programmes sportifs en direct et à venir, tirés du guide. |
| ⏺️ **Enregistrement** | Enregistrement des chaînes en direct et relecture. |
| 👨‍👩‍👧 **Profils et code parental** | Profil enfant, catégories masquées, réglages verrouillés par code. |
| 🔎 **Recherche** | Chaînes, films et séries dans une seule recherche. |
| 🖥️ **Sur Mac** | Multi-écran, zapping instantané, pistes audio et sous-titres. |

---

## 🚀 Premiers pas

1. Lancez StreamGuide et ouvrez **Listes**.
2. Ajoutez votre liste : identifiants **Xtream Codes** ou adresse d'un fichier **M3U**.
3. Patientez pendant la première synchronisation (une à deux minutes pour un gros catalogue).

### Options facultatives

- **Clé TMDB** (gratuite, [themoviedb.org](https://www.themoviedb.org/)) : tendances de la semaine
  sur l'accueil, recommandations par titre, synopsis en français.
- **Clé OpenSubtitles** : recherche de sous-titres en ligne (Mac).

Les deux se saisissent dans **Paramètres**.

---

## ⚠️ Limites connues

- Le replay dépend de votre fournisseur.
- Sur Android : pas de multi-écran réel, pas de choix de pistes audio ni de sous-titres.
- Pas de version Windows, Linux ni iOS pour l'instant.

---

## 🛠️ Construire depuis les sources

Le code est dans `app/` (Rust + [egui](https://github.com/emilk/egui)).

```bash
bash scripts/build_macos_dmg.sh
```

```bash
bash scripts/build_android_apk.sh
```

Les fichiers produits arrivent dans `dist/`. La version Android demande le SDK et le NDK Android
ainsi que [`cargo-apk`](https://github.com/rust-mobile/cargo-apk).

Pour changer de logo, remplacez `app/assets/logo.jpeg` puis régénérez toutes les icônes :

```bash
python3 scripts/make_icons.py
```

---

## 🙏 Données ouvertes

- [TMDB](https://www.themoviedb.org/) — *This product uses the TMDB API but is not endorsed or certified by TMDB.*
- [TVmaze](https://www.tvmaze.com/) — distribution des séries (CC BY-SA).
- [Wikidata](https://www.wikidata.org/) et Wikimedia Commons — distribution et films liés.
- [iptv-org](https://github.com/iptv-org) — logos de chaînes manquants.

---

<div align="center">

**StreamGuide ne fournit aucun contenu.**
L'application lit uniquement les listes de votre propre fournisseur.

</div>
