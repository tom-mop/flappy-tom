# flappyTOM - Ein süchtig machendes 8-Bit Browser Game

Steuere das rotierende TOM-Zahnrad durch die Hindernisse aus gelben Röhren.

## 🎮 Spielprinzip

- **Ziel**: Fliege so weit wie möglich durch die Röhren-Hindernisse
- **Steuerung**: Leertaste oder Mausklick zum Springen
- **Scoring**: Jede erfolgreich passierte Röhre gibt einen Punkt
- **Highscore**: Dein bester Score wird lokal gespeichert

## 🛠 Technische Details

### Aufbau
- **Single-File HTML**: Komplettes Spiel in einer HTML-Datei
- **Canvas-basiert**: Verwendet HTML5 Canvas für Rendering
- **Responsive Design**: Funktioniert auf Desktop und Mobile (max. 720x1280px)
- **8-Bit Ästhetik**: Pixelated Grafiken und retro Styling

### Spielmechanik
- **Physik**: Realistische Schwerkraft und Sprungmechanik
- **Kollisionserkennung**: Präzise Kollision zwischen Spieler und Hindernissen
- **Prozedurelle Generierung**: Zufällige Röhren-Positionen
- **Animationen**: Kontinuierliche Zahnrad-Rotation und bewegte Wolken

### Features
- ✅ Start-Bildschirm mit Anweisungen
- ✅ Game Over-Bildschirm mit Score-Anzeige
- ✅ Highscore-System mit localStorage
- ✅ Restart-Verzögerung (1 Sekunde) gegen versehentlichen Neustart
- ✅ TOM-Branding mit Karriere-Links
- ✅ Responsive Design für alle Bildschirmgrößen

## 🎨 Design-Spezifikationen

### Farbschema
- **Hintergrund**: `#E6E6E6` (Hellgrau)
- **Hindernisse**: `#FFBE5A` (TOM-Gelb)
- **Akzente**: `#FF9500` (Dunkleres Gelb)
- **Text/Rahmen**: `#333` (Dunkelgrau)

### Typografie
- **Schriftart**: Montserrat (400, 700, 900)
- **Effekte**: Mehrschichtige Text-Schatten für 8-Bit Look
- **Responsive**: Clamp-basierte Schriftgrößen

### Spieler-Charakter
- **Größe**: 44x44 Pixel (25% größer als Original)
- **Grafik**: TOM-Zahnrad PNG mit kontinuierlicher Rotation
- **Fallback**: Blauer Kreis falls PNG nicht lädt

## 🚀 Installation & Verwendung

### Lokale Ausführung
1. Datei `flappy-tom.html` herunterladen
2. `TOMzahnrad.png` in denselben Ordner legen
3. HTML-Datei im Browser öffnen
4. Spielen!

### Deployment
- Kann auf jedem Webserver gehostet werden
- Keine Server-seitigen Abhängigkeiten
- Funktioniert offline nach dem ersten Laden

## 📱 Browser-Kompatibilität

- ✅ Chrome/Chromium (empfohlen)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile Browser (iOS/Android)

### Anforderungen
- HTML5 Canvas Support
- JavaScript ES6+
- localStorage für Highscore-Speicherung

## 🎯 Spieltipps

1. **Timing**: Kurze, rhythmische Sprünge sind effektiver als lange
2. **Vorausschauen**: Plane deine Route durch die nächsten Röhren
3. **Ruhe bewahren**: Panik führt zu unkontrollierten Sprüngen
4. **Übung**: Die ersten Röhren sind am schwersten - danach wird es einfacher

## 🔧 Code-Struktur

### Hauptkomponenten
- **Game Loop**: `gameLoop()` - Hauptspiel-Schleife mit 60 FPS
- **Physics**: `updatePlayer()` - Schwerkraft und Bewegung
- **Collision**: `checkCollisions()` - Kollisionserkennung
- **Rendering**: `render()` - Canvas-Zeichnung
- **Input**: `handleInput()` - Tastatur/Maus-Steuerung

### Datenstrukturen
\`\`\`javascript
// Spieler-Objekt
player = {
    x, y,           // Position
    size,           // Größe (44px)
    velocity,       // Vertikale Geschwindigkeit
    rotation,       // Rotationswinkel
    jumpPower,      // Sprungkraft (-12)
    gravity         // Schwerkraft (0.8)
}

// Röhren-Array
pipes = [{
    x,              // Horizontale Position
    topHeight,      // Höhe der oberen Röhre
    bottomY,        // Y-Position der unteren Röhre
    bottomHeight,   // Höhe der unteren Röhre
    passed          // Ob Spieler passiert hat (Scoring)
}]
\`\`\`

## 📈 Performance

- **60 FPS**: Flüssige Animation durch requestAnimationFrame
- **Optimiert**: Effiziente Kollisionserkennung und Rendering
- **Speicher**: Automatische Bereinigung von Off-Screen Objekten
- **Mobile**: Touch-optimierte Steuerung

## 🏢 TOM-Integration

- **Branding**: TOM-Zahnrad als Spieler-Charakter
- **Farben**: TOM-Corporate Design (#FFBE5A)
- **Karriere-Links**: Integration von Recruiting-Links
- **Favicon**: TOM-Zahnrad als Browser-Icon

## 📄 Lizenz

Dieses Projekt wurde für TOM (TOM Instandhaltungssoftware) entwickelt.

---

**Viel Spaß beim Spielen! 🎮**

Für Karrieremöglichkeiten bei TOM: [Karriere im TOMteam](https://www.tom-instandhaltungssoftware.de/ueber-tom/karriere/)
