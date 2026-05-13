# Workshop zu KI, Programmierung, Linux, Datenschutz und Social Media

## Ein fertiges Unterrichtspaket für die Oberstufe

### Überblick

Dieser Workshop vermittelt Jugendlichen praxisnah die Grundlagen von Datenschutz, IT-Sicherheit und Open-Source-Software. Alle Inhalte sind handlungsorientiert aufbereitet und in einer fertigen, abgeschotteten virtuellen Maschine (VM) umgesetzt, die sofort, ohne aufwändige Vorbereitung, einsetzbar ist.

### Zielgruppe

- Jugendliche von 15 bis 18 Jahren (mit Anpassungen auch ab 12 Jahren)
- Keine technischen Vorkenntnisse erforderlich
- Einsetzbar in Schulen, Jugendzentren, Hacking Spaces oder Projektwochen

### Aufbau des Workshops (2x 8 Stunden)

1. Einführung: Was ist Open Source? Warum ist Datenschutz wichtig?
2. Diskussion: Aktuelle Datenschutz-Themen anhand echter Medienbeiträge
3. Hands-on-Phase: Praxisnahe Übungen mit realen Werkzeugen
4. Challenges: Vertiefende Wettbewerbsaufgaben ohne Unterstützung

### Didaktisches Konzept

Der Workshop folgt einem handlungsorientierten und differenzierenden Ansatz:

- **Learning by Doing:** Aktive Mitarbeit statt Frontalunterricht
- **Individuelle Förderung:** Grundübungen für alle, Zusatz-Challenges für Schnellere
- **Authentische Materialien:** Echte Fotos (mit EXIF-Daten), echte TikTok-Videos (Fake News), reale Tracking-Szenarien
- **Selbstwirksamkeit:** Kleine Erfolgserlebnisse durch lösbare Aufgaben

Die Präsentation im universitären Vorlesungsstil ist bewusst gewählt. Sie begegnet Jugendlichen auf Augenhöhe, vermittelt ernsthaftes Arbeiten und gibt einen Vorgeschmack auf akademische Lernkulturen.

### Hands-on-Übungen im Detail

| Thema | Inhalt | Tools |
|---|---|---|
| EXIF-Daten | Analyse versteckter GPS-Koordinaten in Fotos | exiftool, OpenStreetMap |
| Passwortsicherheit | Analyse schwacher Passwörter in Demo-Dateien | John the Ripper, Python |
| Passwortverwaltung | Einrichtung und Nutzung eines Passwortmanagers | KeePassXC |
| Tracker blockieren | Identifikation und Blockierung von Web-Trackern | uBlock Origin, Firefox |
| Verschlüsselte Container | Erstellung versteckter, verschlüsselter Datenträger | VeraCrypt |
| Messenger-Verschlüsselung (historisch) | OTR-verschlüsselte Kommunikation | Pidgin, OTR-Plugin |
| Fake News erkennen | Frame-Extraktion und Rückwärtssuche | vlc, GIMP, Google Bilder, TinEye |
| Digitaler Fußabdruck | Analyse der eigenen Standortverläufe | Google Maps Timeline / Apple-Einstellungen |
| Zensur umgehen | Nutzung von Tor und alternativen DNS-Servern | Tor Browser, DNS-Konfiguration |

### KI-Module im Workshop

Ergänzend zu den Datenschutz- und Sicherheitstools enthält der Workshop ein eigenständiges KI-Projekt, das lokal und ohne externe Cloud-Dienste betrieben wird. Sieben vortrainierte Modelle werden über eine Flask-basierte Webanwendung zugänglich gemacht:

- GPT-2 (Textgenerierung)
- EasyOCR (Texterkennung aus Bildern)
- DistilBERT (Sentiment-Analyse)
- BLIP (automatische Bildbeschreibungen)
- Real-ESRGAN (Bildverbesserung, optimiert für Anime/Manga)
- Coqui TTS (Text-to-Speech auf Deutsch)
- Stable Diffusion 1.5 (Text-to-Image)

