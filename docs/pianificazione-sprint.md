# Pianificazione Didattica e Sprint — GPOI (Classe 5ITB)

**Materia**: Gestione Progetto e Organizzazione d'Impresa (GPOI)  
**Periodo di Esecuzione**: Ottobre 2026 – Fine Marzo 2027  
**Monte Ore Laboratorio**: 2 ore a settimana (~40 ore totali)  
**Ciclo Valutativo**: 1 Sprint = 4 settimane (8 ore di laboratorio) $\rightarrow$ **1 Report di valutazione**

---

## 📅 Quadro Cronologico dei 4 Sprint

| Sprint | Periodo Indicativo | Ore Aula | Obiettivo di Sprint | Consegna Report |
| :---: | :--- | :---: | :--- | :--- |
| **Sprint 1** | Metà Ottobre – Metà Novembre | 8 ore | **Setup & Fondamenta**: Architettura semantica HTML5 pura, assenza `div`/`span`, CI W3C automatica, prime schede reali Nevegal. | **Report 1** (Fine Settimana 4) |
| **Sprint 2** | Metà Novembre – Natale | 8 ore | **Design System & Stile**: Implementazione CSS condiviso, palette alpina (`--forest-green`, `--rock-gray`, `--snow-white`), layout *mobile-first* e tabelle responsive. | **Report 2** (Prima delle vacanze di Natale) |
| **Sprint 3** | Metà Gennaio – Metà Febbraio | 8 ore | **Contenuti Avanzati & Integrazione**: Mappe e schede tecniche dettagliate, link incrociati tra i 4 team, ottimizzazione asset multimediali (`< 300 KB`). | **Report 3** (Fine Settimana 12) |
| **Sprint 4** | Metà Febbraio – Fine Marzo | 8 ore | **Audit, Collaudo & Rilascio Finale**: Verifica accessibilità WCAG 2.1 AA+, test cross-browser, documentazione conclusiva e pubblicazione su GitHub Pages. | **Report Finale** (Fine Marzo) |

---

## 🔄 Matrice di Rotazione Ruoli nei Feature Team

Ogni team è composto da 4 studenti. La rotazione assicura che **ogni studente sperimenti tutti i 4 ruoli professionali** prima del termine del progetto a marzo:

| Membro del Team | Sprint 1 | Sprint 2 | Sprint 3 | Sprint 4 |
| :--- | :--- | :--- | :--- | :--- |
| **Studente A** | *Scrum Master* | *Product Specialist* | *Core Developer* | *QA & Accessibilità* |
| **Studente B** | *Product Specialist* | *Core Developer* | *QA & Accessibilità* | *Scrum Master* |
| **Studente C** | *Core Developer* | *QA & Accessibilità* | *Scrum Master* | *Product Specialist* |
| **Studente D** | *QA & Accessibilità* | *Scrum Master* | *Product Specialist* | *Core Developer* |

---

## 📊 Regole per la Valutazione Periodica

1. **Scadenza Consegna**: Al termine della 4ª settimana di ogni Sprint, lo *Scrum Master* di ciascun team redige e consegna il report (basato sul modello in `docs/templates/template-report-sprint.md`).
2. **Criteri di Valutazione Docente (Scala 1-10)**:
   - Dettagliati nella [Rubrica di Valutazione GPOI](rubrica-valutazione-gpoi.md).
   - Valutazione composta da una componente **di team** (avanzamento deliverable e rispetto DoD) e una **individuale** (efficacia nell'interpretazione del ruolo a rotazione).

---

## ⏱️ Scansione Dettagliata delle Ore di Laboratorio (Sprint 1 – 4)

### Fase 0: Kick-off & Onboarding Tecnico (Metà Ottobre — 4 ore)
- **Settimana 0.1 (2h):** Presentazione portale alla LIM, insediamento Feature Team, studio di `CONTRIBUTING.md`, clonazione repository e configurazione account Git.
- **Settimana 0.2 (2h):** Esercitazione guidata su rami Git (`team-X/...`), creazione Issue, Pull Request e introduzione alla pipeline CI W3C Validator.

---

### Sprint 1: Setup Architetturale & Fondamenta Semantiche (Fine Ottobre – Novembre — 8 ore)
- **Settimana 1 (2h):** Sprint Planning, consultazione fonti territoriali Nevegal (CAI Belluno, impianti, rifugi), progettazione scheletro semantico.
- **Settimana 2 (2h):** Codifica markup HTML5 puro (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`) con zero `<div>`/`<span>`.
- **Settimana 3 (2h):** Configurazione skip-link da tastiera e sincronizzazione blocco `<nav aria-label="Navigazione principale">`.
- **Settimana 4 (2h):** Revisione QA interna, apertura Pull Request verso `main`, superamento CI W3C e consegna **Report Sprint 1**.

---

### Sprint 2: Design System, Dati Strutturati & Immagini (Dicembre – Metà Gennaio — 8 ore)
- **Settimana 1 (2h):** Rotazione ruoli, Sprint Planning, progettazione tabelle orari/dislivelli/tariffe e selezione immagini in `img/`.
- **Settimana 2 (2h):** Codifica di `<table>` accessibili (`<caption>`, `<thead>`, `<tbody>`, `<th scope="col/row">`) e liste `<dl>`.
- **Settimana 3 (2h):** Ottimizzazione immagini (`kebab-case` minuscolo), inserimento in `<figure>` con `<figcaption>` e testi `alt` contestualizzati.
- **Settimana 4 (2h):** Validazione W3C, merge Pull Request, Sprint Retrospective e consegna **Report Sprint 2**.

---

### Sprint 3: CSS Mobile-First Avanzato & Integrazione Cross-Team (Metà Gennaio – Febbraio — 8 ore)
- **Settimana 1 (2h):** Rotazione ruoli, verifica palette alpina (`--forest-green`, `--rock-gray`, `--snow-white`), responsive design su schermi mobile.
- **Settimana 2 (2h):** Griglie semantiche responsive per `<article>`, layout schede rifugi e tabelle scrollabili.
- **Settimana 3 (2h):** Ottimizzazione collegamenti incrociati tra i 4 team, stati `:focus-visible` ad alto contrasto e foglio di stampa (`@media print`).
- **Settimana 4 (2h):** Test cross-browser, Code Review incrociata, merge PR e consegna **Report Sprint 3**.

---

### Sprint 4: Audit WCAG 2.1 AA+, Raccordo Homepage & Rilascio Finale (Fine Febbraio – Fine Marzo — 8 ore)
- **Settimana 1 (2h):** Ultima rotazione ruoli, revisione congiunta della homepage `index.html` come Hub centrale.
- **Settimana 2 (2h):** Audit di accessibilità: collaudo completo navigazione solo da tastiera (`Tab`/`Shift+Tab`), contrasto cromatico $\ge 4.5:1$.
- **Settimana 3 (2h):** Risoluzione difetti residui (*Bug Bash*), congelamento del codice (*Code Freeze*) e verifica finale GitHub Actions.
- **Settimana 4 (2h):** Consegna **Report Finale**, pubblicazione definitiva su GitHub Pages e presentazione alla classe.
