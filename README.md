<p align="center">
  <img src="docs/icon.png" width="112" alt="XBrowser SHIELD Symbol">
</p>

<h1 align="center">XBrowser SHIELD</h1>

<p align="center">
  <b>Privater Browser für Android – nur HTTPS, strenger Tracker-Schutz und eingebauter Tor.</b><br>
  Ein Projekt von <b>X-Projekt</b> · Version <b>1.4.0</b> · Android <b>8.0</b> und neuer
</p>

<p align="center">
  <a href="https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/latest"><b>⬇ Download</b></a> ·
  <a href="#funktionen">Funktionen</a> ·
  <a href="#sicherheitsmodell">Sicherheit</a> ·
  <a href="#tor">Tor</a> ·
  <a href="#ehrliche-grenzen">Grenzen</a> ·
  <a href="https://xbrowser.xanonymeki.net/datenschutz/">Datenschutz</a> ·
  <a href="#english">English</a>
</p>

<p align="center">
  <img src="docs/1-startseite.png" width="150" alt="Startseite">
  <img src="docs/3-menue.png" width="150" alt="Menü">
  <img src="docs/5-schutz.png" width="150" alt="Schutzeinstellungen">
  <img src="docs/6-tabs.png" width="150" alt="Private Tabs">
  <img src="docs/7-download-warnung.png" width="150" alt="Download-Warnung">
</p>

XBrowser SHIELD ist ein Webbrowser für Android, bei dem Privatsphäre die Grundeinstellung ist und nicht
ein Schalter, den man erst suchen muss. Webseiten stellt **Mozilla GeckoView** dar – dieselbe Engine wie
Firefox, mit Mozillas Sicherheitsupdates. Darum herum baut XBrowser eigene Schutzschichten: nur verschlüsselte
Verbindungen, private Tabs, Tracker- und Link-Filter, sichere Downloads und auf Wunsch Tor, direkt in der App.

**Kein Konto. Keine Werbung. Keine Analyse- oder Tracking-Dienste. Keine Absturzberichte.**
X-Projekt erfährt nicht, welche Seiten du besuchst oder was du suchst.

## Auf einen Blick

| | |
|---|---|
| 🔒 **Nur HTTPS** | Unverschlüsselte Verbindungen werden nicht geladen; `http://`-Links werden zu `https://`. |
| 🕶 **Jeder Tab ist privat** | Cookies und Website-Daten verschwinden, sobald die Tabs geschlossen sind. |
| 🛡 **Tracker-Schutz** | Strenger Schutz von Mozilla plus eigener SHIELD-Filter, Zähler „· 7 Tracker blockiert“. |
| 🧅 **Tor eingebaut** | Ohne Zusatz-App, mit eigener Tor-Verbindung pro Website, Brücken und .onion-Seiten. |
| 🧩 **Add-ons** | uBlock Origin und Buster (Captcha-Hilfe) mit einem Tipp. |
| ✅ **Signierte Updates** | Die App prüft Update-Informationen mit einer digitalen Signatur. |

## Download

Aktuelle Version: **[XBrowser SHIELD 1.4.0](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/tag/android-v1.4.0)**

| Datei | Für welches Gerät? |
|---|---|
| [`XBrowser-SHIELD-Android8-1.4.0-ARM64.apk`](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/download/android-v1.4.0/XBrowser-SHIELD-Android8-1.4.0-ARM64.apk) | **Fast alle Handys und Tablets.** Im Zweifel diese Datei. |
| [`XBrowser-SHIELD-Android8-1.4.0-ARMv7.apk`](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/download/android-v1.4.0/XBrowser-SHIELD-Android8-1.4.0-ARMv7.apk) | Ältere oder günstige Geräte mit 32-Bit-Prozessor |
| [`XBrowser-SHIELD-Android8-1.4.0-x86_64.apk`](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/download/android-v1.4.0/XBrowser-SHIELD-Android8-1.4.0-x86_64.apk) | Emulatoren und Chromebooks mit Intel-/AMD-Prozessor |
| [`SHA256SUMS.txt`](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/download/android-v1.4.0/SHA256SUMS.txt) | Prüfsummen zum Kontrollieren der Dateien |

