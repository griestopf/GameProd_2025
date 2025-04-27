+++
title = '3D Reconstruction (SFM)'
draft = false
weight = 50 
+++

## 1. Bilder aufnehmen

- Für ambiente Beleuchtung sorgen. Raum mit viel Licht und hellen Wänden. Ggf. durch indirekte Beleuchtung nachhelfen. Wenn möglich Tageslicht-Softboxen verwenden
- Objekt sollte an Aufnahmestelle keine Schlagschatten werfen
- Objekt so platzieren, dass es von allen Seiten zugänglich ist
- Mind. einen Kreis um das Objekt aufnehmen (blau)
  - Alle 10° ein Bild: 36 Aufnahmen pro Kreis
  - Blickrichtung möglichst horizontal (nicht von oben nach unten)
- Ggf. zweiten Kreis leicht von oben mit leicht nach unten geneigtem Blickwinkel: weitere 36 Bilder
- Vier 180°-Bögen (alle 45° einen Bogen) über das Objekt mit 10-20 Bildern pro Bogen (rot/grün)
- [Hilfs-Untergrund mit 10°- und 45°-Kreiseinteilung verwenden](img/ScanningCompas.pdf), um Überblick bei den Aufnahmen zu behalten.
  ![Scanning Setup](img/ScanningSetup.png)

- Um die Bilder zu schießen, mit Kamera um das Objekt laufen. Nicht das Objekt drehen
- Falls erwünscht: Gleiche Prozedur für die Rückseite (Standfläche der ersten Aufnahme)
- Entscheiden, ob Bilder nachbearbeitet/angeglichen werden sollen: 
  - Falls ja (mehr Arbeit, bessere Ergebnisse): 
    - Raw aufnehmen
    - Gleiche Aufnahmeparameter für alle Bilder (Belichtungszeit, Blende, ISO, Helligkeit)
    - Farbkarte verwenden
  - Falls nein (weniger Arbeit, weniger Kontrolle über Rekonstruktionsergebnis): 
    - JPG aufnehmen
    - MÖGLICHST gleiche Aufnahmeparameter für alle Bilder (Belichtungszeit, Blende, ISO, Helligkeit)
- Unschärfe im Objekt unbedingt vermeiden. Soweit möglich, Unschärfe auch in der Umgebung vermeiden



  
## 2. Bilder nachbearbeiten (optional)

Ziele: 
- Bei Raw: Bilder mit gleichem Farb-Mapping erzeugen: Gleiche Bereiche in unterschiedlichen Bildern sollen die selbe Farbwirkung haben
- Delighting: Farben mit möglichst wenig Beleuchtungseffekten (Schatten, Diffuse, Glanz, Ambient Occlusion) darstellen

Schritte
- Dazu eine digitale Entwicklungssoftware mit Bulk-Optionen wie z. B. die kostenlose Software Darktable verwenden
- Weißpunkt/Schwarzpunkt definieren:
- Farbzuordnung ggf. anhand Farbkarte
- Alle gestalterischen Prozessschritte ("filmic") ausschalten
- Pseudo-Delighting: mit Exposure und tone-equalizer Dunkle Bereiche aufhellen und helle Bereiche abdunkeln
- Ggf. schärfen


### Beispielprozedur für die Vorbereitung von JPG-Aufnahmen mit Darktable

- Bilder importieren:
  - Alle gewünschten Bilder im Ordner mit CTRL+A auswählen.
  - Per Drag & Drop in darktable einfügen.

- Referenz-Bild zur Bearbeitung auswählen:
  - Ein Bild mit gutem Fokus auf das Objekt und guten Lichtverhältnissen wählen.
  - In den „darkroom“-Modus wechseln.

- Software-Einstellungen überprüfen:
  - In den Einstellungen unter storage > xmp die Option „write sidecar file for each image“ deaktivieren (vermeidet unnötige .xmp-Dateien).
  - „filmic rgb“ und „base curve“ deaktivieren (natürlichere Darstellung).
    ![Filmic RGB Off](img/01_filmic_off.jpeg)


- Bildbearbeitung des Referenzbildes:
  - White Balance: 
    - Mit dem Eyedropper-Tool ein neutrales Grau im Bild auswählen.
      ![White Balance](img/02_white_balance.jpeg)
  - Exposure (Belichtung):
    - Schatten aufhellen, um Details besser sichtbar zu machen.
  - Tone Equalizer:
    - Helle und dunkle Bereiche ausbalancieren (Pseudo-Delighting).
  - Sharpen (Schärfen) - optional:
    - Objektkanten und Texturdetails hervorheben.

- Bearbeitungen auf andere Bilder übertragen:
   - Zurück zum Übersichtsmenü.
   - „Selective Copy“ → alle vorgenommenen Einstellungen auswählen.
   - Mit `CTRL+A` alle Bilder markieren.
   - „Selective Paste“ → Einstellungen auf alle Bilder anwenden.
     ![Selective Paste](img/03_selective_paste.jpeg)

- Export der fertigen Bilder:
  - Klare Ordnerstruktur anlegen (importierte und exportierte Bilder in getrennten Ordnern).
  - Exportformat: TIFF (Detailerhalt).
  - Optional: Bildgröße über „set size“ begrenzen (für Tests & kleinere Dateigröße).

→ Bilder sind bereit für den Structure-From-Motion-Prozess (SFM).


## 3. Bilder nach Reality Capture importieren

- Bilder per Drag and Drop 