# Bondaita — Imagine. Create. Play. 🎮

**Bondaita** is an online gaming platform — a next-generation alternative to Roblox — built entirely as a single-page application in one `index.html` file, powered by Firebase.

## 🚀 Features

- **Single HTML File SPA** — Zero build steps, deploy anywhere
- **Hash-Based Routing** — Full client-side navigation with 20+ routes
- **Firebase Backend** — Authentication, Firestore database, real-time updates
- **Dual Currency System** — Bonds (premium) & Studs (free earnable)
- **Game Discovery** — Browse, search, filter games by genre
- **Avatar Customization** — 2D paper-doll avatar editor
- **Catalog Marketplace** — Buy/sell items with Bonds
- **Social Features** — Friends, messaging, groups, profiles
- **Creator Hub** — Create games, manage game passes, view analytics
- **Dark/Light Theme** — System-aware with manual toggle
- **Mobile Responsive** — Full mobile sidebar and adaptive layouts
- **Custom SVG Icons** — 80+ hand-crafted inline SVG icons, no icon libraries

## 💰 Currency System

### Studs (Free Currency)
- **Daily Login**: +10 Studs/day
- **7-Day Streak**: +50 bonus Studs
- **Game Milestones**: 100→+20, 1K→+100, 10K→+500, 100K→+2,000
- **Achievements**: Complete platform challenges

### Bonds (Purchase Currency)
- **Exchange**: 10 Studs = 1 Bond
- **Demo Purchase**: Add Bonds for testing
- Used for: Catalog items, game passes, group creation (50 Bonds)

### New User Starter Pack
- 50 Studs, 0 Bonds on account creation

## 🛠 Setup

### 1. Create Firebase Project
1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project
3. Enable **Authentication** (Email/Password + Google)
4. Enable **Cloud Firestore**
5. Copy your Firebase config

### 2. Update Config
Replace the `firebaseConfig` object in `index.html` with your Firebase project credentials:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### 3. Deploy Security Rules
Deploy `firestore.rules` and `storage.rules` to your Firebase project.

### 4. Add Assets
Place your brand assets in the `/assets/` directory:
- `assets/icon.png` — Bondaita brand icon
- `assets/bond.png` — Bond currency icon
- `assets/stud.png` — Stud currency icon

### 5. Deploy
- **GitHub Pages**: Push to repo, enable Pages from Settings
- **Any static host**: Just serve `index.html`

## 📁 Repository Structure

```
/index.html          ← Entire application
/assets/
  ├── icon.png       ← Brand icon
  ├── bond.png       ← Bond currency icon
  └── stud.png       ← Stud currency icon
/firestore.rules     ← Firestore security rules
/storage.rules       ← Storage security rules
/README.md
/LICENSE
/.nojekyll           ← Required for GitHub Pages
```

## 🎨 Tech Stack

- **HTML5, CSS3, Vanilla JS (ES6+)** — Single file
- **Firebase v10** — Auth, Firestore (CDN)
- **Chart.js v4** — Creator analytics (CDN)
- **Google Fonts** — Inter (CDN)
- **Custom Inline SVGs** — 80+ icons, no external libraries

## 📱 Pages

| Route | Description |
|-------|-------------|
| `#/` | Landing page |
| `#/login` | Sign in |
| `#/signup` | Create account |
| `#/discover` | Game discovery hub |
| `#/game/:id` | Game detail |
| `#/profile/:id` | User profile |
| `#/avatar` | Avatar customization |
| `#/catalog` | Item marketplace |
| `#/catalog/:id` | Item detail |
| `#/friends` | Friends management |
| `#/messages` | Real-time messaging |
| `#/groups` | Groups list |
| `#/groups/:id` | Group detail |
| `#/create` | Creator hub |
| `#/settings` | User settings |
| `#/currency` | Bonds & Studs exchange |
| `#/search` | Search results |
| `#/notifications` | Notifications |

## 📄 License

MIT License — See [LICENSE](LICENSE) file.
