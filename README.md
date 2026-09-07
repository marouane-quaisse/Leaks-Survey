# 🔍 Leaks Survey — Inspection des fuites industrielles

Application de **gestion et d'inspection des fuites de vapeur** pour le site industriel OCP. Les techniciens recensent et documentent les fuites (photos, vidéos, audio, GPS), suivent leur réparation et estiment les pertes financières et émissions de CO₂.

## 🧩 Les 3 applications

| Dossier | Technologie | Rôle |
|---------|-------------|------|
| `backend/` | Spring Boot + H2 | API REST, authentification, analyse IA |
| `frontend/` | Flutter | App mobile Android (techniciens terrain) |
| `web/` | React + TypeScript | Dashboard web (suivi & rapports) |

## ✨ Fonctionnalités

- 🔐 **Authentification** des techniciens
- 📋 **Campagnes** d'inspection (actives / clôturées)
- 💧 **Fuites** : tag, type de vapeur, pression, statut
- 📍 **Localisation GPS** + ouverture Google Maps
- 📸 **Médias** : photos, vidéos, enregistrements audio
- 🤖 **Analyse IA** des photos de fuites
- 📊 **Rapports** : pertes financières, émissions CO₂, taux de réparation

## 🚀 Démarrage

**Backend** (API sur `http://localhost:8080`)
```bash
cd backend && mvn spring-boot:run
```

**App mobile**
```bash
cd frontend && flutter pub get && flutter run
```

**Dashboard web** (sur `http://localhost:5173`)
```bash
cd web && npm install && npm run dev
```

> ⚙️ Configuration par variables d'environnement : `GEMINI_API_KEY` (analyse IA) et `JWT_SECRET` (tokens). Des valeurs de dev par défaut sont fournies.

## 🐳 Déploiement

`docker-compose.yml` à la racine + **CI/CD GitHub Actions** (`.github/workflows/deploy.yml`) sur push vers `main`.

## 🛠️ Stack

Java 17 · Spring Boot · H2 · JWT · Gemini API · Flutter · React · TypeScript · Vite · Tailwind · Nginx

## 📄 Licence

Projet interne — usage réservé.
