<p align="center">
  <img src="images/TOOLS_GITHUB_ACTIONS_MONITOR_WATCH_BANNER.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH banner" width="100%">
</p>

# 🛠️ TOOLS-GITHUB-ACTIONS-MONITOR-WATCH

<p align="center"><a href="README.md">🇺🇸 English</a> | <a href="README_spa.md">🇪🇸 Español</a> | <a href="README_fra.md">🇫🇷 Français</a> | <a href="README_ita.md">🇮🇹 Italiano</a> | 🇩🇪 <b>Deutsch</b> | <a href="README_zho.md">🇨🇳 中文</a> | <a href="README_jpn.md">🇯🇵 日本語</a> | <a href="README_por.md">🇵🇹 Português</a></p>

### Geplante minimale Wear-OS-Smartwatch-Version der Android-App von GitHub Actions Monitor: ein schneller Blick auf deine Workflows am Handgelenk. Nur ein Gerüst: noch nichts ist umgesetzt.

<p align="center">
  <img src="https://img.shields.io/badge/License-GPL%203.0--or--later-blue.svg" alt="GPL 3.0 or later">
  <img src="https://img.shields.io/badge/Stack-Kotlin%20%2B%20Wear%20OS%20(planned)-blue.svg" alt="Kotlin and Wear OS (planned)">
  <img src="https://img.shields.io/badge/Languages-8-00E5FF.svg" alt="Languages">
  <img src="https://img.shields.io/badge/Tests-none%20yet-lightgrey.svg" alt="Tests">
  <img src="https://img.shields.io/badge/Version-0.0.1-0f6cbd.svg" alt="Version">
  <img src="https://img.shields.io/badge/Maturity-scaffolding-FFB020.svg" alt="Maturity">
</p>

---

**Ehrlichkeitsprüfung - was heute tatsächlich läuft:** nichts von der Smartwatch-App. Dieses Repository enthält nur ihre Grundlage: die Dokumente, das Manifest, die Lizenz und die gemeinsamen Repository-Prüfungen. Es gibt keinen Code, kein Paket, keinen Bildschirm, keinen Benachrichtigungsdienst und keinen Test der App, und nichts wurde auf einer Smartwatch ausprobiert.

---

## 📋 Auf einen Blick

| | |
|---|---|
| Version | `0.0.1` |
| Reifegrad | Gerüst |
| Tests | Noch keine (nur die Prüfungen des Repositorys) |
| Technologie-Stack | Kotlin und Wear OS (geplant) |
| Auf echter Hardware | Nicht auf einer Smartwatch ausgeführt |

