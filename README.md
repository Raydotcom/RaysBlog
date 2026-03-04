# Ray's Blog

Blog d'analyses indépendantes en français, anglais et arabe.

---

## 🚀 Déployer sur GitHub Pages (5 minutes)

### Étape 1 — Créer le repository
1. Va sur [github.com](https://github.com) et connecte-toi
2. Clique sur le **+** en haut à droite → **New repository**
3. Nom : `raysblog` (ou ce que tu veux)
4. Coche **Public**
5. Clique **Create repository**

### Étape 2 — Mettre les fichiers en ligne
1. Sur la page du repository, clique **uploading an existing file**
2. Fais glisser TOUS les fichiers et dossiers de ce projet :
   - `index.html`
   - `articles/` (tout le dossier avec les JSON)
   - `README.md`
3. Clique **Commit changes**

### Étape 3 — Activer GitHub Pages
1. Va dans **Settings** (onglet en haut du repository)
2. Dans le menu à gauche, clique **Pages**
3. Sous "Source", choisis **Deploy from a branch**
4. Sous "Branch", choisis **main** et **/ (root)**
5. Clique **Save**
6. Attends 1-2 minutes, ton site sera en ligne à :
   `https://TON-PSEUDO.github.io/raysblog/`

---

## 📝 Publier un nouvel article

### Méthode simple (via GitHub.com)

1. Va dans ton repository → dossier `articles/`
2. Clique **Add file** → **Create new file**
3. Nomme le fichier : `006.json` (le numéro suivant)
4. Colle ce template :

```json
{
  "id": 6,
  "lang": "FR",
  "category": "geopolitics",
  "title": "Le titre de ton article",
  "excerpt": "Un résumé en une phrase.",
  "date": "4 mars 2026",
  "readTime": 10,
  "featured": false,
  "body": "Premier paragraphe de ton article.\n\nDeuxième paragraphe.\n\nTroisième paragraphe."
}
```

5. Clique **Commit new file**
6. Ensuite, ouvre `articles/index.json` et ajoute `"006.json"` à la liste
7. C'est en ligne !

### Champs de l'article

| Champ      | Description                                                |
|------------|------------------------------------------------------------|
| `id`       | Numéro unique (incrémente à chaque article)                |
| `lang`     | `"FR"`, `"EN"`, ou `"AR"`                                 |
| `category` | `"geopolitics"`, `"economy"`, `"politics"`, `"society"`, ou `"psychology"` |
| `title`    | Le titre de l'article                                      |
| `excerpt`  | Résumé court (1-2 phrases) affiché sur la page d'accueil   |
| `date`     | Date affichée (format libre)                               |
| `readTime` | Temps de lecture estimé en minutes                         |
| `featured` | `true` pour l'article à la une, `false` sinon             |
| `body`     | Le texte complet. Utilise `\n\n` pour séparer les paragraphes |

### Important
- Un seul article peut avoir `"featured": true` à la fois
- Pour les articles en arabe, utilise `"lang": "AR"` et le site gère automatiquement le sens de lecture droite-à-gauche
- Les sauts de paragraphe se font avec `\n\n` dans le body

---

## 🔗 Partager sur les réseaux sociaux

Chaque article a une URL permanente :
```
https://TON-PSEUDO.github.io/raysblog/#article-1
```

Le site inclut des boutons de partage pour Twitter/X, LinkedIn, Facebook et WhatsApp directement sur chaque article.

---

## 🎨 Personnaliser

- **Couleurs** : modifie les variables CSS dans `:root { }` en haut de `index.html`
- **Textes "À propos"** : modifie les traductions dans l'objet `i18n` dans le JavaScript
- **Catégories** : ajoute des catégories dans `categoryLabels` et `catKeys`

---

## 📁 Structure du projet

```
raysblog/
├── index.html              ← Le site complet (HTML + CSS + JS)
├── README.md               ← Ce fichier
└── articles/
    ├── index.json           ← Liste des fichiers d'articles
    ├── 001.json             ← Article 1
    ├── 002.json             ← Article 2
    ├── 003.json             ← Article 3
    ├── 004.json             ← Article 4
    └── 005.json             ← Article 5
```
