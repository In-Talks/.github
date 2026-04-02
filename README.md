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

### 🚀 Liens Utiles
* **Tableau de bord Vercel** : [Lien vers votre console]
* **Documentation API** : [Lien vers votre doc interne ou Postman]
* **Maquette Design** : [Lien Figma/Adobe XD]