# Profil Hermès — Design (Celdel AI)

Produire des documents beaux et professionnels : flyers, guides clients, docx, powerpoint, infographies.

## Contenu

| Skill | Catégorie | Origine |
|---|---|---|
*(aucun skill personnalisé dans ce profil)*

La fiche de profil est dans `profil/SOUL.md` : c'est elle qui définit le rôle et les règles de
l'assistant. À recopier dans `<profil>/SOUL.md` sur une nouvelle installation.

## Le strict minimum

1. ce dépôt ne contient **aucun skill personnalisé** — le profil design utilise les skills *fournis avec Hermès*
2. la fiche de profil (`profil/SOUL.md`) et la liste des skills à garder ci-dessous

## Installation

```bash
./install.sh <nom_du_profil>        # ex. ./install.sh design
```

Le script copie chaque skill dans la bonne catégorie du profil (d'après `MANIFEST.tsv`).
Pour le manuel :

```bash
cp -r skills/<skill> ~/.hermes/profiles/<profil>/skills/<catégorie>/
```

Puis redémarrer Hermès ou lancer `/reload-skills`.

## Skills fournis par Hermès à garder dans ce profil

Ces skills sont livrés avec Hermès : ne pas les copier ici (ils deviendraient obsolètes à
chaque mise à jour). Il suffit de vérifier qu'ils sont présents dans le profil :

- `creative/claude-design` — concevoir une maquette, une landing, un deck en HTML
- `creative/design-md` — écrire/valider un fichier de tokens de design (DESIGN.md)
- `creative/popular-web-designs` — 54 systèmes de design réels en HTML/CSS
- `creative/baoyu-infographic` — infographies (21 mises en page × 21 styles)
- `creative/architecture-diagram` — schémas d'architecture en SVG (thème sombre)
- `creative/p5js` — croquis génératifs, shaders, interactif, 3D
- `creative/manim-video` — animations mathématiques/algorithmiques
- `creative/ascii-video` — vidéo/audio en ASCII coloré
- `creative/humanizer` — retirer les tics d'écriture « IA »
- `productivity/docx`, `productivity/powerpoint`, `productivity/pdf` — documents bureautiques

Contrôle rapide :

```bash
hermes -p design skills list --enabled-only | grep -E "claude-design|design-md|popular-web|baoyu|docx|powerpoint"
```

## Mise à jour

Les skills se modifient dans le profil (`~/.hermes/profiles/<profil>/skills/`), puis se copient
ici. Un dépôt = un profil : ne pas mélanger les domaines.
