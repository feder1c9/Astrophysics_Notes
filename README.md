# Astrophysics_notes
# 📚 Appunti di Astrophysics - A.A. 2026/2027

Benvenuti nella repository condivisa degli appunti del corso! Qui raccogliamo, scriviamo in **LaTeX** e aggiorniamo insieme il materiale delle lezioni.

---

## 🛠️ 1. Installazione e Configurazione Iniziale (Solo la prima volta)

Per scrivere e compilare gli appunti sul tuo computer devi installare **Git**, **Visual Studio Code** e un **compilatore LaTeX**. Segui la guida per il tuo sistema operativo.

### 🪟 Procedura per Windows

1. **Installa Git:**
   * Vai su [git-scm.com/download/win](https://git-scm.com/download/win), scarica l'installer (**64-bit Git for Windows Setup**) e avvialo cliccando sempre su *Next* (lascia tutte le impostazioni predefinite).
2. **Installa Visual Studio Code (VS Code):**
   * Vai su [code.visualstudio.com](https://code.visualstudio.com/), scarica l'installer per Windows e installalo.
   * *(Consigliato)* Durante l'installazione, metti la spunta su **"Aggiungi 'Apri con Code' al menu contestuale..."** e **"Aggiungi a PATH"**.
3. **Installa il compilatore LaTeX (MiKTeX + Strawberry Perl):**
   * **Passo A (MiKTeX):** Vai su [miktex.org/download](https://miktex.org/download), scarica l'installer per Windows e avvialo. Quando ti chiede *"Install missing packages on-the-fly"* (Installa pacchetti mancanti al volo), seleziona **Yes** (eviterà blocchi durante la compilazione).
   * **Passo B (Applica aggiornamenti MiKTeX):** Apri il programma **MiKTeX Console** dal menu Start, clicca su **Updates** a sinistra -> **Check for updates** e, se presenti, clicca su **Update now**.
   * **Passo C (Strawberry Perl - OBBLIGATORIO):** VS Code ha bisogno di Perl per automatizzare la compilazione del PDF. Vai su [strawberryperl.com](https://strawberryperl.com/), scarica la versione **64-bit Recommended** (`.msi`) e installala lasciando le opzioni predefinite.
   * **Riavvia il computer** al termine delle installazioni affinché Windows riconosca i nuovi programmi.

---

### 🍎 Procedura per Mac (macOS)

1. **Installa Git:**
   * Apri l'app **Terminale** (cercala con `Cmd + Spazio`), scrivi `git --version` e premi Invio. Se non è installato, macOS farà apparire una finestra automatica: clicca su **Installa** per installare gli *Strumenti da riga di comando di Xcode*.
2. **Installa Visual Studio Code (VS Code):**
   * Vai su [code.visualstudio.com](https://code.visualstudio.com/) e scarica la versione per Mac (*Universal*).
   * Apri il file `.zip` scaricato e **trascina l'icona di Visual Studio Code dentro la cartella Applicazioni**.
3. **Installa il compilatore LaTeX (MacTeX):**
   * Vai su [tug.org/mactex/mactex-download.html](https://www.tug.org/mactex/mactex-download.html) e clicca su **`MacTeX.pkg`** per scaricarlo (pesa circa 5 GB, include tutti i pacchetti matematici e non richiede configurazioni aggiuntive).
   * Apri il file `MacTeX.pkg` scaricato e segui la procedura guidata. *(Nota: su Mac Perl è già preinstallato di sistema, quindi non serve altro).*
   * *(Alternativa da Terminale se usi Homebrew)*: puoi installarlo eseguendo `brew install --cask mactex-no-gui`.

---

### ⚙️ Configurare VS Code (Per tutti: Windows e Mac)

Una volta installati i programmi, apri **Visual Studio Code** e completa questi 3 passaggi:

1. **Installa l'estensione LaTeX Workshop:**
   * Clicca sull'icona **Extensions** nella barra laterale sinistra (i quattro quadratini, oppure premi `Ctrl + Shift + X` su Windows / `Cmd + Shift + X` su Mac).
   * Cerca **`LaTeX Workshop`** (di *James Yu*) e clicca su **Install**.
2. **Configura nome ed email su Git:**
   * Dal menu in alto di VS Code clicca su **Terminal** -> **New Terminal**.
   * Nel terminale in basso, incolla questi due comandi (sostituendo i dati tra virgolette con il tuo nome e la mail del tuo account GitHub) e premi Invio dopo ciascuno:
     ```bash
     git config --global user.name "Tuo Nome"
     git config --global user.email "tua-email@esempio.com"
     ```
3. **Collega il tuo account GitHub a VS Code:**
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

## 📄 3. Come sono organizzati i file LaTeX e come compilare il PDF

Per evitare che due persone modifichino lo stesso file contemporaneamente creando conflitti, gli appunti sono divisi così:

* **`main.tex`**: è il file principale che contiene solo l'impostazione grafica, i pacchetti (`\usepackage`), l'indice e i richiami alle singole lezioni (`\input{lezioni/lezioneXX.tex}`). **Non scrivere gli appunti direttamente qui dentro.**
* **Cartella `lezioni/`**: contiene un file separato per ogni lezione (es. `lezione01.tex`, `lezione02.tex`). Qui dentro va scritto solo il contenuto della lezione (partendo da `\section{...}`), **senza** rimettere `\documentclass` o `\begin{document}`.
* **Cartella `immagini/`**: contiene tutte le immagini e i grafici richiamati negli appunti.

### Come generare e vedere il PDF su VS Code:
1. Quando salvi un file (`Ctrl + S` su Windows / `Cmd + S` su Mac), *LaTeX Workshop* compila automaticamente il documento.
2. Per vedere il PDF affiancato al codice, apri `main.tex` e clicca sull'icona **View LaTeX PDF** in alto a destra (il foglio con la lente d'ingrandimento).
3. **Nota importante:** Il file `main.pdf` generato resta solo sul tuo computer per farti vedere l'anteprima e viene ignorato da Git (tramite `.gitignore`) per evitare conflitti con gli altri colleghi.

---

## 🔄 4. Come lavorare insieme (Flusso quotidiano)

Per non sovrascrivere il lavoro degli altri, segui **sempre** questi 4 passaggi nell'ordine esatto ogni volta che apri VS Code:

### Passo A: Scarica le modifiche degli altri (`Pull`) — *FALLO SEMPRE PRIMA DI INIZIARE*
Prima di scrivere qualsiasi cosa, aggiorna la tua copia locale:
1. Clicca sull'icona **Source Control** nella barra a sinistra (quella con i tre pallini collegati da linee, oppure premi `Ctrl + Shift + G`).
2. Clicca sui tre puntini **`...`** in alto nel pannello Source Control -> **Pull**. *(In alternativa, clicca sull'icona delle frecce circolari in basso a sinistra nella barra di stato di VS Code).*

### Passo B: Scrivi o modifica gli appunti
* Apri il file della lezione su cui devi lavorare (dentro la cartella `lezioni/`) o creane uno nuovo e aggiungilo in `main.tex` con `\input{lezioni/nomefile.tex}`.
* Salva il file (`Ctrl + S` o `Cmd + S`) e controlla dal PDF che non ci siano errori di compilazione LaTeX.

### Passo C: Registra le tue modifiche (`Commit`)
Quando hai finito di sistemare una lezione:
1. Vai nel pannello **Source Control** a sinistra: vedrai i file che hai modificato sotto la voce *Changes*.
2. Passa il mouse sopra la voce *Changes* e clicca sul simbolo **`+`** (*Stage All Changes*) per preparare i file.
3. Nella casella di testo **Message** in alto, scrivi un breve messaggio chiaro di cosa hai fatto (es. `Aggiunti appunti lezione 04`).
4. Clicca sul pulsante blu **Commit**.

### Passo D: Invia le modifiche online (`Push`)
1. Subito dopo il Commit, il pulsante blu diventerà **Sync Changes** (oppure **Push**). Cliccaci sopra.
2. Se un collega ha caricato qualcosa su altri file mentre tu scrivevi, VS Code scaricherà le sue modifiche e caricherà le tue automaticamente.

---

## 🌿 5. Lavorare su modifiche grandi senza fare danni (Branch)

Se devi fare una revisione enorme o ristrutturare più capitoli, **non lavorare sul ramo principale (`main`)**, ma crea un ramo separato:
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