**Installieren:** APK auf dem Handy herunterladen und öffnen. Android fragt einmal, ob dein Browser bzw.
Dateimanager Apps installieren darf („Unbekannte Apps installieren“) – erlauben, dann „Installieren“.
Danach kannst du die Erlaubnis wieder entziehen.

**Updates:** XBrowser meldet neue Versionen selbst (Menü → Einstellungen → Sicherheit & Updates). Ein
Update installierst du wie die erste Version; Lesezeichen und Einstellungen bleiben erhalten.

<details>
<summary><b>Download prüfen (empfohlen)</b></summary>

1. **Prüfsumme:** Der SHA-256-Wert der heruntergeladenen Datei muss mit dem Eintrag in `SHA256SUMS.txt`
   übereinstimmen.
   - Windows: `Get-FileHash .\XBrowser-SHIELD-Android8-1.4.0-ARM64.apk -Algorithm SHA256`
   - macOS / Linux: `shasum -a 256 XBrowser-SHIELD-Android8-1.4.0-ARM64.apk`
2. **Signatur:** Alle APKs sind mit demselben Schlüssel von X-Projekt signiert (APK-Signatur v2 und v3).
   Zertifikat SHA-256:
   ```
   0827ba16bec12379e935072c82130cd33e892732a72ad5fa5325b65136c169dd
   ```
   Prüfen mit `apksigner verify --print-certs XBrowser-SHIELD-Android8-1.4.0-ARM64.apk` (Android SDK).
   Android selbst lehnt ein Update ab, das mit einem anderen Schlüssel signiert ist.

Die Version aus Google Play wird von Google signiert. Ein Wechsel zwischen GitHub- und Play-Version geht
deshalb nur durch Deinstallieren und neu Installieren.
</details>

## Funktionen

### Privatsphäre
- **Private Tabs:** Jeder Tab ist eine private Sitzung. Cookies, Cache und Website-Daten bleiben nur im
  Arbeitsspeicher und sind weg, sobald alle Tabs geschlossen sind oder XBrowser beendet wird.
  „Alles löschen“ entfernt sie sofort.
- **Vollständiger Cookie-Schutz:** Jede Website bekommt ihren eigenen Cookie-Speicher; Drittanbieter-Cookies
  sind gesperrt. Dazu Schutz vor Bounce-Tracking, E-Mail-Trackern und Social-Media-Trackern.
- **Fingerprint-Schutz** der Engine und **Global Privacy Control** (Bitte an Webseiten, keine Daten zu
  verkaufen oder zu teilen).
- **Link Cleaner** entfernt bekannte Tracking-Parameter wie `utm_…` oder `fbclid` aus Links.
- **Verlauf ist standardmäßig aus.** Eingeschaltet bleibt er nur auf dem Gerät, im Tor-Modus wird er nie
  geschrieben, und Ausschalten löscht ihn vollständig.
- **Bildschirmschutz** wie bei privaten Fenstern in Firefox: keine Screenshots und keine Vorschau in
  „Zuletzt verwendet“ (in den Einstellungen erlaubbar). Die Tastatur bekommt das Inkognito-Signal.
- **Keine Website-Berechtigungen:** Standort, Kamera, Mikrofon und Benachrichtigungen sind gesperrt.
- Daten der App sind von Android-Cloud-Backups und Geräteumzügen ausgeschlossen.

### Sicherheit
- **Nur HTTPS** mit Zertifikatsanzeige: Ein Tipp auf „HTTPS“ zeigt Aussteller, Gültigkeit, Netzwerk,
  blockierte Tracker und gesperrte Rechte der Seite.
- **Heimnetz geschützt:** Webseiten können weder dein Gerät noch Router oder andere Geräte im lokalen Netz
  erreichen (Schutz vor DNS-Rebinding und Router-Angriffen).
- **Warnung vor verdächtigen Adressen:** Punycode-Domains, ungewöhnliche Adressen und typische
  Phishing-Begriffe, zusätzlich Google Safe Browsing über die Engine. Anmelde-Dialoge aus eingebetteten
  fremden Inhalten tragen eine Phishing-Warnung.
