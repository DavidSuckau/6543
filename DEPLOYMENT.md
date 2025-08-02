# 🚀 Vercel Deployment Anleitung für FlexBOM

## Voraussetzungen

1. **GitHub Account** (kostenlos)
2. **Vercel Account** (kostenlos)
3. **Node.js** (optional, für lokale Entwicklung)

## Schritt-für-Schritt Deployment

### 1. Repository auf GitHub erstellen

```bash
# Git Repository initialisieren
git init

# Alle Dateien hinzufügen
git add .

# Ersten Commit erstellen
git commit -m "Initial commit: FlexBOM Landing Page"

# GitHub Repository erstellen (manuell auf github.com)
# Dann remote hinzufügen:
git remote add origin https://github.com/YOUR_USERNAME/flexbom-landing.git
git branch -M main
git push -u origin main
```

### 2. Vercel Account erstellen

1. Gehen Sie zu [vercel.com](https://vercel.com)
2. Klicken Sie auf "Sign Up"
3. Wählen Sie "Continue with GitHub"
4. Autorisieren Sie Vercel für Ihr GitHub Account

### 3. Projekt auf Vercel deployen

#### Option A: Über Vercel Dashboard
1. **Dashboard öffnen:** [vercel.com/dashboard](https://vercel.com/dashboard)
2. **"New Project"** klicken
3. **GitHub Repository** auswählen: `flexbom-landing`
4. **Framework Preset:** "Other" auswählen
5. **Root Directory:** `/` (Standard)
6. **Build Command:** leer lassen (nicht erforderlich)
7. **Output Directory:** leer lassen (nicht erforderlich)
8. **"Deploy"** klicken

#### Option B: Über Vercel CLI
```bash
# Vercel CLI installieren
npm i -g vercel

# Im Projektverzeichnis
vercel

# Folgen Sie den Anweisungen:
# - GitHub Account verbinden
# - Repository auswählen
# - Projektname bestätigen
# - Framework: Other
# - Deploy bestätigen
```

### 4. Domain konfigurieren

Nach dem Deployment erhalten Sie eine URL wie: `https://flexbom-landing-xyz.vercel.app`

#### Custom Domain hinzufügen:
1. **Vercel Dashboard** → Ihr Projekt
2. **Settings** → **Domains**
3. **"Add Domain"** klicken
4. **Domain eingeben:** z.B. `flexbom.com`
5. **DNS-Einstellungen** folgen

## 🔧 Konfiguration

### Environment Variables (falls benötigt)
```bash
# Im Vercel Dashboard:
# Settings → Environment Variables
NODE_ENV=production
```

### Build Settings
- **Framework:** Other
- **Build Command:** (leer)
- **Output Directory:** (leer)
- **Install Command:** (leer)

### Headers & Redirects
Die `vercel.json` Datei ist bereits konfiguriert mit:
- **Security Headers**
- **Cache-Control** für CSS/JS
- **Routing** für SPA

## 📊 Monitoring & Analytics

### Vercel Analytics
1. **Dashboard** → Ihr Projekt
2. **Analytics** → **Enable**
3. **Tracking Code** wird automatisch hinzugefügt

### Google Analytics (optional)
```html
<!-- In index.html vor </head> hinzufügen: -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔄 Updates deployen

### Automatisches Deployment
- Jeder Push zu `main` Branch deployt automatisch
- Preview Deployments für Pull Requests

### Manuelles Deployment
```bash
# Lokale Änderungen
git add .
git commit -m "Update: Beschreibung der Änderungen"
git push origin main

# Oder über Vercel CLI
vercel --prod
```

## 🛠️ Troubleshooting

### Häufige Probleme

#### 1. 404 Fehler
```bash
# Überprüfen Sie die vercel.json
# Stellen Sie sicher, dass die Routes korrekt sind
```

#### 2. CSS/JS nicht geladen
```bash
# Überprüfen Sie die Pfade in HTML
# Stellen Sie sicher, dass alle Dateien committed sind
```

#### 3. Service Worker Fehler
```bash
# sw.js ist bereits erstellt
# Überprüfen Sie die Browser Console für Fehler
```

### Debugging
```bash
# Vercel Logs anzeigen
vercel logs

# Lokale Entwicklung
vercel dev
```

## 📈 Performance Optimierung

### Lighthouse Score verbessern
1. **Images optimieren** (WebP Format)
2. **Fonts optimieren** (display=swap bereits aktiv)
3. **Minify CSS/JS** (für Production)

### Caching
- **Static Assets:** 1 Jahr Cache
- **HTML:** Kein Cache (immer aktuell)

## 🔒 Sicherheit

### HTTPS
- **Automatisch aktiviert** auf Vercel
- **HSTS** Header konfiguriert

### Security Headers
```json
// Bereits in vercel.json konfiguriert:
"X-Content-Type-Options": "nosniff"
"X-Frame-Options": "DENY"
"X-XSS-Protection": "1; mode=block"
```

## 📱 PWA Features

### Service Worker
- **Offline-Funktionalität** aktiviert
- **Cache-Strategie:** Cache First

### Manifest
- **Install-Prompt** verfügbar
- **App-Icons** konfiguriert
- **Theme Colors** gesetzt

## 🎯 SEO Optimierung

### Meta Tags
- **Title, Description, Keywords** gesetzt
- **Open Graph** Tags konfiguriert
- **Twitter Cards** aktiviert

### Structured Data
```html
<!-- Optional: JSON-LD Schema hinzufügen -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "FlexBOM",
  "description": "Intelligente Stücklistenverwaltung"
}
</script>
```

## 📞 Support

Bei Problemen:
1. **Vercel Documentation:** [vercel.com/docs](https://vercel.com/docs)
2. **GitHub Issues:** Repository Issues
3. **Community:** [vercel.com/community](https://vercel.com/community)

---

**🎉 Ihr FlexBOM Projekt ist jetzt live auf Vercel!** 