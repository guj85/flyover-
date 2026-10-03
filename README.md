# Flyover

3D-Satelliten-Flyover aus einer GPX-Datei – wie der Strava-Flyover, aber als MP4 zum Verschicken.

**Seite:** https://guj85.github.io/flyover-/

## Benutzung

1. GPX wählen (Strava: Aktivität → ⋯ → *GPX exportieren*, oder Garmin Connect).
2. Titel/Untertitel anpassen, Format und Länge wählen.
3. **Vorschau** spielt den Flug live ab.
4. **Video erstellen** rendert Bild für Bild ein H.264-MP4 (wartet pro Bild, bis Satellitenbild und Gelände geladen sind – dauert ein paar Minuten). Seite dabei im Vordergrund lassen; am Handy 720p nutzen.
5. **Teilen** öffnet das Teilen-Menü (z. B. WhatsApp), **Speichern** lädt die Datei herunter.

Alles läuft lokal im Browser, es wird nichts hochgeladen. Benötigt aktuelles Chrome/Edge oder Safari ab iOS 16.4.

## Technik

- [MapLibre GL JS](https://maplibre.org) 4.7 mit 3D-Gelände (`raster-dem`, 1,6-fach überhöht)
- Satellitenbilder: Esri World Imagery (© Esri, Maxar, Earthstar Geographics)
- Gelände: Mapzen/AWS Terrain Tiles (Terrarium)
- Ortsnamen: OpenFreeMap (© OpenStreetMap-Mitwirkende)
- Video: WebCodecs `VideoEncoder` + [mp4-muxer](https://github.com/Vanilagy/mp4-muxer)

Eine einzige Datei: `index.html`.
