# 🔥 Blazed

Blazed est une application de **matching intelligent** entre freelances et entreprises autour des missions et des profils. Prêt à faire flamber le marché ?

---

## 📸 Aperçu

<img src="images/250518_15h25m35s_screenshot.png" alt="Aperçu" width="300"/>

---

## 🌟 Fonctionnalités principales

* 🔐 Authentification sécurisée (JWT + refresh token)
* 📏 Formulaires multi-étapes (inscription freelance et entreprise)
* 💡 Matching automatique par domaines et intérêts
* 🎨 Interface moderne en React + Tailwind
* ⚙️ API robuste en NestJS
* 🐳 Déploiement avec Docker / Railway

---

## ⚙️ Installation locale

### 🧰 Prérequis

* Node.js ≥ 18
* Docker + Docker Compose
* Railway CLI (si besoin)

### 1. Cloner le projet

```bash
git clone https://github.com/Jupower38300/Blazed.git
cd blazed
```

### 2. Lancer le backend

```bash
cd back
cp .env.example .env
npm install
npm run start:dev
```

### 3. Lancer le frontend

```bash
cd ../front
npm install
npm run dev
```

### 💻 Ou tout lancer avec Docker

```bash
docker-compose up --build
```

---

## 📦 Déploiement

Le déploiement se fait via Railway ou tout autre serveur Docker-compatible.

### 🔧 Procédure rapide

1. **Préparer l’environnement**

   * Configurer les variables `.env` sur Railway (ou Vercel pour le front)
2. **Build & push Docker**

   ```bash
   docker-compose build
   docker-compose push
   ```
3. **Exécuter les migrations**

   * Utilisation de TypeORM :

   ```bash
   npm run migration:run
   ```
4. **Vérification**

   * Endpoint API : `/api`

---

## Tests

### ✅ Tests unitaires

```bash
# Front
cd front
npm run test
```

```bash
# Back
cd back
npm run test
```

### 🔄 Tests d’intégration (back)

* Utilisent une base de données isolée (ex : PostgreSQL via Docker)
* Ciblent les cas d’usage transverses : auth, matching, utilisateurs, etc.

### 🔍 Tests système & acceptation

* Effectués dans les environnements de préproduction
* Outils prévus : **Playwright** pour les E2E
* Réalisables manuellement ou via scripts CI/CD

---

## 🔐 Sécurité
* 🔐 Hashage de mot de passe avec **Argon2**
* 🔐 Authentification JWT + refresh token
* 🔒 Rôles utilisateurs via **AccessControl** (`guest`, `user`, `admin`)
* ✅ Validation de schéma via **Zod**
* 🛡️ Évaluation régulière des vulnérabilités

---

## 🚧 Roadmap

* [x] Authentification + rôles
* [x] Inscription multi-étapes
* [x] Matching automatique
* [ ] 🔔 Notifications en temps réel
* [ ] 🔪 E2E avec Cypress
* [ ] 📋 Tableau de bord admin
* [ ] 💳 Intégration de paiement

---

## 📄 Licence

Projet personnel – Tous droits réservés.
Utilisation uniquement avec autorisation de l’auteur.

---

## 👤 Auteur

**Julien Legrand**
[GitHub – Jupower38300](https://github.com/Jupower38300)
