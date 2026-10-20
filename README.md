# Astrophysics_notes
# 📚 Appunti di [Nome Corso] - A.A. [Anno/Anno]

Benvenuti nella repository condivisa degli appunti del corso! Qui raccogliamo e aggiorniamo insieme il materiale delle lezioni.

---

## 🛠️ 1. Configurazione Iniziale (Solo la prima volta)

Per modificare gli appunti dal tuo computer ti servono due programmi gratuiti:

1. **Installa Git:** Scaricalo da [git-scm.com](https://git-scm.com/) e installalo lasciando tutte le impostazioni predefinite.
2. **Installa Visual Studio Code (VS Code):** Scaricalo da [code.visualstudio.com](https://code.visualstudio.com/).
3. **Configura nome ed email in Git:**
   * Apri VS Code e apri il terminale integrato dal menu in alto: **Terminal** -> **New Terminal**.
   * Incolla questi due comandi (sostituendo i dati tra virgolette con il tuo nome e la mail del tuo account GitHub) e premi Invio dopo ciascuno:
     ```bash
     git config --global user.name "Tuo Nome"
     git config --global user.email "tua-email@esempio.com"
     ```
4. **Collega l'account GitHub a VS Code:**
   * Clicca sull'icona del **Profilo** (in basso a sinistra nella barra laterale di VS Code).
   * Clicca su **Sign in with GitHub to use...** e autorizza l'accesso dal browser.

---

## 📥 2. Come scaricare la Repository su VS Code (Clonazione)

1. Apri VS Code.
2. Premi `Ctrl + Shift + P` (su Windows/Linux) oppure `Cmd + Shift + P` (su Mac) per aprire la barra dei comandi in alto.
3. Digita **`Git: Clone`** e premi Invio.
4. Scegli **Clone from GitHub** (oppure incolla direttamente l'URL di questa pagina web).
5. Seleziona questa repository dalla lista e scegli una cartella sul tuo computer dove salvare gli appunti.
6. Quando VS Code te lo chiede in basso a destra, clicca su **Open** per aprire la cartella del progetto.

---

## 🔄 3. Come lavorare insieme (Flusso quotidiano)

Per evitare di sovrascrivere il lavoro degli altri, segui **sempre** questi 4 passaggi nell'ordine esatto ogni volta che apri VS Code:

### Passo A: Scarica le modifiche degli altri (`Pull`) — *FALLO SEMPRE PRIMA DI INIZIARE*
Prima di scrivere qualsiasi cosa, aggiorna la tua copia locale:
1. Clicca sull'icona **Source Control** nella barra a sinistra (quella con i tre pallini collegati da linee, oppure premi `Ctrl + Shift + G`).
2. Clicca sui tre puntini **`...`** in alto nel pannello Source Control -> **Pull**. *(In alternativa, clicca sull'icona delle frecce circolari in basso a sinistra nella barra di stato di VS Code).*

### Passo B: Scrivi o modifica gli appunti
* Crea o modifica i file nella cartella corretta.
* **Regola importante:** Lavora su file di testo (`.md` o `.tex`). Evita di modificare contemporaneamente lo stesso identico paragrafo su cui sta lavorando un altro collega in quel preciso minuto.
* Salva il file (`Ctrl + S` o `Cmd + S`).

### Passo C: Registra le tue modifiche (`Commit`)
Quando hai finito di sistemare una lezione o un argomento:
1. Vai nel pannello **Source Control** a sinistra: vedrai i file che hai modificato sotto la voce *Changes*.
2. Passa il mouse sopra la voce *Changes* e clicca sul simbolo **`+`** (*Stage All Changes*) per preparare i file.
3. Nella casella di testo **Message** in alto, scrivi un breve messaggio chiaro di cosa hai fatto (es. `Aggiunti appunti lezione 12 ottobre`).
4. Clicca sul pulsante blu **Commit**.

### Passo D: Invia le modifiche online (`Push`)
1. Subito dopo il Commit, il pulsante blu diventerà **Sync Changes** (oppure **Push**). Cliccaci sopra.
2. Se un collega ha caricato qualcosa mentre tu scrivevi, VS Code scaricherà le sue modifiche e caricherà le tue automaticamente.

---

## 🌿 4. Lavorare su modifiche grandi senza fare danni (Branch)

Se devi fare una revisione enorme o riscrivere un intero capitolo, **non lavorare sul ramo principale (`main`)**, ma crea un ramo separato:
1. Clicca sulla scritta **`main`** in basso a sinistra nella barra di stato di VS Code.
2. Nel menu che si apre in alto, clicca su **+ Create new branch...**.
3. Dagli un nome senza spazi (es. `revisione-capitolo-3`) e premi Invio.
4. Lavora normalmente facendo **Commit** e **Push** (clicca su *Publish Branch*).
5. Quando hai finito, vai sulla pagina GitHub della repository e clicca su **Compare & pull request** per unire il tuo lavoro al ramo principale dopo aver controllato che sia tutto ok.

---

## ⚖️ Licenza

Quest'opera è distribuita con Licenza **[Creative Commons Attribuzione - Non commerciale - Condividi allo stesso modo 4.0 Internazionale (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.it)**.

* **Sei libero di:** condividere, copiare e modificare il materiale per qualsiasi fine non commerciale.
* **Alle seguenti condizioni:** devi riconoscere una menzione di paternità adeguata agli autori, non puoi usare il materiale a scopo di lucro e, se distribuisci il materiale modificato, devi farlo con la stessa identica licenza.
