# EISERN — Krafttraining-Tracker als iPhone-App

Deine persönliche PWA für den 4-Tage-Split. Läuft im Vollbild auf dem iPhone, speichert offline, kein App-Store nötig.

---

## 📱 So holst du dir die App aufs iPhone

Du brauchst die Dateien einmal online (sog. "hosten"). Hier sind drei einfache Wege — wähl was zu dir passt:

### Option 1 — Cloudflare Pages (empfohlen, ~3 Min)

1. Geh auf https://pages.cloudflare.com → kostenlos registrieren
2. "Create a project" → "Upload assets"
3. Den **gesamten Ordner** `eisern` reinziehen (oder als ZIP hochladen)
4. Projekt-Name vergeben (z.B. `eisern-chanti`) → "Deploy site"
5. Du bekommst eine URL wie `https://eisern-chanti.pages.dev`
6. Diese URL auf dem iPhone in **Safari** öffnen
7. Teilen-Symbol (Kasten mit Pfeil nach oben) antippen → **"Zum Home-Bildschirm"**
8. Fertig. Auf dem Homescreen ist jetzt ein EISERN-Icon, das die App im Vollbild startet.

### Option 2 — Netlify Drop (am schnellsten, ohne Account)

1. https://app.netlify.com/drop öffnen
2. Den `eisern`-Ordner per Drag & Drop reinziehen
3. URL kopieren (z.B. `https://random-name-12345.netlify.app`)
4. Weiter wie oben bei Schritt 6–8

⚠️ Ohne Account verfällt die URL nach 24 Std. Für dauerhaft: kostenloser Account + "Deploys" → "Drag & Drop" da rein.

### Option 3 — GitHub Pages (wenn du eh GitHub nutzt)

1. Neues Repository erstellen, z.B. `eisern`
2. Inhalt von `eisern`-Ordner reinpushen (NICHT den Ordner selbst — die Dateien direkt im Root)
3. Settings → Pages → Source: `main` branch, root → Save
4. URL: `https://<deinusername>.github.io/eisern/`
5. Weiter wie oben bei Schritt 6–8

---

## ⚙️ Was die App kann

- **Smart-Vorschlag**: Schlägt automatisch den nächsten Trainingstag vor (Tag 1→2 direkt, sonst mind. 1 Tag Pause)
- **Aktives Tracking**: Pro Übung Gewicht, Reps und RIR pro Satz, mit Checkbox
- **Previous-Performance-Hint**: Bei jedem Satz siehst du dein letztes Gewicht & Reps für genau diesen Satz
- **Workout-Resume**: Schließt du die App mitten im Training, kannst du nahtlos weitermachen
- **Verlauf & Fortschritt**: Alle Trainings + Top-Gewicht-Visualisierung pro Übung
- **Offline-fähig**: Einmal geladen, läuft sie ohne Internet (z.B. im Gym-Keller)
- **Daten lokal**: Alles im Browser-Speicher deines iPhones, kommt nirgendwo hin

---

## 📂 Was ist in diesem Ordner

```
eisern/
├── index.html              ← Die App
├── manifest.json           ← PWA-Konfig (Name, Farben, Icons)
├── sw.js                   ← Service Worker für Offline-Modus
├── icon.svg                ← Vektor-Icon
├── icon-120.png            ← iOS Icon (iPhone Retina)
├── icon-152.png            ← iOS Icon (iPad)
├── icon-167.png            ← iOS Icon (iPad Pro)
├── icon-180.png            ← iOS Icon (iPhone Plus/Pro)
├── icon-192.png            ← Android/PWA Icon
├── icon-512.png            ← PWA Splash-Screen
├── apple-touch-icon.png    ← Standard iOS Icon
├── favicon-32.png          ← Browser-Tab Icon
└── README.md               ← Diese Anleitung
```

---

## 🔄 Wenn du was ändern willst

Die ganze Logik (Übungen, Cadence, RIR-Targets, Pausenregeln) steht oben in `index.html` in den Konstanten `PLANS` und `TRANSITIONS`. Übungen tauschen, Sätze ändern, etc. ist nur Text-Editing.

Nach Änderung: Datei neu hochladen, dann auf dem iPhone die App einmal aus dem Multitasking schließen und neu öffnen (Service Worker zieht die neue Version).

---

## ⚠️ Backup deiner Daten

Da alles lokal im iPhone gespeichert ist: Wenn du Safari-Daten löschst oder die App vom Homescreen entfernst und neu installierst, sind die Trainings weg. Falls du das willst, sag Bescheid — ich kann eine Export/Import-Funktion einbauen.

---

Viel Spaß beim Trainieren. 💪