**Springe zu:** [Überblick](#-überblick) · [Architektur](#-architektur) · [Schnellstart](#-schnellstart) · [Tests](#-tests) · [Struktur des Repositorys](#-struktur-des-repositorys) · [Verwandte Projekte](#-verwandte-projekte)

## 🚦 Projektstatus

Jede Zeile ist ein Teil dieses Repositorys, und die Ampel sagt, wie weit er heute ist. Sie beruht auf dem, was das Repository zeigen kann (Tests, Builds, Läufe), nicht auf dem, was geplant ist.

🟢 Fertig und überprüft · 🟡 Funktioniert, mit bekannten Grenzen · 🟠 Teilweise fertig oder noch nicht überprüft · 🔴 Nicht gemacht oder funktioniert nicht

| Bereich | Stand | Was das hier bedeutet |
|---|---|---|
| Grundlage des Repositorys | 🟡 | Das Manifest, die README-Dateien in acht Sprachen, die Lizenz und die gemeinsamen Repository-Prüfungen laufen in der CI. |
| Code der Smartwatch-App | 🔴 | Nicht begonnen: in diesem Repository gibt es noch kein Smartwatch-Projekt. |
| Tests | 🔴 | Die App hat keine Tests; es laufen nur die Prüfungen des Repositorys. |
| Verbindung zum Monitor | 🔴 | Nicht begonnen. Wie die Smartwatch ihre Daten bekommt (über die Android-App oder direkt), ist nicht entschieden. |
| Smartwatch und Benachrichtigungen | 🔴 | Nicht begonnen und nie auf einer Smartwatch ausgeführt; kein Benachrichtigungsdienst ist angebunden. |

## 🎯 Überblick

* **Was es sein wird:** eine minimale Wear-OS-Smartwatch-Version der Android-App, mit einem schnellen Blick darauf, ob etwas rot ist, und auf die letzten wichtigen Warnungen deines eigenen Monitors.
* **Sie folgt der Android-App:** sie entsteht nach [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) und beschränkt sich auf einen Teil dessen, was diese App zeigt.
* **Nur Lesen:** sie liest nur aus deinem Monitor. Sie schreibt nicht in GitHub und ändert nichts im Monitor.
* **Was es (noch) nicht ist:** es gibt keine App zum Installieren, kein Release und kein Datum. Dieses Repository reserviert nur ihren Platz und sagt ehrlich, was geplant ist.

## 🧩 Rolle in EH3D

TOOLS-GITHUB-ACTIONS-MONITOR-WATCH soll die minimale Wear-OS-Smartwatch-Version der Android-App [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) von GitHub Actions Monitor werden ([TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR)). Sie würde einen kleinen Teil dessen zeigen, was der Monitor schon weiß, und selbst nichts entscheiden.

## 🏛️ Architektur

<p align="center">
  <img src="images/architecture.svg" alt="Architektur von TOOLS-GITHUB-ACTIONS-MONITOR-WATCH: wer es nutzt, was es enthält und wovon es abhängt" width="100%">
</p>

Wie die Teile dieses Repositorys zusammenpassen: wer es nutzt, was es enthält und wovon es abhängt. Das Bild wird aus `docs/architecture.json` gezeichnet und gegen den Code geprüft.

## ✨ Funktionen

**Geplant, und nichts davon existiert bisher:**
* Ein Blick: ist etwas rot?
* Die letzten wichtigen Warnungen in Kurzform.
* Optional eine Vibration bei einer wichtigen Warnung, standardmäßig aus.
* Texte in acht Sprachen.

**Nicht geplant:** in GitHub zu schreiben, lange Listen oder irgendeine andere Aktion als Ansehen. Die Smartwatch wird nicht gebraucht, um den Monitor zu betreiben.

## 🔒 Sicherheit und Schutz

* Beabsichtigt: die Smartwatch-App liest nur, und jedes Zugriffstoken bleibt auf deinen Geräten und wird nur an die Adresse deines Monitors (oder an die Android-App) gesendet.
* Nichts Geheimes gehört in dieses Repository: kein Schlüssel, kein Token, keine Datei eines Benachrichtigungsdienstes und kein Signaturschlüssel.
* Das sind Entwurfsabsichten. Nichts davon existiert bisher, daher konnte es niemand prüfen.

## 🚀 Schnellstart

Es gibt noch nichts zu installieren oder auszuführen. Um die Grundlage dieses Repositorys zu prüfen, brauchst du Python 3.10 oder neuer:

```bash
python -I tools/ci_validate.py
python -I tools/make_architecture.py --check
python -I tools/make_structure.py --check --readmes
python -I -m unittest discover -s tools -p "test_*.py"
```

## 🧪 Tests

Die CI führt die Prüfungen des Repositorys und die Tests dieser Prüfungen aus. Die Smartwatch-App hat keine eigenen Tests, weil sie noch keinen Code hat, und hier wird keine Testzahl behauptet.

## 🏗️ Build und Veröffentlichung

Es gibt weder Build noch Release, weil keine Version der App existiert. Die Version `0.0.1` in `VERSION`, im Manifest und im Changelog ist die der Grundlage des Repositorys.

## 📂 Struktur des Repositorys

<p align="center">
  <img src="images/repository-structure.svg" alt="Struktur des Repositorys TOOLS-GITHUB-ACTIONS-MONITOR-WATCH" width="100%">
</p>

<details>
<summary>Textversion des Baums</summary>

```text
MONITOR-WATCH/
├── tools/
│   ├── ci_validate.py                           Manifest, Versionen, README-Parität
│   └── make_architecture.py make_structure.py   zeichnen die beiden Bilder des README
├── docs/                                        die Quellen der beiden Bilder
├── images/                                      Banner und die beiden Bilder
├── .github/                                     CI-Workflows und Vorlagen
├── VERSION                                      die Version des Repositorys
├── electro-hobby-3d.project.json                das Manifest des Projekts
├── CHANGELOG.md                                 was sich in jeder Version geändert hat
├── SECURITY.md SUPPORT.md                       Schwachstellen melden und Fragen stellen
└── CONTRIBUTING.md CODE_OF_CONDUCT.md LICENSE   Mitwirken, Verhaltenskodex und Lizenz
```

</details>

## 🗺️ Roadmap und bekannte Grenzen

**Bekannte Grenzen heute**

* Es gibt keinen Code: keine App, kein Paket, keinen Bildschirm.
* Nichts wurde auf einer Smartwatch oder mit einem echten Monitor ausprobiert.
* Die Smartwatch folgt der Android-App und kann daher nicht beginnen, bevor diese App existiert.
* Wie die Smartwatch ihre Daten bekommt, ist noch nicht entschieden.

**Als Nächstes**

* Auf die Android-App warten, entscheiden, wie die Smartwatch ihre Daten bekommt, und den kleinsten nützlichen Bildschirm bauen, mit seinen Tests in der CI.

## 🌍 Sprachen

README und Texte gibt es auf Englisch, Spanisch, Französisch, Italienisch, Deutsch, Chinesisch, Japanisch und europäischem Portugiesisch.

## 🔗 Verwandte Projekte

* [TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR): der Monitor, dessen Daten die Wear-OS-Smartwatch zeigen soll
* [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID): die geplante Android-App, der diese Wear-OS-Smartwatch-Version folgt
* [EH3D-DOCS](https://github.com/JuanenRac/EH3D-DOCS): die Konventionen und die gemeinsamen Prüfungen

## 📚 Dokumentation

* [Die Konventionen der Suite](https://github.com/JuanenRac/EH3D-DOCS/blob/main/docs/CONVENTIONS.md)
* [Änderungsprotokoll](CHANGELOG.md)

## 🤝 Mitwirken und Community

* Führe vor einem Pull Request `python -I tools/ci_validate.py` aus; die übrigen Prüfungen laufen in der CI. Siehe [CONTRIBUTING.md](CONTRIBUTING.md) und den [Verhaltenskodex](CODE_OF_CONDUCT.md).
* Das README gibt es in acht Sprachen: Eine Textänderung wird in allen acht Dateien vorgenommen, und die beiden Bilder werden aus `docs/architecture.json` und `docs/structure.json` mit `tools/make_architecture.py` und `tools/make_structure.py` gezeichnet.
* Melde eine Sicherheitslücke privat: [SECURITY.md](SECURITY.md). Fragen, Ideen und Meldungen: electrohobby3d@gmail.com ([SUPPORT.md](SUPPORT.md)).

## 👤 AUTOR

**JuanenRac (Electro Hobby 3D)** · electrohobby3d@gmail.com

## 📜 LIZENZ

Software: GPL-3.0-or-later. Siehe [LICENSE](LICENSE). Die Hardware-Entwürfe der Suite verwenden die CERN OHL-S.
