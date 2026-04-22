# BriefAI ⚡

> Générateur de briefs créatifs propulsé par l'IA — en une page, sans backend, déployable en 30 secondes.

![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-Claude-orange?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)

---

## 🎯 C'est quoi ?

BriefAI est une application web minimaliste qui génère un **brief créatif complet et structuré** à partir d'une simple description de projet. Tu décris ton idée, tu choisis un ton, et l'IA produit un document actionnable en quelques secondes : objectifs, cible, proposition de valeur, fonctionnalités clés, inspirations, contraintes, next steps.

Pas de compte à créer. Pas de backend. Zéro donnée stockée.

---

## ✨ Fonctionnalités

- **Double compatibilité API** — fonctionne avec OpenAI (GPT-4o mini) et Anthropic (Claude Haiku), switchable en un clic
- **Brief structuré en 10 sections** — contexte, objectifs, cible, proposition de valeur, ton & style, fonctionnalités, inspirations, contraintes, next steps, mots-clés
- **Sélecteur de tons interactif** — moderne, professionnel, premium, ludique, minimaliste, bold, accessible
- **Export presse-papier** — copie le brief complet en un clic
- **100% frontend** — aucune clé API stockée, aucun serveur, fonctionne en local
- **Responsive** — mobile & desktop

---

## 🚀 Demo

👉 **[Voir la démo live](https://bakadechi.github.io/briefAI/)**

---

## 📦 Installation

Cloner le repo et ouvrir `index.html` — c'est tout.

```bash
git clone https://github.com/bakadechi/briefai.git
cd briefai
open index.html   # ou double-clic sur le fichier
```

Aucune dépendance. Aucun `npm install`.

---

## 🔑 Configuration

BriefAI utilise directement les APIs d'OpenAI ou Anthropic depuis ton navigateur.

1. Obtiens une clé API sur [platform.openai.com](https://platform.openai.com/api-keys) ou [console.anthropic.com](https://console.anthropic.com/)
2. Colle-la dans le champ prévu dans l'interface
3. Ta clé n'est **jamais stockée** ni transmise ailleurs qu'à l'API officielle

> ⚠️ Pour la production, il est recommandé de passer par un backend (proxy) pour ne pas exposer ta clé côté client.

---

## 🛠️ Stack technique

| Élément | Choix |
|---|---|
| Frontend | HTML / CSS / JavaScript vanilla |
| IA | OpenAI GPT-4o mini · Anthropic Claude Haiku |
| Fonts | Syne (Stype) + DM Sans (Google Fonts) |
| Déploiement | GitHub Pages / Vercel / Netlify |
| Dépendances | **Aucune** |

---

## 📁 Structure du projet

```
briefai/
├── index.html        # Application complète (HTML + CSS + JS)
└── README.md
```

Tout tient dans un seul fichier — par choix de lisibilité et pour simplifier le déploiement.

---

## 🧠 Comment ça marche ?

```
Utilisateur remplit le formulaire
        ↓
Prompt structuré généré côté client
        ↓
Appel fetch() → API OpenAI ou Anthropic
        ↓
Réponse JSON parsée
        ↓
Brief affiché en sections dans l'UI
```

Le prompt demande à l'IA de répondre **uniquement en JSON** selon un schéma fixe à 10 clés. Ça garantit un rendu cohérent et parsable sans regex fragile.

---

## 🗺️ Roadmap

- [ ] Export PDF du brief généré
- [ ] Historique des briefs (localStorage)
- [ ] Mode dark / light toggle
- [ ] Support multilingue (EN, ES)
- [ ] Intégration Notion (push du brief directement dans une page)
- [ ] Backend proxy pour sécuriser les clés API

---

## 🤝 Contribuer

Les PRs sont les bienvenues. Pour les changements importants, ouvre d'abord une issue pour discuter de ce que tu voudrais modifier.

```bash
# Fork le repo
git checkout -b feature/ma-fonctionnalite
git commit -m 'feat: ajout de X'
git push origin feature/ma-fonctionnalite
# Ouvre une Pull Request
```

---

## 📄 Licence

MIT — fais-en ce que tu veux.

---

<p align="center">Fait avec ☕ et trop de prompts · <a href="https://github.com/bakadechi">@bakadechi</a></p>
