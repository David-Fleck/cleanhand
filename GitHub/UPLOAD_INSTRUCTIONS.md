# 📤 GitHub Upload Anleitung

## ✅ BEREITS ERSTELLT

Folgende Dateien sind bereits im `/GitHub` Ordner vorhanden:

```
/GitHub/
├── .gitignore
├── README.md
├── UPLOAD_INSTRUCTIONS.md (diese Datei)
├── App.tsx
├── index.html
├── package.json
├── vite.config.ts
├── tsconfig.json
├── tsconfig.node.json
├── postcss.config.js
├── vercel.json
├── src/
│   └── main.tsx
└── styles/
    └── globals.css
```

---

## 📋 ZUSÄTZLICHE ORDNER DIE DU KOPIEREN MUSST

### 1. `/components/` Ordner
**WICHTIG:** Kopiere den **GESAMTEN** `/components/` Ordner aus dem Root in `/GitHub/components/`

Dieser enthält:
- `/components/component-library/` (18 Dateien)
- `/components/design-system/` (11 Dateien)
- `/components/library/` (16 Dateien)
- `/components/ui/` (50+ Dateien)
- `/components/figma/ImageWithFallback.tsx` ⚠️ PROTECTED
- `/components/BackupManager.tsx`

```bash
# Kopier-Befehl (falls du Zugriff auf Filesystem hast)
cp -R components/ GitHub/components/
```

---

### 2. `/pages/` Ordner
Kopiere den **GESAMTEN** `/pages/` Ordner in `/GitHub/pages/`

Enthält:
- `/pages/DevGateway.tsx`
- `/pages/LoginScreen.tsx`
- `/pages/Taskboard.tsx`

```bash
cp -R pages/ GitHub/pages/
```

---

### 3. `/config/` Ordner
Kopiere den **GESAMTEN** `/config/` Ordner in `/GitHub/config/`

Enthält:
- `/config/design-system-config.ts` 🔒 LOCKED FILE

```bash
cp -R config/ GitHub/config/
```

---

### 4. `/utils/` Ordner
Kopiere den **GESAMTEN** `/utils/` Ordner in `/GitHub/utils/`

Enthält:
- `/utils/fetchUtils.ts`
- `/utils/upload-audit-protocol.ts`
- `/utils/supabase/client.tsx`
- `/utils/supabase/info.tsx` ⚠️ PROTECTED

```bash
cp -R utils/ GitHub/utils/
```

---

### 5. `/supabase/` Ordner
Kopiere den **GESAMTEN** `/supabase/` Ordner in `/GitHub/supabase/`

Enthält:
- `/supabase/functions/server/index.tsx`
- `/supabase/functions/server/audit-protocol-data.tsx`
- `/supabase/functions/server/audit-runner.tsx`
- `/supabase/functions/server/kv_store.tsx` ⚠️ PROTECTED

```bash
cp -R supabase/ GitHub/supabase/
```

---

### 6. `/public/` Ordner
Kopiere den **GESAMTEN** `/public/` Ordner in `/GitHub/public/`

Enthält:
- `/public/manifest.json`
- Evtl. weitere Assets

```bash
cp -R public/ GitHub/public/
```

---

### 7. `/docs/` Ordner (OPTIONAL)
Falls du die Dokumentation auch pushen willst:

```bash
cp -R docs/ GitHub/docs/
```

Enthält:
- Design System Audits
- Code Reviews
- Guidelines
- Attribution Files

---

## 🚀 NACH DEM KOPIEREN

### Schritt 1: Überprüfe die Struktur

Deine `/GitHub/` Ordner sollte jetzt so aussehen:

```
/GitHub/
├── .gitignore
├── README.md
├── UPLOAD_INSTRUCTIONS.md
├── App.tsx
├── index.html
├── package.json
├── vite.config.ts
├── tsconfig.json
├── tsconfig.node.json
├── postcss.config.js
├── vercel.json
│
├── src/
│   └── main.tsx
│
├── styles/
│   └── globals.css
│
├── components/
│   ├── component-library/
│   ├── design-system/
│   ├── library/
│   ├── ui/
│   ├── figma/
│   └── BackupManager.tsx
│
├── pages/
│   ├── DevGateway.tsx
│   ├── LoginScreen.tsx
│   └── Taskboard.tsx
│
├── config/
│   └── design-system-config.ts
│
├── utils/
│   ├── fetchUtils.ts
│   ├── upload-audit-protocol.ts
│   └── supabase/
│       ├── client.tsx
│       └── info.tsx
│
├── supabase/
│   └── functions/
│       └── server/
│           ├── index.tsx
│           ├── audit-protocol-data.tsx
│           ├── audit-runner.tsx
│           └── kv_store.tsx
│
├── public/
│   └── manifest.json
│
└── docs/ (optional)
```

---

### Schritt 2: Erstelle neues Git Repository

```bash
cd GitHub

# Git initialisieren
git init

# Alle Dateien adden
git add .

# Ersten Commit
git commit -m "chore: Initial commit - Clean repository structure"

# Remote hinzufügen (DEINE REPO URL)
git remote add origin https://github.com/DEIN-USERNAME/DEIN-REPO.git

# Push zu Main Branch
git push -u origin main
```

---

### Schritt 3: Teste auf GitHub

1. Gehe zu deinem GitHub Repository
2. Überprüfe ob alle Dateien da sind
3. Checke die Struktur im Browser

---

## ⚠️ WICHTIGE HINWEISE

### PROTECTED FILES
Diese Dateien NIEMALS bearbeiten:
- `/components/figma/ImageWithFallback.tsx`
- `/utils/supabase/info.tsx`
- `/supabase/functions/server/kv_store.tsx`

### LOCKED FILES
Diese Dateien NUR mit expliziter Erlaubnis ändern:
- `/styles/globals.css`
- `/config/design-system-config.ts`

### Environment Variables
Die folgenden Secrets sind auf Supabase gespeichert und NICHT im Git:
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`
- `SUPABASE_SERVICE_ROLE_KEY`
- `SUPABASE_DB_URL`

Diese musst du in GitHub Secrets oder Vercel Environment Variables hinzufügen!

---

## 🛠️ ALTERNATIVE: MANUELLER UPLOAD

Falls du keinen Zugriff auf CLI hast:

1. Öffne deinen File Explorer
2. Gehe zum `/GitHub` Ordner
3. Kopiere die oben genannten Ordner **manuell** hinein
4. Gehe zu GitHub.com
5. Erstelle ein neues Repository
6. Nutze "Upload files" Button
7. Ziehe den gesamten Inhalt von `/GitHub` in den Upload-Bereich
8. Commit & Push

---

## ✅ CHECKLISTE

- [ ] `.gitignore` vorhanden
- [ ] `README.md` vorhanden
- [ ] `package.json` vorhanden
- [ ] `/src/main.tsx` vorhanden
- [ ] `/styles/globals.css` vorhanden
- [ ] `/components/` komplett kopiert
- [ ] `/pages/` komplett kopiert
- [ ] `/config/` komplett kopiert
- [ ] `/utils/` komplett kopiert
- [ ] `/supabase/` komplett kopiert
- [ ] `/public/` komplett kopiert
- [ ] Alle Config-Dateien vorhanden (vite, tsconfig, etc.)
- [ ] Git initialisiert
- [ ] Erster Commit gemacht
- [ ] Remote hinzugefügt
- [ ] Zu GitHub gepusht

---

**Status:** Bereit zum Upload! 🚀
