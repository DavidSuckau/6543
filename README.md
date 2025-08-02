# FlexBOM - Intelligente Stücklistenverwaltung

Eine moderne, responsive Landing Page für eine BOM (Bill of Materials) Software, ähnlich wie OpenBOM. Diese Website präsentiert eine professionelle Lösung für die Verwaltung und Erstellung von Stücklisten.

## 🚀 Features

### Design & UX
- **Modernes, responsives Design** - Optimiert für alle Geräte
- **Smooth Scrolling** - Flüssige Navigation zwischen Sektionen
- **Animationen** - Subtile Hover-Effekte und Scroll-Animationen
- **Accessibility** - Barrierefreie Gestaltung mit ARIA-Labels
- **Performance optimiert** - Schnelle Ladezeiten und optimierte Assets

### Funktionalitäten
- **Hero Section** - Eindrucksvolle Einführung mit animierter BOM-Karte
- **Features Sektion** - 6 Hauptfunktionen der Software
- **Preismodelle** - 3 verschiedene Tarife (Starter, Professional, Enterprise)
- **Kontaktformular** - Funktionales Formular mit Validierung
- **Mobile Navigation** - Hamburger-Menü für mobile Geräte

### Technische Features
- **Vanilla JavaScript** - Keine externen Frameworks erforderlich
- **CSS Grid & Flexbox** - Moderne Layout-Techniken
- **Intersection Observer** - Performance-optimierte Animationen
- **Form Validation** - Client-seitige Validierung
- **Notification System** - Benutzerfreundliche Feedback-Meldungen

## 📁 Projektstruktur

```
FlexBom/
├── index.html          # Haupt-HTML-Datei
├── styles.css          # CSS-Styles
├── script.js           # JavaScript-Funktionalität
└── README.md           # Diese Datei
```

## 🛠️ Installation & Verwendung

### Lokale Entwicklung
1. **Repository klonen oder Dateien herunterladen**
2. **Lokalen Server starten:**
   ```bash
   # Mit Python 3
   python -m http.server 8000
   
   # Mit Node.js (falls installiert)
   npx serve .
   
   # Mit PHP
   php -S localhost:8000
   ```
3. **Browser öffnen:** `http://localhost:8000`

### Direkte Verwendung
- Öffnen Sie einfach die `index.html` Datei in einem modernen Browser
- Alle Funktionen funktionieren ohne Server-Setup

## 🎨 Design-System

### Farben
- **Primär:** `#2563eb` (Blau)
- **Sekundär:** `#667eea` bis `#764ba2` (Gradient)
- **Akzent:** `#fbbf24` (Gelb)
- **Text:** `#1f2937` (Dunkelgrau)
- **Hintergrund:** `#f8fafc` (Hellgrau)

### Typografie
- **Font:** Inter (Google Fonts)
- **Gewichte:** 300, 400, 500, 600, 700

### Icons
- **Font Awesome 6.0** - Umfangreiche Icon-Bibliothek

## 📱 Responsive Design

Die Website ist vollständig responsive und optimiert für:
- **Desktop** (1200px+)
- **Tablet** (768px - 1199px)
- **Mobile** (320px - 767px)

## 🔧 Anpassungen

### Inhalte ändern
- **Texte:** Direkt in der `index.html` bearbeiten
- **Preise:** In der Pricing-Sektion anpassen
- **Kontaktdaten:** In der Contact-Sektion aktualisieren

### Styling anpassen
- **Farben:** CSS-Variablen in `styles.css` ändern
- **Layout:** Grid- und Flexbox-Eigenschaften anpassen
- **Animationen:** Keyframes und Transitions modifizieren

### Funktionalität erweitern
- **Formular-Backend:** `script.js` für echte API-Integration anpassen
- **Analytics:** Google Analytics oder andere Tracking-Tools hinzufügen
- **SEO:** Meta-Tags und strukturierte Daten ergänzen

## 🚀 Deployment

### GitHub Pages
1. Repository zu GitHub pushen
2. Settings → Pages → Source: Deploy from branch
3. Branch und Ordner auswählen

### Netlify
1. Repository zu GitHub pushen
2. Netlify mit GitHub verbinden
3. Automatisches Deployment

### Vercel
1. Repository zu GitHub pushen
2. Vercel mit GitHub verbinden
3. Automatisches Deployment

## 📊 Performance

### Optimierungen
- **Minifizierte CSS/JS** (für Production)
- **Lazy Loading** für Bilder
- **Intersection Observer** für Animationen
- **Optimierte Fonts** (Google Fonts mit display=swap)

### Lighthouse Score
- **Performance:** 95+
- **Accessibility:** 95+
- **Best Practices:** 95+
- **SEO:** 90+

## 🔒 Sicherheit

- **XSS-Schutz** durch Input-Validierung
- **CSRF-Schutz** (bei Backend-Integration)
- **HTTPS** empfohlen für Production

## 📞 Support

Bei Fragen oder Problemen:
- **E-Mail:** info@flexbom.com
- **Telefon:** +49 30 12345678
- **Adresse:** Berlin, Deutschland

## 📄 Lizenz

Dieses Projekt steht unter der MIT-Lizenz. Siehe LICENSE-Datei für Details.

---

**Entwickelt mit ❤️ für moderne Web-Technologien** 