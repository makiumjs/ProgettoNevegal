# Benvenuti nel Progetto Nevegal — Guida per la Prima Lezione

Questa guida è pensata per essere proiettata alla LIM o condivisa con gli studenti della classe 5ITB per la prima lezione introduttiva a GitHub e al progetto di laboratorio GPOI.

---

## 💡 1. Cos'è GitHub? (Spiegazione Rapida per la Classe)

Non pensate a GitHub come a un semplice "Google Drive per programmatori".  
GitHub è contemporaneamente:
1. **Una Macchina del Tempo**: registra la storia esatta di ogni riga di codice scritta, permettendo di risalire a qualsiasi versione passata senza paura di perdere il lavoro.
2. **Uno Spazio di Lavoro Collaborativo**: permette a 16 o più persone di lavorare contemporaneamente sullo stesso sito web senza sovrascrivere o cancellare i file degli altri compagni.
3. **Una Piattaforma di Controllo Qualità**: prima che il codice diventi visibile al pubblico, un sistema automatico (CI) verifica che non ci siano errori di sintassi o violazioni delle regole di progetto.

---

## 🚀 2. Come Entrare nel Progetto Oggi (Istruzioni per gli Studenti)

### Passo 1: Creazione e Verifica dell'Account
* Se non ne avete uno, create un account gratuito su [github.com](https://github.com).
* Scegliete un *username* professionale o riconoscibile (es. `nome-cognome` o `cognome-classe`).

### Passo 2: Accettare l'Invito al Repository
* Il docente vi inviterà come collaboratori diretti del repository.
* Controllate la vostra email oppure aprite direttamente questo link per accettare l'invito:  
  👉 **[https://github.com/makiumjs/ProgettoNevegal/invitations](https://github.com/makiumjs/ProgettoNevegal/invitations)**

### Passo 3: Configurazione Iniziale della Postazione di Laboratorio
Aprite il terminale del vostro PC a scuola ed eseguite questi due comandi inserendo il vostro nome e la vostra email:

```bash
git config --global user.name "Nome Cognome"
git config --global user.email "tua-email@scuola.it"
```

### Passo 4: Scaricare il Progetto sul PC (Clone)
Posizionatevi nella vostra cartella di lavoro sul computer (es. su Documenti o Desktop) e scaricate l'intero portale con questo comando:

```bash
git clone https://github.com/makiumjs/ProgettoNevegal.git
cd ProgettoNevegal
```

---

## 🔍 3. Esplorazione Guidata dei File (In Classe)

Aprite la cartella appena scaricata con il vostro editor (es. Visual Studio Code):
1. **Aprite `index.html`**: fate doppio clic per visualizzarlo nel browser. Noterete che non c'è nessun `<div>` o `<span>`: tutto è strutturato solo con tag semantici (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`).
2. **Leggete `CONTRIBUTING.md`**: troverete le regole su come nominare i rami Git e la checklist obbligatoria da verificare prima di consegnare il lavoro.
3. **Guardate la sezione "Issues" su GitHub**: [github.com/makiumjs/ProgettoNevegal/issues](https://github.com/makiumjs/ProgettoNevegal/issues). Troverete le 4 attività di partenza assegnate ai Feature Team per il primo Sprint.

---

## ⚠️ Regola d'Oro per Evitare Errori
> **Non si lavora MAI direttamente sul ramo `main`.**  
> Nelle prossime lezioni ogni team creerà il proprio ramo dedicato (es. `team-1/sentieri`) in modo da lavorare in totale autonomia e sicurezza!
