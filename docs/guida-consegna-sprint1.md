# 🎯 Guida Operativa di Chiusura Sprint 1 — Classe 5ITB
**Docente:** Prof. Marco Cassarino | **Materia:** GPOI (Laboratorio)  
**Obiettivo della Sessione:** Finalizzazione codice, superamento CI W3C, Pull Request verso `main` e consegna del **Report di Sprint 1** da parte di tutti i 4 Feature Team.

---

## ⚡ Comandi Base Git Indispensabili (Cheat Sheet per Tutti)

Prima di iniziare qualsiasi modifica, ogni studente deve posizionarsi nella cartella del progetto e aggiornare il repository locale:

```bash
# 1. Scarica tutte le novità da GitHub
git fetch origin
git checkout main
git pull origin main
```

Per lavorare senza bloccare i compagni e salvare le modifiche:
```bash
# 2. Spostati sul branch del tuo team (o creane uno personale)
git checkout <nome-branch>

# 3. Controlla lo stato dei file modificati
git status

# 4. Aggiungi i file e registra il commit con messaggio convenzionale
git add <nome-file.html>
git commit -m "feat(<ambito>): descrizione chiara di cosa hai aggiunto o corretto"

# 5. Invia il codice su GitHub
git push -u origin <nome-branch>
```

---

## 👥 Istruzioni Puntuali per Ogni Singolo Alunno

---

