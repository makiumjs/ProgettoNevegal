# Portale Web Monte Nevegal — Classe 5ITB

![W3C Validation](https://github.com/makiumjs/ProgettoNevegal/actions/workflows/w3c-validator.yml/badge.svg)

Progetto didattico di **GPOI (Gestione Progetto e Organizzazione d'Impresa)** sviluppato dagli studenti della classe **5ITB** (ITIS - Indirizzo Informatica).

Il portale promuove il territorio alpino del **Monte Nevegal (Belluno)** attraverso un'architettura web modulare, accessibile (**WCAG 2.1 AA+**) e scritta in **HTML5 Semantico Puro**, gestita con metodologia **Scrumban** e rotazione dei ruoli su 4 Feature Team.

---

## 🌐 Demo Live (GitHub Pages)

* **URL Produzione**: [https://makiumjs.github.io/ProgettoNevegal/](https://makiumjs.github.io/ProgettoNevegal/)

---

## 🏗️ Architettura del Repository

```text
ProgettoNevegal/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── user_story.md           # Template per l'assegnazione attività ai Feature Team
│   ├── workflows/
│   │   └── w3c-validator.yml       # Pipeline CI per validazione W3C e controllo semantico
│   └── PULL_REQUEST_TEMPLATE.md    # Template PR con checklist Definition of Done
├── docs/                           # Documentazione didattica e di gestione GPOI
│   ├── pianificazione-sprint.md    # Calendario 4 Sprint (Ottobre - Marzo, 2 ore/settimana)
│   ├── rubrica-valutazione-gpoi.md # Griglia di valutazione docente (scala 1 - 10)
│   └── templates/
│       └── template-report-sprint.md # Modello report periodico (ogni 4 settimane)
├── img/                            # Asset grafici ottimizzati (kebab-case, minuscolo)
│   ├── placeholder.jpg
│   ├── panorama-creste-nevegal.jpg
│   ├── sentiero-col-visentin.jpg
│   ├── bike-park-downhill.jpg
│   ├── malga-rifugio-visentin.jpg
│   └── stazione-meteo-piazzale.jpg
├── css/                            # Foglio di stile globale condiviso
│   └── style.css                   # Design token, reset accessibile e layout responsive
├── index.html                      # Homepage comune / Hub di navigazione
├── sentieri.html                   # Team 1: Trekking, anelli escursionistici, dislivelli
├── sport.html                      # Team 2: Downhill, sci, ciaspole, noleggio attrezzatura
├── rifugi.html                     # Team 3: Malghe, rifugi in quota, sapori tipici
├── info.html                       # Team 4: Trasporti, meteo, webcam, numeri soccorso alpino
├── README.md                       # Overview del progetto e documentazione principale
└── CONTRIBUTING.md                 # Regole Git, Scrumban, convenzioni e Definition of Done
```

---

## 📅 Pianificazione Didattica e Valutazione (GPOI)

* **Monte Ore**: 2 ore di laboratorio a settimana (Ottobre 2026 – Marzo 2027).
* **Ciclo di Sprint**: 4 Sprint da 4 settimane ciascuno (8 ore di laboratorio per Sprint).
* **Consegna Report**: Al termine di ogni Sprint viene consegnato un report di avanzamento.
* **Scala di Valutazione**: Voti da 1 a 10 assegnati secondo la [Rubrica di Valutazione GPOI](docs/rubrica-valutazione-gpoi.md).
* **Documenti di Riferimento**:
  * [Pianificazione Dettagliata dei 4 Sprint](docs/pianificazione-sprint.md)
  * [Rubrica di Valutazione Docente](docs/rubrica-valutazione-gpoi.md)
  * [Modello Report di Sprint per gli Studenti](docs/templates/template-report-sprint.md)

---

## 👥 Organizzazione dei Feature Team (Scrumban)

| Team | Area di Competenza | File di Riferimento | Contenuti Principali |
| :--- | :--- | :--- | :--- |
| **Team 1** | Sentieri & Trekking | `sentieri.html` | Anelli escursionistici, segnavia CAI, dislivelli, tempi di percorrenza |
| **Team 2** | Sport & Outdoor | `sport.html` | Bike Park, downhill, sci alpino, scialpinismo, ciaspole, noleggio |
| **Team 3** | Rifugi & Sapori | `rifugi.html` | Malghe in quota, pernottamenti, formaggio Schiz, Pastin e cucina tipica |
| **Team 4** | Info, Meteo & Sicurezza | `info.html` | Mobilità Dolomiti Bus, accesso stradale, webcam, Soccorso Alpino (112/118) |

---

## ✅ Standard Tecnici Principali

1. **HTML5 Semantico Puro**: Zero utilizzo di `<div>` e `<span>`; struttura costruita esclusivamente tramite `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<time>`, `<address>`, `<table>`, `<dl>`.
2. **Accessibilità Nativa (WCAG 2.1 AA+)**: Skip-link per navigazione da tastiera, attributi `aria-label` e `aria-current="page"`, gerarchia rigorosa dei titoli (`h1` → `h2` → `h3`), contrasto cromatico verificato ≥ 4.5:1 e tabelle con `<caption>` e `scope`.
3. **Continuous Integration**: Validazione automatica su ogni Push e Pull Request tramite GitHub Actions (`.github/workflows/w3c-validator.yml`).

Per le regole di contribuzione, il flusso Git e la **Definition of Done (DoD)** completa, consultare il file [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 🔍 Collaudo Locale Rapido

Per verificare in locale il rispetto dei vincoli architetturali prima di aprire una Pull Request:

```bash
# 1. Verifica assenza di tag <div> e <span> (deve restituire 0 occorrenze)
grep -rn -i -E "<(div|span)([[:space:]>]|$)" . --include="*.html"

# 2. Avvio server statico locale per testare navigazione e accessibilità da tastiera
python3 -m http.server 8000
```

