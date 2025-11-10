# Berichtsheft-Tool - Coded Prototype

## Projektübersicht

Das **Berichtsheft-Tool** ist eine moderne, webbasierte Anwendung zur Verwaltung von Ausbildungsberichten. Dieses Projekt wurde als Teil einer Prüfungsaufgabe entwickelt und demonstriert die Umsetzung eines vollständigen User-Flow-Konzepts mit modernen Web-Technologien.

### Highlights

-  **Modernes UI** mit Tailwind CSS Framework
-  **ISO 9241 konform** (Usability-Standards)
-  **Responsive Design** für Desktop und Mobile
-  **Vollständiger Login-Flow** mit Feedback-System
-  **Zero Dependencies** - Läuft direkt im Browser

---

##  Projektstruktur

```
coded-prototype-animeclub/
│
├── index.html          # Hauptdatei mit kompletter Applikation
└── README.md          # Diese Dokumentation
```

---

##  Design & Wireframe-Umsetzung

Das Projekt basiert auf einem detaillierten Wireframe und User-Flow-Diagramm, das folgende Screens umfasst:

### 1️ **Startseite (BERICHTSHEFT-TOOL)**
- Zwei Buttons: "Login" und "Registrieren"
- Minimalistisches Design
- Klare Call-to-Action

### 2️ **Login-Screen**
- Benutzername-Eingabefeld
- Passwort-Eingabefeld
- "Angemeldet bleiben"-Checkbox
- "Passwort vergessen?"-Link
- Anmelde-Button

### 3️ **Feedback-System**
-  **Erfolgsmeldung** (grün): "Login erfolgreich ✓"
  - ISO 9241-11: Zufriedenheit
  - Visuelle Bestätigung für erfolgreichen Login
  
-  **Fehlermeldung** (rot): "Login fehlgeschlagen ✕"
  - ISO 9241-110: Fehlertoleranz
  - Klare Kommunikation bei Eingabefehlern

### 4️ **Dashboard**
- Personalisierte Begrüßung: "Willkommen, BENUTZERNAME"
- Abmelden-Button (oben rechts)
- Drei Hauptfunktionen als Cards:
  
  ** Neuen Bericht anlegen**
  - Erstellen Sie einen neuen Ausbildungsbericht
  - Icon: Dokument mit Stift
  
  ** Meine Berichte**
  - Alle Ihre bisherigen Berichte anzeigen
  - Icon: Liste
  
  ** Einstellungen**
  - Profil und Kontoeinstellungen verwalten
  - Icon: Zahnrad

---

##  Technologien

### Tailwind CSS Framework
Das Projekt nutzt **Tailwind CSS** als primäres Styling-Framework:

####  Vorteile von Tailwind CSS:
- **Utility-First Approach**: Schnelle Entwicklung durch vordefinierte Klassen
- **Responsive Design**: Mobile-first Design out of the box
- **Konsistenz**: Einheitliche Design-Sprache
- **Keine Custom CSS nötig**: Alles über HTML-Klassen steuerbar
- **Performance**: Nur genutzte Styles werden geladen
- **Moderne Ästhetik**: Professionelles Look & Feel

####  Verwendete Tailwind-Features:
```html
- Layout: flex, grid, container
- Spacing: p-{size}, m-{size}, space-{x/y}
- Typography: text-{size}, font-{weight}
- Colors: bg-{color}-{shade}, text-{color}-{shade}
- Borders: border, rounded-{size}
- Shadows: shadow-{size}
- Transitions: transition, duration-{time}
- Hover/Focus States: hover:*, focus:*
- Responsive: md:*, lg:*
```

### Weitere Technologien:
- **HTML5**: Semantische Struktur
- **Vanilla JavaScript**: Interaktivität ohne Framework-Overhead
- **CSS3 Animations**: Custom Slide-Down & Fade-In Effekte

---

##  ISO 9241 Konformität

Das Projekt folgt den international anerkannten Usability-Standards:

### ISO 9241-11: Gebrauchstauglichkeit
 **Effektivität**: Benutzer erreichen ihre Ziele (Login, Navigation)  
 **Effizienz**: Minimaler Aufwand für Aufgaben  
 **Zufriedenheit**: Positives Feedback durch Erfolgsmeldungen