### 🏔️ FEATURE TEAM 1 — `sentieri.html` (Sentieri & Trekking CAI)
*Situazione attuale:* Team molto attivo. Ci sono due rami personali separati (Borra e De Simoi) e una PR (#7) aperta direttamente verso `main` che va riordinata.

#### 1. 🎖️ Cristian Piccoli (*Scrum Master & Lead Dev*)
* **Cosa devi fare:**
  1. Il tuo compito prioritario oggi è **coordinare l'integrazione del lavoro dei tuoi due compagni** sul ramo ufficiale `team-1/sentieri`.
  2. Scarica e unisci il lavoro di Borra (tabella CAI) e di De Simoi (layout schede) dentro `team-1/sentieri`.
  3. Chiudi la PR #7 aperta per errore verso `main` e apri la PR ufficiale di team: `team-1/sentieri` $\rightarrow$ `main`.
  4. Compila il file `docs/templates/template-report-sprint.md` per il Team 1 e consegnalo al docente.
* **Comandi Git da eseguire:**
  ```bash
  git checkout team-1/sentieri
  git pull origin team-1/sentieri
  git merge origin/feature/borra-Tabella03/11-o-descrizione
  git merge origin/feature/desimoi-schedesentiericondescrizione-o-aggiuntapaginedescrizioni
  # Se ci sono conflitti, risolvili con Borra e De Simoi in VS Code, poi:
  git add sentieri.html
  git commit -m "feat(sentieri): integrazione finale schede descrittive e tabella CAI"
  git push origin team-1/sentieri
  ```

#### 2. 🔍 Emanuele Borra (*QA & Data Specialist*)
* **Cosa devi fare:**
  1. Hai già realizzato un'ottima tabella CAI con quote, tempi e dislivelli reali (+713 m, CAI 2005/2000).
  2. Verifica l'accessibilità della tabella: controlla che ogni colonna abbia `<th scope="col">` e che la prima cella di ogni riga abbia `<th scope="row">`.
  3. Esegui il test anti-div: assicurati che in `sentieri.html` ci siano **zero `<div>` e zero `<span>`**.
  4. Dai il via libera a Piccoli per il merge finale.
* **Comandi Git da eseguire:**
  ```bash
  git checkout feature/borra-Tabella03/11-o-descrizione
  # Verifica tag non consentiti
  grep -rnE '<(div|span)([[:space:]>])' sentieri.html
  # Se pulito, segnala a Piccoli che il tuo codice è pronto
  ```

#### 3. 📝 Enrico De Simoi (*Product & Content Specialist*)
* **Cosa devi fare:**
  1. Nella tua PR #7 hai inserito link a pagine secondarie (`colVisentin.html`, `anelloPanoramico.html`, ecc.).
  2. **Attenzione:** i nomi dei file devono essere rigorosamente in `kebab-case` minuscolo (es. `col-visentin.html`, `anello-panoramico.html`).
  3. Se le sottopagine non sono ancora state create (per evitare errori 404 al click), mantieni per ora un paragrafo descrittivo sintetico all'interno della card `<article>`, rimandando la creazione dei file dedicati allo Sprint 2.
  4. Aiuta Piccoli a risolvere i conflitti tra le tue schede e la tabella di Borra.
* **Comandi Git da eseguire:**
  ```bash
  git checkout feature/desimoi-schedesentiericondescrizione-o-aggiuntapaginedescrizioni
  git pull
  # Applica le correzioni sui nomi dei link o sui testi
  git add sentieri.html
  git commit -m "fix(sentieri): correzione nomi link in kebab-case e testi schede"
  git push origin feature/desimoi-schedesentiericondescrizione-o-aggiuntapaginedescrizioni
  ```

---

### ⛷️ FEATURE TEAM 2 — `sport.html` (Sport, Bike Park & Sci)
*Situazione attuale:* Nessun branch o commit ancora caricato su GitHub. Bisogna partire subito e recuperare il lavoro oggi!

#### 4. 🎖️ Tommaso Cortina (*Scrum Master & Lead Dev*)
* **Cosa devi fare:**
  1. Crea subito il branch ufficiale `team-2/sport` su GitHub.
  2. Sposta l'Issue #2 della bacheca GitHub da **To Do** a **In Progress**.
  3. Struttura lo scheletro della pagina `sport.html` in HTML5 Semantico Puro: `<main id="contenuto-principale">`, `<section>` per Downhill/Bike Park e `<section>` per Sci Alpino/Ciaspole.
  4. Redigi il Report di Sprint 1 del Team 2.
* **Comandi Git da eseguire:**
  ```bash
  git checkout main
  git pull origin main
  git checkout -b team-2/sport
  # Modifica sport.html insieme al tuo team
  git add sport.html
  git commit -m "feat(sport): scheletro semantico e sezioni bike park e sci"
  git push -u origin team-2/sport
  ```

#### 5. 📝 Davide Gaio (*Product & Content Specialist*)
* **Cosa devi fare:**
  1. Raccogli e scrivi testi reali su:
     - **Bike Park Nevegal:** tracciati Downhill ed Enduro, noleggio e-bike e risalite con seggiovia.
     - **Sport Invernali:** piste storiche (Coca, Grava), anello di fondo, escursioni guidate con ciaspole.
  2. Nessun testo latino (*lorem ipsum*)!
  3. Inserisci i testi nelle card `<article>` preparate da Cortina.

#### 6. 🔍 Luca D'Incau (*QA & Code Reviewer*)
* **Cosa devi fare:**
  1. Progetta e codifica la **tabella delle tariffe e noleggio attrezzatura** in `sport.html`.
  2. Rispetta rigorosamente i criteri di accessibilità: inserisci `<caption>`, `<thead>`, `<tbody>`, `<th scope="col">` e `<th scope="row">`.
  3. Prima del commit finale, verifica che non sia presente nessun `<div>` o `<span>`.
* **Comandi di verifica:**
  ```bash
  grep -rnE '<(div|span)([[:space:]>])' sport.html
  ```

---

### 🧀 FEATURE TEAM 3 — `rifugi.html` (Rifugi in Quota & Sapori Tipici)
*Situazione attuale:* Il branch `team-3/rifugi` è stato creato su GitHub ma non contiene ancora modifiche.

#### 7. 🎖️ Kevin Curto (*Scrum Master & Content Lead*)
* **Cosa devi fare:**
  1. Sposta l'Issue #3 su GitHub in **In Progress**.
  2. Raccogli e redigi i dati autentici di:
     - **Rifugi in quota:** Rifugio Col Visentin (1.763 m), Rifugio Bristot (1.616 m).
     - **Malghe:** Malga Toront, Malga Faverghera.
     - **Sapori tipici:** Formaggio Schiz alla piastra, Pastin bellunese, polenta e funghi.
  3. Compila il Report di Sprint 1 per il Team 3.
* **Comandi Git da eseguire:**
  ```bash
  git checkout team-3/rifugi
  git pull origin team-3/rifugi
  # Lavora con Bonetto su rifugi.html
  git add rifugi.html
  git commit -m "feat(rifugi): censimento malghe in quota e gastronomia bellunese"
  git push origin team-3/rifugi
  ```

#### 8. 💻 Francesco Bonetto (*Core Developer & QA Specialist*)
* **Cosa devi fare:**
  1. Codifica le schede dei rifugi in `rifugi.html` usando `<article>`, inserendo per ciascuno:
     - Quota s.l.m. e periodo di apertura stagionale (con tag `<time>`).
     - Recapiti e contatti gestore racchiusi in tag `<address>`.
  2. Implementa la tabella orari/aperture con `<caption>` e `<th scope="...">`.
  3. Verifica il superamento del test semantico (zero `<div>`/`<span>`).

---

### ℹ️ FEATURE TEAM 4 — `info.html` (Mobilità Dolomiti Bus & Soccorso Alpino)
*Situazione attuale:* Cristina Ye ha già scritto tutto il codice necessario con standard eccellenti. Serve solo unirlo nel branch di team e chiudere la consegna!

#### 9. 🎖️ Giovanna David (*Scrum Master & Content Lead*)
* **Cosa devi fare:**
  1. Sposta l'Issue #4 della bacheca GitHub in **In Progress** e poi in **In Review**.
  2. Coordina con Cristina Ye l'unione del suo lavoro dal branch `CriYe007-patch-1` al branch ufficiale `team-4/info`.
  3. Compila il Report di Sprint 1 per il Team 4 (evidenziando i dati raccolti su Dolomiti Bus Linea 11 e Soccorso Alpino 112/118).
  4. Apri la Pull Request finale da `team-4/info` verso `main`.
* **Comandi Git da eseguire:**
  ```bash
  git checkout team-4/info
  git pull origin team-4/info
  git merge origin/CriYe007-patch-1
  git push origin team-4/info
  ```

#### 10. 💻 Cristina Ye (*Core Developer & QA Lead*)
* **Cosa devi fare:**
  1. Hai già realizzato un codice eccellente con orari reali Dolomiti Bus, contatti Infopoint e numeri di emergenza.
  2. Supporta Giovanna nell'eseguire il merge su `team-4/info`.
  3. Assicurati che al termine del push la pipeline GitHub Actions rimanga verde con zero errori di validazione W3C.
* **Comandi Git da eseguire:**
  ```bash
  git checkout team-4/info
  git pull origin team-4/info
  # Verifica che tutto sia allineato
  git log -n 3 --oneline
  ```

---

## 🏁 Checklist Finale di Uscita per Ogni Team (Definition of Done)
Prima di lasciare l'aula, ogni Scrum Master deve accertarsi che:
- [ ] Il file assegnato al team è stato salvato, committato e pushato sul branch `team-X/...`.
- [ ] La Pull Request verso `main` è stata aperta su GitHub.
- [ ] La pipeline CI W3C termina con la spunta verde (`✓`).
- [ ] Il file `Report di Sprint 1` è stato compilato e consegnato al docente.
- [ ] L'Issue sulla board GitHub è stata spostata in **In Review** o **Done**.
