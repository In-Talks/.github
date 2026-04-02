# 🤝 Contribuer à In-Talks

Merci de vouloir contribuer à l'intelligence sociale en temps réel ! Ce document contient les directives pour maintenir une base de code saine et cohérente.

---

### 🚀 Guide de démarrage rapide

1. **Cloner le dépôt** : `git clone https://github.com/In-Talks/nom-du-repo.git`
2. **Installer les dépendances** : `npm install` (ou `pnpm install`)
3. **Configurer les variables d'environnement** : 
   - Copiez `.env.example` vers `.env`
   - Ajoutez vos clés API (OpenAI, Vercel, etc.)
4. **Lancer en local** : `npm run dev`

---

### 🌿 Gestion des Branches

Nous utilisons une stratégie de **Trunk-Based Development** simplifiée :
- **`main`** : Branche de production, toujours stable.
- **Features/Fixes** : Créez une branche depuis `main` avec un nom descriptif :
  - `feat/nom-feature` (ex: `feat/sentiment-analysis`)
  - `fix/nom-bug` (ex: `fix/mobile-navbar`)
  - `docs/nom-update`

---

### 📝 Standards de Code

#### 1. Commits (Conventional Commits)
Nous suivons le format `type(scope): description`.
- `feat:` : Nouvelle fonctionnalité.
- `fix:` : Correction de bug.
- `refactor:` : Modification du code sans changement de logique.
- `style:` : Mise en forme, points-virgules manquants, etc.

#### 2. Qualité du code
- **Linting** : Exécutez `npm run lint` avant de commit.
- **Tests** : Assurez-vous que tous les tests passent avec `npm test`.

---

### 📥 Processus de Pull Request (PR)

1. Poussez votre branche sur GitHub.
2. Ouvrez une **Pull Request** vers la branche `main`.
3. Remplissez le template de PR (il s'affichera automatiquement).
4. Attendez la revue d'un **Code Owner** (@In-Talks/admins).
5. Une fois approuvée et les tests validés, la PR sera mergée.

---

### 🛡️ Sécurité
Si vous découvrez une vulnérabilité de sécurité, merci de **ne pas ouvrir d'issue publique**. Envoyez un email directement à [security@in-talks.ma](mailto:security@in-talks.ma).

---

*Merci de construire le futur de la Social Intelligence avec nous !* 🎙️