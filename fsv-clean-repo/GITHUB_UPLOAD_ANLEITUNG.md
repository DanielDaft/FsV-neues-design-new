# 📤 GitHub Upload Anleitung

## Schritt 1: Repository auf GitHub erstellen

1. Gehe zu [GitHub](https://github.com)
2. Klicke auf **"+"** (oben rechts) → **"New repository"**
3. Fülle die Details aus:
   - **Repository name**: `FsV-neues-design-new` (oder einen anderen Namen)
   - **Description**: "Deutsche Fahrschul-App - PWA mit Schülerverwaltung"
   - **Visibility**: Public oder Private (deine Wahl)
   - ⚠️ **WICHTIG**: **KEINE** der folgenden Optionen ankreuzen:
     - ❌ Add a README file
     - ❌ Add .gitignore
     - ❌ Choose a license
4. Klicke **"Create repository"**

## Schritt 2: Repository hochladen

Nach dem Erstellen zeigt GitHub dir Befehle an. Du benötigst nur diese:

### Option A: Per Kommandozeile (Terminal)

```bash
# 1. Navigiere zum Repository-Ordner
cd /app/fsv-clean-repo

# 2. Füge deine GitHub-Repository-URL hinzu (ersetze die URL mit deiner!)
git remote add origin https://github.com/DEIN-USERNAME/FsV-neues-design-new.git

# 3. Push zum GitHub
git push -u origin main
```

### Option B: GitHub Desktop

1. Öffne [GitHub Desktop](https://desktop.github.com/)
2. File → Add Local Repository
3. Wähle den Ordner: `/app/fsv-clean-repo`
4. Publish Repository
5. Wähle dein GitHub-Konto
6. Klicke "Publish"

## Schritt 3: Verifizierung

Nach dem Upload:
1. Gehe zu deinem GitHub-Repository
2. Du solltest sehen:
   - ✅ index.html
   - ✅ manifest.json
   - ✅ sw.js
   - ✅ README.md
   - ✅ LICENSE
   - ✅ .gitignore

## 🌐 Live-Deployment (Optional)

### GitHub Pages aktivieren:

1. Gehe zu deinem Repository auf GitHub
2. **Settings** → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** → Folder: **/ (root)**
5. Klicke **Save**
6. Nach 1-2 Minuten ist deine App live unter:
   ```
   https://DEIN-USERNAME.github.io/FsV-neues-design-new/
   ```

### Netlify Deploy (Alternative):

1. Gehe zu [Netlify](https://www.netlify.com/)
2. "Add new site" → "Import an existing project"
3. Wähle GitHub
4. Wähle dein Repository
5. Deploy Settings:
   - Build command: (leer lassen)
   - Publish directory: `/`
6. Click "Deploy"
7. Fertig! Du bekommst eine URL wie: `https://dein-site-name.netlify.app`

## 📁 Lokaler Ordner zum Hochladen

Der fertige Ordner befindet sich hier:
```
/app/fsv-clean-repo/
```

Du kannst diesen Ordner auch:
- Per FTP/SFTP auf deinen eigenen Server hochladen
- In einen ZIP komprimieren und teilen
- Auf andere Git-Plattformen hochladen (GitLab, Bitbucket)

## 🔄 Zukünftige Updates

Wenn du Änderungen machst:

```bash
cd /app/fsv-clean-repo

# Änderungen hinzufügen
git add .

# Commit mit Beschreibung
git commit -m "Beschreibung deiner Änderungen"

# Zu GitHub pushen
git push origin main
```

## 🆘 Probleme?

### Authentication Failed?

Wenn GitHub nach Passwort fragt:
1. Verwende stattdessen einen **Personal Access Token**
2. GitHub → Settings → Developer settings → Personal access tokens
3. Generate new token (classic)
4. Wähle `repo` scope
5. Verwende den Token statt deines Passworts

### Permission Denied?

```bash
# SSH-Key einrichten oder HTTPS mit Token verwenden
git remote set-url origin https://DEIN-TOKEN@github.com/DEIN-USERNAME/REPO-NAME.git
```

---

**Viel Erfolg! 🚀**
