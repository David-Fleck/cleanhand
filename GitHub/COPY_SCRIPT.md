# 🤖 Automatisches Kopier-Script

## Option 1: Via Figma Make Interface

Da du in Figma Make bist, kannst du die Ordner nicht direkt kopieren.

**LÖSUNG:** Bitte den Assistenten, die fehlenden Ordner zu kopieren:

```
"Bitte kopiere folgende Ordner komplett in /GitHub/:
- /components/
- /pages/
- /config/
- /utils/
- /supabase/
- /public/
"
```

---

## Option 2: Via Terminal (falls du Zugriff hast)

Falls du Zugriff auf ein Terminal hast:

```bash
#!/bin/bash

# Navigiere zum Projekt-Root
cd /pfad/zum/projekt

# Erstelle Basis-Struktur
mkdir -p GitHub

# Kopiere alle Ordner
cp -R components/ GitHub/components/
cp -R pages/ GitHub/pages/
cp -R config/ GitHub/config/
cp -R utils/ GitHub/utils/
cp -R supabase/ GitHub/supabase/
cp -R public/ GitHub/public/

# Optional: Docs kopieren
cp -R docs/ GitHub/docs/

echo "✅ Alle Ordner wurden nach /GitHub/ kopiert!"
```

---

## Option 3: Manuell (File Explorer)

1. Öffne zwei File Explorer Fenster
2. Links: Projekt Root
3. Rechts: `/GitHub` Ordner
4. Drag & Drop folgende Ordner von Links nach Rechts:
   - `components/`
   - `pages/`
   - `config/`
   - `utils/`
   - `supabase/`
   - `public/`

---

## Danach: Git Push

```bash
cd GitHub
git init
git add .
git commit -m "chore: Initial commit - Complete project structure"
git remote add origin <DEINE-REPO-URL>
git push -u origin main
```
