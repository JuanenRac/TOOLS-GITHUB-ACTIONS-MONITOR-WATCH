<p align="center">
  <img src="images/TOOLS_GITHUB_ACTIONS_MONITOR_WATCH_BANNER.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH banner" width="100%">
</p>

# 🛠️ TOOLS-GITHUB-ACTIONS-MONITOR-WATCH

<p align="center"><a href="README.md">🇺🇸 English</a> | <a href="README_spa.md">🇪🇸 Español</a> | <a href="README_fra.md">🇫🇷 Français</a> | 🇮🇹 <b>Italiano</b> | <a href="README_deu.md">🇩🇪 Deutsch</a> | <a href="README_zho.md">🇨🇳 中文</a> | <a href="README_jpn.md">🇯🇵 日本語</a> | <a href="README_por.md">🇵🇹 Português</a></p>

### Versione minima prevista per smartwatch dell'app Android di GitHub Actions Monitor: uno sguardo rapido ai tuoi workflow al polso. Solo impalcatura: non è ancora implementato nulla.

<p align="center">
  <img src="https://img.shields.io/badge/License-GPL%203.0--or--later-blue.svg" alt="GPL 3.0 or later">
  <img src="https://img.shields.io/badge/Stack-Kotlin%20%2B%20Wear%20OS%20(planned)-blue.svg" alt="Kotlin and Wear OS (planned)">
  <img src="https://img.shields.io/badge/Languages-8-00E5FF.svg" alt="Languages">
  <img src="https://img.shields.io/badge/Tests-none%20yet-lightgrey.svg" alt="Tests">
  <img src="https://img.shields.io/badge/Version-0.0.1-0f6cbd.svg" alt="Version">
  <img src="https://img.shields.io/badge/Maturity-scaffolding-FFB020.svg" alt="Maturity">
</p>

---

**Verifica di onestà - ciò che gira oggi:** niente dell'app per smartwatch. Questo repository contiene solo la sua base: i documenti, il manifesto, la licenza e i controlli condivisi del repository. Non ci sono codice, pacchetto, schermate, servizio di notifiche né test dell'app, e nulla è stato provato su uno smartwatch.

---

## 📋 In breve

| | |
|---|---|
| Versione | `0.0.1` |
| Maturità | Impalcatura |
| Test | Nessuno per ora (solo i controlli del repository) |
| Stack tecnologico | Kotlin e Wear OS (previsto) |
| Su hardware reale | Mai eseguita su uno smartwatch |

