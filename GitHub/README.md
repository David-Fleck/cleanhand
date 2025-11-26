# Wellbeing V2 - Material Design Web App

Eine MVP Web-App mit umfassendem Design System und Component Library, die Google Material Design folgt.

## 🎯 Projekt-Struktur

```
/
├── App.tsx                              # Root Component (im ROOT!)
├── index.html                           # Entry Point
├── package.json                         # Dependencies
│
├── src/
│   └── main.tsx                         # React Entry Point
│
├── styles/
│   └── globals.css                      # Design System CSS (LOCKED)
│
├── components/
│   ├── component-library/               # Component Showcases
│   ├── design-system/                   # Design System Displays
│   ├── library/                         # Reusable Components
│   ├── ui/                              # ShadCN UI Components
│   ├── figma/                           # Figma Utilities (PROTECTED)
│   └── BackupManager.tsx                # Backup Utility
│
├── pages/
│   ├── DevGateway.tsx                   # Development Navigation
│   ├── LoginScreen.tsx                  # Login Page
│   └── Taskboard.tsx                    # Taskboard Page
│
├── config/
│   └── design-system-config.ts          # Design System Config (LOCKED)
│
├── utils/
│   ├── fetchUtils.ts                    # Fetch Utilities
│   ├── upload-audit-protocol.ts         # Audit Upload
│   └── supabase/                        # Supabase Config
│       ├── client.tsx
│       └── info.tsx
│
├── supabase/
│   └── functions/server/                # Backend Server
│       ├── index.tsx                    # Hono Server
│       ├── audit-protocol-data.tsx
│       ├── audit-runner.tsx
│       └── kv_store.tsx                 # (PROTECTED)
│
├── docs/                                # Documentation
└── public/                              # Static Assets
    └── manifest.json                    # PWA Manifest
```

## 🚀 Installation

```bash
# Dependencies installieren
npm install

# Development Server starten
npm run dev

# Production Build
npm run build

# Preview Build
npm run preview
```

## 📋 Wichtige Regeln

### ⚠️ PROTECTED FILES (NIEMALS BEARBEITEN!)
- `/supabase/functions/server/kv_store.tsx`
- `/utils/supabase/info.tsx`
- `/components/figma/ImageWithFallback.tsx`

### 🔒 LOCKED FILES (Nur mit expliziter Erlaubnis!)
- `/styles/globals.css` - Design System Tokens (Wahrheitsquelle)
- `/config/design-system-config.ts` - Design System Config

### ✅ Design System Prinzipien
- **NUR definierte Variablen/Tokens verwenden** aus `globals.css`
- **Perfekte Synchronisation** zwischen Code und visueller Dokumentation
- **Alle Änderungen** am Design System erfordern spezielle Erlaubnis

## 📱 Responsive Design

- **Primär:** iPhone SE bis iPad (375px - 1024px)
- **Sekundär:** Desktop Support
- **Fullscreen:** Läuft ohne Browser-Bars

## 🛠️ Tech Stack

- **Frontend:** React 18 + TypeScript
- **Styling:** Tailwind CSS 4.0 + CSS Custom Properties
- **Backend:** Supabase (Edge Functions + Hono)
- **Build:** Vite 6
- **UI Components:** Radix UI + Custom Library
- **Icons:** Lucide React
- **Charts:** Recharts

## 🔧 Alias Konfiguration

```ts
// @ = /src/*
import { Something } from '@/components/...'
```

## 📦 Deployment

Das Projekt ist für **Vercel** konfiguriert:

```bash
# Build Command
npm run build

# Output Directory
dist/
```

## ⚙️ Environment Variables

Bereits konfiguriert:
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`
- `SUPABASE_SERVICE_ROLE_KEY`
- `SUPABASE_DB_URL`

## 📄 Git Workflow

### Branch Struktur
- `main` - Production-ready Code
- `develop` - Development Code

### Commits
```bash
git add .
git commit -m "feat: Beschreibung"
git push origin main
```

### .gitignore
Automatisch ignoriert:
- `node_modules/`
- `dist/`
- `.env*`
- IDE Dateien (`.vscode/`, `.idea/`)
- OS Dateien (`.DS_Store`)

## 🎨 Design System

Das Design System ist in `/styles/globals.css` definiert und umfasst:

- **Typography:** Geologica Font, 6 Stufen
- **Colors:** Primary, Dark, Light, Success, Warning, Error
- **Spacing:** Fixed & Fluid (VH-responsive)
- **Border Radius:** sm, md, lg, xl, 2xl, full
- **Shadows:** Elevation System
- **Transitions:** Fast, Base, Slow

## 📚 Komponenten

### Design System Displays
- FontDisplay, ColorDisplay, BorderRadiusDisplay
- ShadowDisplay, SpacingDisplay, TransitionDisplay
- AssetDisplay, LayoutDisplay, VariablesDisplay

### Component Library
- Button, Input Field, Card, Badge
- Checkbox, Radio, Toggle, Select
- Avatar, Alert, Tabs, Breadcrumb
- Pagination, Toast, Modal, Loading
- Container, Grid, Stack

## 🔄 Figma Sync

- Struktur wird 1:1 zu Git gepusht
- **KEIN** Build-Prozess beim Export
- **KEIN** Flattening der Ordnerstruktur

## 🐛 Troubleshooting

### Import Fehler?
```ts
// RICHTIG (von /src/main.tsx)
import '../styles/globals.css'

// FALSCH
import './styles/globals.css'
```

### Build Fehler?
```bash
# Cache löschen
rm -rf node_modules dist
npm install
npm run build
```

## 📞 Support

Bei Fragen zum Design System: **Immer um Erlaubnis fragen!**

---

**Version:** 2.0.0  
**Letztes Update:** 26.11.2024
