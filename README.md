# Ma Santé – Pied Cheville (Ortho Charcot Lyon)

Une PWA (Progressive Web App) développée avec Astro + Tailwind pour améliorer le parcours de soins orthopédiques des patients.

## 🚀 Fonctionnalités

### ✅ Pages principales
- **Accueil** : Vue d'ensemble avec accès rapide aux fonctionnalités
- **Mes Douleurs** : Grille des zones anatomiques avec fiches détaillées (MDX)
- **Prendre RDV** : Intégration Doctolib et informations pratiques
- **Préparer Consultation** : Formulaire mémo avec localStorage
- **Après Consultation** : Checklist post-consultation avec localStorage
- **Chirurgie** : Timeline complète du parcours chirurgical
- **Correspondants** : Page pour les professionnels de santé

### 🔒 Confidentialité V1/V2
- **Aucune collecte de données** côté serveur
- Tous les formulaires utilisent le **localStorage** du navigateur
- Impression/PDF via `window.print()` (pas d'upload)
- Bandeau de confidentialité sur chaque page

### 📱 PWA Features
- **Installable** sur l'écran d'accueil
- **Mode hors-ligne** avec service worker
- **Thème** : #0ea5e9 (bleu)
- **Icônes** : 192x192 et 512x512

## 🛠️ Stack Technique

- **Framework** : Astro 4.0
- **Styling** : Tailwind CSS
- **PWA** : @vite-pwa/astro
- **Build** : Vite
- **Langage** : TypeScript/JavaScript

## 📦 Installation

```bash
# Installer les dépendances
npm install

# Démarrer le serveur de développement
npm run dev

# Build pour la production
npm run build

# Preview du build
npm run preview
```

## 🎨 Design System

### Couleurs
- **Primary** : #0ea5e9 (bleu)
- **Background** : #f8fafc (gris très clair)
- **Cards** : Blanc avec ombres douces
- **Text** : Gris foncé (#1f2937)

### Typographie
- **Font** : Inter (Google Fonts)
- **Tailles** : >= 16px (accessibilité)
- **Contrastes** : Respect des standards WCAG

### Composants
- **Navigation** : Onglets en capsule arrondie
- **Cards** : Bordures arrondies + ombres légères
- **Boutons** : États hover et focus visibles
- **Formulaires** : Validation et feedback visuel

## 📋 Fonctionnalités localStorage

### Mémo Consultation
- Sauvegarde automatique des réponses
- Aperçu en temps réel
- Impression/PDF personnalisé
- Effacement avec confirmation

### Checklist Post-Consultation
- Cases à cocher persistantes
- Impression des éléments cochés
- Sauvegarde automatique

## 🏥 Contenu Médical

### Fiches Pathologies (MDX)
- Structure standardisée : "C'est quoi ?", "Pourquoi ça fait mal ?", "Quand consulter ?", "Si chirurgie"
- Exemple : Hallux valgus (oignon)
- Liens vers Doctolib

### Timeline Chirurgie
- **Pré-op** : Jeûne, douche, anesthésie, organisation
- **Jour J** : Déroulement de l'intervention
- **Post-op** : J0-J7, J7-J30, J30+ avec phases détaillées

### Matériel Post-Op
- Chaussure post-opératoire
- Attelle cheville
- Botte avec/sans appui
- Fiches détaillées pour chaque matériel

## 🔧 Configuration

### astro.config.mjs
```javascript
export default defineConfig({
  integrations: [
    tailwind(),
    VitePWA({
      registerType: 'autoUpdate',
      display: 'standalone',
      theme_color: '#0ea5e9'
    })
  ]
});
```

### tailwind.config.mjs
- Couleurs personnalisées (primary palette)
- Ombres douces (soft, soft-lg)
- Police Inter
- Responsive design

## 📱 PWA Manifest

```json
{
  "name": "Ma Santé – Pied Cheville",
  "short_name": "Ma Santé Pied",
  "theme_color": "#0ea5e9",
  "background_color": "#f8fafc",
  "display": "standalone",
  "start_url": "/"
}
```

## 🚀 Déploiement

L'application est prête pour le déploiement sur :
- Vercel
- Netlify
- GitHub Pages
- Tout hébergeur statique

## 📄 Licence

Application développée pour Ortho Charcot Lyon - Usage médical uniquement.

## 🔒 Conformité RGPD

- **V1/V2** : Aucune collecte de données personnelles
- Toutes les données restent sur l'appareil de l'utilisateur
- Aucun tracking ou analytics
- Bandeau de confidentialité visible

---

**Développé avec ❤️ pour améliorer le parcours de soins orthopédiques**