**Vai a:** [Panoramica](#-panoramica) · [Architettura](#-architettura) · [Avvio rapido](#-avvio-rapido) · [Test](#-test) · [Struttura del repository](#-struttura-del-repository) · [Progetti correlati](#-progetti-correlati)

## 🚦 Stato del progetto

Ogni riga è una parte di questo repository e il semaforo dice a che punto è oggi. È scritta in base a ciò che il repository può mostrare (test, compilazioni, esecuzioni), non a ciò che è previsto.

🟢 Fatto e verificato · 🟡 Funziona, con limiti noti · 🟠 Fatto a metà o non ancora verificato · 🔴 Non fatto o non funzionante

| Area | Stato | Cosa significa qui |
|---|---|---|
| Base del repository | 🟡 | Il manifesto, i README in otto lingue, la licenza e i controlli condivisi del repository girano nella CI. |
| Codice dell'app per smartwatch | 🔴 | Non iniziato: questo repository non ha ancora alcun progetto per smartwatch. |
| Test | 🔴 | L'app non ha test; girano solo i controlli del repository. |
| Collegamento al monitor | 🔴 | Non iniziato. Non è deciso come lo smartwatch otterrà i dati (tramite l'app Android o direttamente). |
| Smartwatch e notifiche | 🔴 | Non iniziato e mai eseguito su uno smartwatch; nessun servizio di notifiche è collegato. |

## 🎯 Panoramica

* **Cosa sarà:** una versione minima per smartwatch dell'app Android, con uno sguardo rapido per sapere se qualcosa è rosso e agli ultimi avvisi importanti del tuo monitor.
* **Segue l'app Android:** viene costruita dopo [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) e si limita a una parte di ciò che quell'app mostra.
* **Sola lettura:** leggerà soltanto dal tuo monitor. Non scriverà su GitHub e non cambierà nulla nel monitor.
* **Cosa non è (ancora):** non c'è alcuna app da installare, né release, né data. Questo repository riserva solo il suo posto e dice con onestà ciò che è previsto.

## 🧩 Ruolo in EH3D

TOOLS-GITHUB-ACTIONS-MONITOR-WATCH vuole essere la versione minima per smartwatch dell'app Android [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) di GitHub Actions Monitor ([TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR)). Mostrerebbe una piccola parte di ciò che il monitor già sa e non deciderebbe nulla da sé.

## 🏛️ Architettura

<p align="center">
  <img src="images/architecture.svg" alt="Architettura di TOOLS-GITHUB-ACTIONS-MONITOR-WATCH: chi lo usa, che cosa contiene e da che cosa dipende" width="100%">
</p>

Come si incastrano le parti di questo repository: chi lo usa, che cosa contiene e da che cosa dipende. L'immagine è disegnata da `docs/architecture.json` e verificata rispetto al codice.

## ✨ Funzionalità

**Previsto, e nulla di tutto ciò esiste ancora:**
* Uno sguardo: c'è qualcosa di rosso?
* Gli ultimi avvisi importanti in forma breve.
* Facoltativamente, una vibrazione per un avviso importante, disattivata per impostazione predefinita.
* Testi in otto lingue.

**Non previsto:** scrivere su GitHub, elenchi lunghi o qualsiasi azione diversa dal guardare. Lo smartwatch non servirà per far funzionare il monitor.

## 🔒 Sicurezza e protezione

* Previsto: l'app per smartwatch legge soltanto, e qualsiasi token di accesso resta sui tuoi dispositivi e viene inviato solo all'indirizzo del tuo monitor (o all'app Android).
* Nulla di segreto deve stare in questo repository: né chiavi, né token, né file di servizi di notifica, né chiavi di firma.
* Sono intenzioni di progetto. Nulla di tutto ciò esiste ancora, quindi nessuno ha potuto verificarlo.

## 🚀 Avvio rapido

Non c'è ancora nulla da installare o eseguire. Per controllare la base di questo repository serve Python 3.10 o successivo:

```bash
python -I tools/ci_validate.py
python -I tools/make_architecture.py --check
python -I tools/make_structure.py --check --readmes
python -I -m unittest discover -s tools -p "test_*.py"
```

## 🧪 Test

La CI esegue i controlli del repository e i test di quei controlli. L'app per smartwatch non ha test propri perché non ha ancora codice, e qui non si dichiara alcun numero di test.

## 🏗️ Compilazione e rilascio

Non ci sono compilazione né release, perché non esiste alcuna versione dell'app. La versione `0.0.1` in `VERSION`, nel manifesto e nel changelog è quella della base del repository.

## 📂 Struttura del repository

<p align="center">
  <img src="images/repository-structure.svg" alt="Struttura del repository TOOLS-GITHUB-ACTIONS-MONITOR-WATCH" width="100%">
</p>

<details>
<summary>Versione testuale dell'albero</summary>

```text
MONITOR-WATCH/
├── tools/
│   ├── ci_validate.py                           manifesto, versioni, parità dei README
│   └── make_architecture.py make_structure.py   disegnano le due immagini del README
├── docs/                                        le sorgenti delle due immagini
├── images/                                      banner e le due immagini
├── .github/                                     workflow di CI e modelli
├── VERSION                                      la versione del repository
├── electro-hobby-3d.project.json                il manifesto del progetto
├── CHANGELOG.md                                 cosa è cambiato in ogni versione
├── SECURITY.md SUPPORT.md                       come segnalare una vulnerabilità e dove chiedere
└── CONTRIBUTING.md CODE_OF_CONDUCT.md LICENSE   come contribuire, codice di condotta e licenza
```

</details>

## 🗺️ Roadmap e limiti noti

**Limiti noti oggi**

* Non c'è codice: né app, né pacchetto, né schermata.
* Nulla è stato provato su uno smartwatch né con un monitor reale.
* Lo smartwatch segue l'app Android, quindi non può iniziare prima che quell'app esista.
* Non è ancora deciso come lo smartwatch ottenga i dati.

**Prossimo passo**

* Attendere l'app Android, decidere come lo smartwatch ottiene i dati e costruire la più piccola schermata utile, con i suoi test nella CI.

## 🌍 Lingue

Il README e i testi esistono in inglese, spagnolo, francese, italiano, tedesco, cinese, giapponese e portoghese europeo.

## 🔗 Progetti correlati

* [TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR): il monitor di cui lo smartwatch vuole mostrare i dati
* [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID): l'app Android prevista che questa versione per smartwatch segue
* [EH3D-DOCS](https://github.com/JuanenRac/EH3D-DOCS): le convenzioni e i controlli condivisi

## 📚 Documentazione

* [Le convenzioni della suite](https://github.com/JuanenRac/EH3D-DOCS/blob/main/docs/CONVENTIONS.md)
* [Registro delle modifiche](CHANGELOG.md)

## 🤝 Contribuire e comunità

* Prima di una pull request esegui `python -I tools/ci_validate.py`; gli altri controlli girano nella CI. Vedi [CONTRIBUTING.md](CONTRIBUTING.md) e il [codice di condotta](CODE_OF_CONDUCT.md).
* Il README esiste in otto lingue: una modifica al testo si fa in tutti e otto i file, e le due immagini sono disegnate da `docs/architecture.json` e `docs/structure.json` con `tools/make_architecture.py` e `tools/make_structure.py`.
* Segnala una vulnerabilità in privato: [SECURITY.md](SECURITY.md). Domande, idee e segnalazioni: electrohobby3d@gmail.com ([SUPPORT.md](SUPPORT.md)).

## 👤 AUTORE

**JuanenRac (Electro Hobby 3D)** · electrohobby3d@gmail.com

## 📜 LICENZA

Software: GPL-3.0-or-later. Vedi [LICENSE](LICENSE). I progetti hardware della suite usano la CERN OHL-S.