- **Sichere Downloads:** nur von HTTPS-Quellen und nur nach Bestätigung. Dateinamen werden bereinigt;
  App-Pakete, ausführbare Dateien, doppelte Endungen und falsch deklarierte APKs lösen eine Warnung aus und
  werden nie direkt geöffnet.
- **Links in andere Apps** (`mailto:`, `tel:`, `sms:`, `geo:`) nur nach Antippen und Bestätigung.
  Telefon-Links füllen nur die Nummer aus; USSD-/MMI-Codes werden abgelehnt. `intent:`, `market:`, `file:`
  und `content:` bleiben gesperrt.
- **Webseiten-Dialoge** nennen immer die Seite, von der sie kommen; mehr als drei Dialoge in 15 Sekunden
  werden unterdrückt.
- **Schutzprofile** STANDARD, STRENG und MAX (STRENG und MAX schalten JavaScript ab).
- **Verschlüsseltes DNS** über DNS.SB (DNS-over-HTTPS), optional.
- **Signierte Update-Informationen** (ECDSA P-256). Ein veralteter Browser ist ein Risiko: Nach 30 Tagen
  erinnert XBrowser an ein Update, ab Tag 90 schränkt er Webseiten ein, ab Tag 100 lädt er keine mehr.

### Tor
Tor ist eingebaut und mit einem Schalter aktiv (Einstellungen → Tor). XBrowser startet Tor lokal auf dem
Gerät, bestätigt den Tor-Ausgang über `check.torproject.org` und lädt bis dahin **keine** Seite.

- **Wie im Tor Browser angebunden:** Die Engine nutzt Tors SOCKS5-Schnittstelle. Namen von Webseiten löst
  der Tor-Ausgang auf, nie dein Gerät. Lokales DNS, WebRTC, Standort, Vorab-Verbindungen und Direkt-Fallback
  sind im Tor-Modus aus.
- **Eigene Tor-Verbindung pro Website:** Verschiedene Websites laufen über verschiedene Tor-Wege und können
  nicht über einen gemeinsamen Ausgang verknüpft werden.
- **Tor-Relais sehen:** Ein Tipp auf „◉ TOR“ zeigt Eintritt, Mitte und Ausgang der aktuellen Seite mit Land.
- **„Neue Tor-Verbindung für diese Seite“** und **„Neue Tor-Identität“** (schließt Tabs, löscht Daten,
  baut alle Verbindungen neu auf).
- **Onion-Dienste:** `.onion`-Adressen funktionieren. Bietet eine Website eine .onion-Version an, zeigt
  XBrowser „.onion-Version verfügbar ›“ oder öffnet sie auf Wunsch automatisch.
- **Brücken** gegen Tor-Sperren: obfs4, Snowflake, meek oder eigene Brücken-Zeilen. Ist eine gewählte
  Brücke nicht nutzbar, verbindet XBrowser **gar nicht** statt ungeschützt direkt.
- **Sicherheitsstufen** wie im Tor Browser: Standard · Sicherer (kein JIT, kein WebAssembly, kein WebGL) ·
  Am sichersten (JavaScript aus).
- Vereinheitlichter Fingerabdruck (`resistFingerprinting`) und Startfortschritt („Tor verbindet · 45 % …“).

