# ⚙️ In-Talks | Configuration de l'Organisation

Ce dépôt centralise les standards, les modèles et les configurations partagées pour l'ensemble des projets de **In-Talks**.

---

### 📂 Contenu de ce dépôt
* **`/profile`** : Contient le README public affiché sur la page d'accueil de l'organisation.
* **`/.github/ISSUE_TEMPLATE`** : Modèles standardisés pour les rapports de bugs et suggestions.
* **`/.github/PULL_REQUEST_TEMPLATE.md`** : Checklist obligatoire avant chaque déploiement.

---

### 🛠️ Standards de Développement
Pour maintenir une qualité de code constante chez **In-Talks**, nous suivons ces règles :
1. **Nommage des branches** : `feat/`, `fix/`, `docs/`, ou `refactor/` suivi du nom de la tâche (ex: `feat/auth-service`).
2. **Commits** : Nous utilisons les [Conventional Commits](https://www.conventionalcommits.org/).
3. **Revue de code** : Au moins une approbation est requise pour fusionner vers `main`.

---

### 🔑 Accès et Sécurité
* Les clés d'API (OpenAI, Vercel, etc.) ne doivent **jamais** être commitées. Utilisez les **GitHub Secrets** de l'organisation.
* Pour demander l'accès à un service tiers, contactez le CTO ou ouvrez une Issue ici-même.

---

### 🤖 Configuration MCP (Model Context Protocol)

Ce dépôt contient un fichier `mcp.json` partagé pour les assistants IA (GitHub Copilot, Claude...). Il configure trois serveurs :

| Serveur | Utilité |
|---|---|
| `github` | Gérer les Issues, PRs et GitHub Projects de l'org |
| `postgres` | Interroger la base PostgreSQL de production |
| `filesystem` | Naviguer et lire le code source |
| `docker` | Gérer les conteneurs, images et volumes Docker locaux |

**Installation (à faire une seule fois par dev) :**

1. Copier `.github/mcp.json` dans `.vscode/mcp.json` à la racine de votre workspace local.
   > VS Code ne lit que `.vscode/mcp.json` — le fichier `.github/mcp.json` est uniquement la **source partagée** versionnée. Si la config change, re-copier le fichier.
2. Ajouter les variables d'environnement :

**macOS / Linux** — dans `~/.zshrc` ou `~/.bashrc` :

```bash
# GitHub — générer sur https://github.com/settings/tokens (scopes: repo, read:org, project)
export GITHUB_TOKEN=ghp_xxxxxxxxxxxxxxxxxxxx

# PostgreSQL In-Talks (récupérer le mot de passe auprès du CTO)
export DATABASE_URL=postgresql://root:<PASSWORD>@37.60.249.81:3499/in_talks_express

# Chemin absolu vers le dossier racine des repos In-Talks sur votre machine
export INTALKS_WORKSPACE=/Users/<votre-username>/in-talks
```

Recharger le shell :
```bash
source ~/.zshrc
```

**Windows** — dans PowerShell (profil persistant) :

```powershell
# Ouvrir le profil PowerShell
notepad $PROFILE

# Ajouter ces lignes dans le fichier ouvert :
$env:GITHUB_TOKEN = "ghp_xxxxxxxxxxxxxxxxxxxx"
$env:DATABASE_URL = "postgresql://root:<PASSWORD>@37.60.249.81:3499/in_talks_express"
$env:INTALKS_WORKSPACE = "C:\Users\<votre-username>\in-talks"
```

Recharger le profil :
```powershell
. $PROFILE
```

> ⚠️ Ne jamais commiter `DATABASE_URL` ou `GITHUB_TOKEN` en clair dans un repo. Le `GITHUB_TOKEN` est **personnel** à chaque dev.

---

### 🚀 Liens Utiles
* **Tableau de bord Vercel** : [Lien vers votre console]
* **Documentation API** : [Lien vers votre doc interne ou Postman]
* **Maquette Design** : [Lien Figma/Adobe XD]