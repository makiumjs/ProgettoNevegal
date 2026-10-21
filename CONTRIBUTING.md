# Guida alla Contribuzione — Portale Web Monte Nevegal (5ITB)

Benvenuti nel repository ufficiale del progetto scolastico **Portale Web Monte Nevegal** (Materia: **GPOI** — Gestione Progetto e Organizzazione d'Impresa).
Ogni studente e Feature Team è tenuto a rispettare rigorosamente le regole architetturali, organizzative e qualitative definite in questo documento.

---

## 🔄 1. Metodologia Scrumban & Rotazione Ruoli

Il lavoro è organizzato in Sprint iterativi gestiti su board **Scrumban** (flussi Kanban con limiti WIP + cerimonie Scrum leggere). All'inizio di ogni Sprint, all'interno di ciascuno dei 4 Feature Team ruotano i seguenti ruoli:

| Ruolo | Responsabilità nel Team |
| :--- | :--- |
| **Team Lead / Scrum Master** | Facilita il lavoro del team, rimuove i blocchi, verifica il rispetto dei limiti WIP sulla board e coordina le Pull Request. |
| **Product Representative** | Cura la qualità dei contenuti informativi, verifica la coerenza con i requisiti della pagina assegnata e si interfaccia con gli altri team. |
| **Accessibility & QA Specialist** | Verifica il rispetto dello standard WCAG 2.1 AA+, testa la navigazione da tastiera e controlla l'assenza di `<div>` / `<span>`. |
| **Core Developer** | Implementa il codice semantico HTML5/CSS, risolve eventuali errori segnalati dal validatore W3C e mantiene pulita la cronologia Git. |

---

## 🌿 2. Strategia di Branching Git

È **vietato** effettuare commit diretti sul branch `main`. Tutto lo sviluppo avviene su branch dedicati integrati tramite **Pull Request (PR)**:

1. **Branch Principale (`main`)**: Contiene esclusivamente codice stabile, validato dalla CI W3C e pubblicato su GitHub Pages.
2. **Branch di Feature Team (Assegnati agli Studenti)**:
   - `team-1/sentieri`: **Cristian Piccoli**, **Emanuele Borra**, **Enrico De Simoi**
   - `team-2/sport`: **Tommaso Cortina**, **Davide Gaio**, **Luca D'Incau**
   - `team-3/rifugi`: **Kevin Curto**, **Francesco Bonetto**
   - `team-4/info`: **Cristina Ye**, **Giovanna David**
3. **Flusso Operativo**:
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/sentieri-tabella-cai
   # Sviluppo e verifica locale
   git add sentieri.html
   git commit -m "feat(sentieri): aggiunta tabella dislivelli percorsi CAI"
   git push -u origin feature/sentieri-tabella-cai
   ```

---

## 📝 3. Convenzioni di Commit e Naming

### Messaggi di Commit (Conventional Commits)
Ogni commit deve seguire il formato: `<tipo>(<ambito>): <descrizione breve in imperativo/infinito>`

* `feat(sentieri): aggiunge sezione anello delle creste`
* `fix(info): corregge attributo scope nella tabella emergenze`
* `style(css): migliora contrasto focus-visible nei link di navigazione`
* `docs(readme): aggiorna stato sprint e link github pages`
* `ci(w3c): configura validatore automatico html5`

### Nomenclatura File e Asset
* Tutti i file nella cartella `img/` devono avere nomi in **kebab-case** e **solo lettere minuscole**, senza spazi o caratteri speciali (es. `malga-toront-estate.jpg`, `mappa-anello-creste.jpg`).
* Le dimensioni massime consigliate per ogni immagine sono `< 300 KB` con attributi `width`, `height` e `alt` obbligatori nel markup.

---

## ✅ 4. Definition of Done (DoD)

Una User Story o Task può essere spostata nella colonna **Done** e unita in `main` **solo se soddisfa tutti i seguenti criteri**:

- [ ] **HTML5 Semantico Puro**: Zero tag `<div>` e `<span>` nel codice. Uso appropriato di `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<time>`, `<address>`, `<table>`, `<dl>`.
- [ ] **Accessibilità (WCAG 2.1 AA+)**:
  - Presenza dello skip-link `<a href="#contenuto-principale" class="salto-contenuto">` funzionante.
  - Gerarchia dei titoli corretta e sequenziale (`<h1>` unico per pagina, seguito da `<h2>` e `<h3>` senza salti di livello).
  - Tutte le immagini dotate di attributo `alt` descrittivo e contestuale.
  - Tutte le tabelle provviste di `<caption>`, `<thead>`, `<tbody>` e `<th scope="col|row">`.
- [ ] **Barra di Navigazione Globale Unificata**: Tutte le pagine devono contenere il medesimo blocco `<nav>` unificato:
  ```html
  <nav aria-label="Navigazione principale">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="sentieri.html">Sentieri</a></li>
      <li><a href="sport.html">Sport</a></li>
      <li><a href="rifugi.html">Rifugi</a></li>
      <li><a href="info.html">Info Utili</a></li>
    </ul>
  </nav>
  ```
- [ ] **Validazione W3C**: Il job GitHub Actions `W3C HTML5 & Accessibilità Validator` termina con esito positivo (0 errori, 0 warning).
- [ ] **Code Review**: La Pull Request ha ricevuto l'approvazione di almeno un componente con ruolo QA/Lead prima del merge.