Die Anwendung läuft vollständig lokal und kann innerhalb der bereitgestellten VM betrieben werden, da alle Modelle auf der CPU laufen. 

**Datenschutzaspekt:** Keine Daten verlassen die lokale Umgebung. Das Projekt demonstriert, wie moderne KI-Modelle datenschutzkonform, ohne Cloud-Zwang und ohne Accounts, auf handelsüblicher Hardware genutzt werden können.

### Die Challenges (Spielerischer Wettbewerb)

Vier Missionen mit steigendem Schwierigkeitsgrad. Die Teilnehmenden arbeiten eigenständig, unterstützt nur durch [Duck.AI](https://duck.ai/). Preise (z.B. Süßigkeiten von Bobby's Foodstore oder SnackShop) winken den Siegern.

1. **VM-Check:** Wer erkennt als erster, dass die Umgebung eine virtuelle Maschine ist?
2. **EXIF-Stripping:** Komplette Entfernung aller Metadaten aus einem Bild – optional als Bash-Skript.
3. **Zip-Knacken:** Entschlüsselung eines passwortgeschützten Archivs.
4. **VeraCrypt-Verstecken:** Ein versteckter Container innerhalb eines Videos – außen ein Meme, innen eine verschlüsselte Datenbank.

**Abschluss-Challenge:** Kompilieren von Steghide aus dem Quellcode und Verstecken einer Datenbank in einem Bild.

### Die Arbeitsumgebung (Virtuelle Maschine)

**Technische Basis:**
- Debian Trixie mit XFCE-Desktop
- QEMU-basiert, setzt direkt auf den nativen Hypervisor des Hosts auf (WHPX, KVM, Hypervisor.framework)
- Kein separater Hypervisor wie VirtualBox oder VMware erforderlich
- Hardware-Virtualisierung erforderlich (VT-x/AMD-V)

**Vorinstallierte Open-Source-Tools:**
| Kategorie        | Tools                                                                 |
|------------------|-----------------------------------------------------------------------|
| Web           | Firefox + uBlock Origin                                              |
| Passwort      | KeePassXC, `john` (John the Ripper)                                  |
| Verschlüsselung | VeraCrypt                                                    	  |
| Metadaten     | `exiftool`                            |
| Kommunikation | Pidgin + purple-facebook + OTR Plugin, Tor-Browser                   |
| CLI Tools     | `curl`, `git`, `htop` …      					 |
| Programmierung	| VS Code, Geany, Bluefish, Python						|

**Systemzugang:**

| Benutzer | Passwort |
|---|---|
| workshop | workshop |
| root | workshop |

**Plattformunterstützung:**
- Windows 10/11 Pro, Education, Enterprise (mit WHPX)
- Linux (mit KVM)
- macOS Intel (mit Hypervisor.framework)
- Nicht lauffähig auf Apple Silicon

### Links & Downloads

- **Workshop-Repository**: [GitHub](https://github.com/sheepfreak221/IT-Workshop)
- **KI-Projekt**: [GitHub](https://github.com/sheepfreak221/KI-Projekt_ITWorkshop)
- **Virtuelle Maschine**: [Download hier](https://sheepfreak.freeddns.org/assets/downloads/WorkshopVM-Bundle.zip)
- **Folienset (LaTeX)**: [Download hier](https://sheepfreak.freeddns.org/assets/downloads/Workshop_OpenSource_Datenschutz.zip)

### Lizenz

MIT-Lizenz, der Workshop darf kopiert, geteilt, verändert und weiterentwickelt werden. Forks und Pull Requests sind ausdrücklich erwünscht.

### Fazit für Lehrkräfte

| Kriterium | Bewertung |
|---|---|
| Vorbereitungsaufwand | Gering, VM herunterladen, starten |
| Technische Hürden | Mittel, Virtualisierung muss aktiv sein |
| Differenzierung | Hoch, Grundaufgaben plus Challenges |
| Praxisbezug | Hoch, echte Beispiele, echte Tools |
| Materialqualität | Hoch, fertige Folien, Aufgaben, Lösungen |