### ISO 9241-110: Interaktionsprinzipien
 **Aufgabenangemessenheit**: Klare Funktionen pro Screen  
 **Selbstbeschreibungsfähigkeit**: Eindeutige Labels und Platzhalter  
 **Steuerbarkeit**: Logout-Funktion jederzeit verfügbar  
 **Erwartungskonformität**: Standardmäßige Patterns (Login-Form)  
 **Fehlertoleranz**: Validierung und klare Fehlermeldungen  
 **Individualisierbarkeit**: "Angemeldet bleiben"-Option  
 **Lernförderlichkeit**: Intuitive Navigation

---

##  Installation & Nutzung

### Voraussetzungen
- Moderner Webbrowser (Chrome, Firefox, Safari, Edge)
- **Keine** Installation von Abhängigkeiten erforderlich!

### Schritt-für-Schritt Anleitung

1. **Projekt öffnen**
   ```bash
   # Repository klonen (falls nötig)
   git clone <repository-url>
   cd coded-prototype-animeclub
   ```

2. **Anwendung starten**
   - Öffne `index.html` direkt im Browser, ODER
   - Nutze einen lokalen Server (empfohlen):
   
   **Mit Python:**
   ```bash
   python -m http.server 8000
   ```
   Dann: `http://localhost:8000` aufrufen
   
   **Mit Node.js (npx):**
   ```bash
   npx serve .
   ```
   
   **Mit VS Code:**
   - Rechtsklick auf `index.html` → "Open with Live Server"

3. **Login testen**
   - Benutzername: beliebig (z.B. "BGUECLUE")
   - Passwort: mindestens 4 Zeichen
   -  Bei korrekter Eingabe → Dashboard
   -  Bei Fehler → Fehlermeldung

4. **Features erkunden**
   - Dashboard-Cards anschauen
   - Logout-Funktion testen
   - Responsive Design prüfen (Browser-Größe ändern)

---

##  User-Flow Beschreibung

```
┌─────────────┐
│ Startseite  │
│ (Optional)  │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│ Login       │ ◄──── Logout bringt zurück
│ Screen      │
└──────┬──────┘
       │
       ├─── Fehlerhaft ──► Fehlermeldung (rot)
       │
       └─── Erfolgreich ──► Erfolgsmeldung (grün)
                │
                ▼
          ┌─────────────┐
          │ Dashboard   │
          │ - Berichte  │
          │ - Listen    │
          │ - Settings  │
          └─────────────┘
```

### Flow-Details:
1. **Login-Versuch** → Validierung
2. **Erfolgreich** → Grüne Meldung (1,5s) → Dashboard
3. **Fehlgeschlagen** → Rote Meldung (3s) → Erneut versuchen
4. **Abmelden** → Erfolgsmeldung → Zurück zum Login

---

##  Design-Entscheidungen

### Farbschema
| Element | Farbe | Tailwind Klasse | Begründung |
|---------|-------|-----------------|------------|
| Primär-Buttons | Schwarz | `bg-gray-900` | Hoher Kontrast, modern |
| Erfolg | Grün | `bg-green-500` | Universelles Erfolgs-Signal |
| Fehler | Rot | `bg-red-500` | Universelles Fehler-Signal |
| Hintergrund | Hellgrau | `bg-gray-50` | Reduziert Augenbelastung |
| Cards | Weiß | `bg-white` | Saubere Trennung |

### Typografie
- **Überschriften**: `text-3xl font-bold` → Klare Hierarchie
- **Body Text**: `text-sm/text-base` → Lesbarkeit
- **Labels**: `font-medium` → Wichtigkeit

### Spacing
- **Konsistente Abstände**: 4px-Raster (Tailwind Standard)
- **Card Padding**: `p-6` / `p-8` → Luftiger Look
- **Form Spacing**: `space-y-6` → Klare Trennung

---

##  Responsive Design

Das Layout passt sich automatisch an verschiedene Bildschirmgrößen an:

| Breakpoint | Geräte | Anpassungen |
|------------|--------|-------------|
| `< 768px` | Mobile | Single Column, Volle Breite |
| `≥ 768px` | Tablet/Desktop | 3-Column Grid für Cards |

**Tailwind Responsive Classes:**
```html
grid-cols-1 md:grid-cols-3  ← Mobile 1 Spalte, Desktop 3 Spalten
max-w-md                    ← Login: Max 448px Breite
max-w-6xl                   ← Dashboard: Max 1152px Breite
```

---