Tor in XBrowser ersetzt **nicht** den offiziellen [Tor Browser](https://www.torproject.org/download/),
wenn du starke Anonymität brauchst – siehe [Grenzen](#ehrliche-grenzen).

### Add-ons
- **uBlock Origin** – Blocker für Werbung, Tracker und schädliche Seiten.
- **Buster: Captcha Solver for Humans** – löst reCAPTCHA-Audioaufgaben per Spracherkennung. In der
  Captcha-Aufgabe erscheint ein zusätzlicher Knopf. Zum Lösen geht die Audioaufgabe an einen
  Spracherkennungsdienst (standardmäßig Wit.ai von Meta); über Tor lehnt Google Audioaufgaben oft ab.
- Beide werden mit einem Tipp direkt von addons.mozilla.org installiert (von Mozilla signiert) und lassen
  sich ein- und ausschalten oder entfernen. Weitere von Mozilla signierte Add-ons lassen sich als XPI
  installieren.

### Alltag
- Bis zu 8 Tabs (4 auf Geräten mit wenig Arbeitsspeicher), neue Tabs für `target=_blank` und Pop-ups mit
  Abfrage, Lesezeichen als Kacheln auf der Startseite.
- Suche mit DuckDuckGo (Standard), Brave Search, Startpage, Mojeek oder Google; Suche in der Seite mit
  Trefferzähler.
- Downloads nach Downloads/XBrowser ohne Speicherberechtigung (Android 8/9: Speicherort wählbar).
- Webseiten-Dialoge, Datei-Upload, Datum-, Farb- und Auswahlfelder, HTTP-Anmeldung, Vollbild-Video,
  Langdruck-Menü für Links und Bilder, Teilen.
- Als **Standardbrowser** wählbar. Hell/Dunkel nach System, Textgröße, Zoomen auf allen Seiten,
  Desktop-Ansicht, Hardware-Tastaturen.
- Wiederherstellung nach Abstürzen des Inhaltsprozesses ohne Absturzschleife.

## Sicherheitsmodell

**Was XBrowser SHIELD schützen soll:** dein Surfverhalten vor Trackern und Werbenetzwerken, deine Verbindung
vor Mitlesen und Manipulation, dein Gerät und Heimnetz vor Angriffen aus Webseiten – und im Tor-Modus deine
IP-Adresse vor den besuchten Seiten.

| Schutzschicht | Wie |
|---|---|
| Engine | Mozilla GeckoView 158: Webseiten laufen in einem abgeschotteten Inhaltsprozess; Sicherheitsupdates von Mozilla |
| Verbindung | nur HTTPS, Zertifikatsprüfung durch die Engine, optional DNS-over-HTTPS oder Tor |
| Tracking | strenger Tracking-Schutz, vollständiger Cookie-Schutz, SHIELD-Filter, Link Cleaner |
| Gerät | gesperrte Website-Rechte, Heimnetz-Sperre, gefilterte App-Links, Download-Prüfung |
| Daten | private Tabs, kein Verlauf als Standard, kein Cloud-Backup, Bildschirmschutz |
| Updates | signierte Update-Informationen, APKs mit festem X-Projekt-Schlüssel, Warnung bei veralteter Version |

**Welche Verbindungen die App selbst aufbaut:** zu den Seiten, die du öffnest, und deiner Suchmaschine; zu
Mozilla und Google Safe Browsing für Schutzlisten der Engine (ohne besuchte Adressen im Klartext); höchstens alle
sechs Stunden zu GitHub für die signierte Update-Datei; im Tor-Modus zum Tor-Netz und zu
`check.torproject.org`; zu DNS.SB nur, wenn du es einschaltest. Einzelheiten:
[Datenschutzerklärung](https://xbrowser.xanonymeki.net/datenschutz/).

**Getestet:** automatische Unit-, Robolectric- und Lint-Prüfungen; Emulator-Tests auf Android 8.0 und 15;
Tor, Brücken, .onion und Buster auf einem Samsung Galaxy S21 (Android 14). Das ist **kein** unabhängiges
Sicherheitsaudit.

**Sicherheitslücke gefunden?** Bitte vertraulich an
[apple20255@proton.me](mailto:apple20255@proton.me) – nicht als öffentliches Issue.

## Ehrliche Grenzen

- **Kein Browser ist „100 % sicher“**, und XBrowser SHIELD garantiert keine Anonymität. Er wurde **nicht
  unabhängig geprüft**.
- **Tor:** XBrowser ist nicht der Tor Browser. Webseiten können XBrowser-Nutzer von Tor-Browser-Nutzern
  unterscheiden. Links, die andere Apps öffnen (E-Mail, Telefon, Karten, heruntergeladene Dateien), laufen
  nicht über Tor; XBrowser warnt davor. Für starke Anonymität den offiziellen Tor Browser verwenden.
- **Add-ons** laufen auch im Tor-Modus und können Webseiten lesen und verändern – nur vertrauenswürdige
  Add-ons installieren.
- DRM-Inhalte (z. B. manche Streamingdienste) und Website-Rechte wie Kamera, Mikrofon, Standort und
  Benachrichtigungen sind bewusst gesperrt. Manche „Anmelden mit …“-Fenster in eingebetteten Rahmen
  können scheitern.
- Die Webseiten-Engine ist Mozilla GeckoView. Die eigene XBrowser-Engine ist ein Forschungsprojekt und
  nicht Teil der Browserfunktionen.

## Systemvoraussetzungen

Android 8.0 oder neuer · ARM64, ARMv7 oder x86_64 · Download je nach Gerät 190–260 MB

## Lizenzen und Herkunft

XBrowser SHIELD ist ein Projekt von X-Projekt und **kein offizielles Produkt** von Mozilla oder dem Tor Project.

- Mozilla GeckoView – [Mozilla Public License 2.0](https://www.mozilla.org/MPL/2.0/);
  Quellcode: [github.com/mozilla-firefox/firefox](https://github.com/mozilla-firefox/firefox)
- Tor 0.4.9.12 über [Guardian Project tor-android](https://github.com/guardianproject/tor-android) mit OpenSSL,
  libevent, zlib und zstd – BSD-3-Clause, Apache 2.0, zlib-Lizenz
- Brücken: [IPtProxy](https://github.com/tladesignz/IPtProxy) (MIT) mit
  [Lyrebird](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/lyrebird) (obfs4, meek;
  BSD, das Projekt enthält zusätzlich den GPLv3-Text) und
  [Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake) (BSD-3-Clause)
- AndroidX und Kotlin – Apache 2.0 · Tor-GeoIP-Daten aus der IPFire Location Database – CC BY-SA 4.0
- uBlock Origin und Buster werden von addons.mozilla.org geladen und stehen unter ihren eigenen Lizenzen (GPLv3).

Alle Lizenztexte und Copyright-Vermerke: [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) – in der App unter
Einstellungen → Lizenzen → „Alle Lizenztexte“.

Kontakt: [apple20255@proton.me](mailto:apple20255@proton.me) ·
[Datenschutzerklärung](https://xbrowser.xanonymeki.net/datenschutz/) ·
[Privacy Policy (English)](https://xbrowser.xanonymeki.net/privacy/)

---

## English

**XBrowser SHIELD** is a privacy-first web browser for Android 8.0+, made by **X-Projekt**. It renders pages
with **Mozilla GeckoView** (the engine of Firefox) and adds its own protection layers:

- **HTTPS only**, certificate details with one tap, and protection of your home network against web pages.
- **Every tab is private**; total cookie protection, strict tracking protection, link cleaning, Global
  Privacy Control, no history by default, screenshot protection.
- **Built-in Tor** without an extra app: SOCKS5 with remote DNS like Tor Browser, a separate Tor circuit
  for every website, relay view with countries, `.onion` sites and Onion-Location, bridges (obfs4,
  Snowflake, meek, custom) that fail closed, and Tor Browser's security levels.
- **Add-ons:** uBlock Origin and Buster (captcha helper) with one tap from addons.mozilla.org.
- **Safe downloads**, confirmed links to other apps, signed update information.
- **No account, no ads, no analytics, no crash reports.**

**Download:** [latest release](https://github.com/anonymex3/XBrowser-SHIELD-DOWNLOADS/releases/latest) –
ARM64 fits almost every phone. Signing certificate SHA-256:
`0827ba16bec12379e935072c82130cd33e892732a72ad5fa5325b65136c169dd`.

**Limits:** no browser is "100 % secure", and XBrowser SHIELD does not guarantee anonymity. It has not been
independently audited. It is not Tor Browser; use the official Tor Browser if you need strong anonymity.

[Privacy policy](https://xbrowser.xanonymeki.net/privacy/) · Security reports:
[apple20255@proton.me](mailto:apple20255@proton.me)
