# Documentazione progetto sito “Angelologia” (4ª ragioneria)

Questo file descrive **cosa è stato fatto** nel codice e **come si collega al manuale** *Uso dei CSS – parte 2* (consegne del **punto 3**: “Consegne del progetto sito”), senza sostituire le indicazioni del docente su hosting Altervista e consegna Drive.

---

## 1. Requisiti del punto 3 del manuale e soddisfazione

| Richiesta del manuale | Come è stata risposta nel progetto |
|----------------------|-------------------------------------|
| Almeno **4 pagine HTML** e **un file CSS** | `index.html`, `seconda_pagina.html`, `terza_pagina.html`, `quarta_pagina.html`, `stile.css`. |
| In ogni pagina **barra di navigazione** con **pseudoclassi** e **piede** (footer) | Barra ripetuta con link interni; in `stile.css` le pseudoclassi dei link sono `a:link`, `a:visited`, `a:hover`, `a:active` (e analoghe nel footer). Piè di pagina con **licenza Creative Commons** e link alla pagina ufficiale della licenza. |
| **Tutti i tipi di inserimento CSS** coerenti con la teoria | **Foglio esterno**: `stile.css` collegato con `<link rel="stylesheet" href="stile.css">`. **Incorporato**: blocco `<style>...</style>` in `index.html` (tag `mark`) e in `terza_pagina.html` (spaziatura voci lista). **Inline**: attributo `style` su vari elementi (es. colori, larghezze immagini). **Regole condizionali nel foglio esterno**: `@media (max-width: 768px)` in `stile.css` per adattare float e navigazione (stesso file del link, altra modalità di applicazione delle regole, spesso richiesta insieme ai tre inserimenti “classici”). |
| **Impaginazione con `float` o altre proprietà** | In `seconda_pagina.html` il testo principale (`.contenitore2`) ha `float: left` e la colonna parole chiave (`.contenitore3`) ha `float: right`; dopo i blocchi flottanti c’è un contenitore con classe `clearfix` e regola `clear: both` in `stile.css`, come da teoria sul `clear` nel manuale. |
| **Commenti** in HTML e CSS (argomento, layout, parte nuova, fonti, riflessione) | Ogni HTML contiene un commento multi-riga in `<head>` con le cinque voci richieste. In cima a `stile.css` c’è un commento di blocco con motivazioni, layout, elemento nuovo, sitografia. |
| **Licenza Creative Commons** nel piede | Testo e link a **CC BY-NC-SA 4.0** (una delle licenze descritte nel manuale, con più condizioni). |
| **Layout** legato al tema e agli **elementi di ottimizzazione** | Tema spirituale/reflexivo: palette blu/indaco/azzurro, testo giustificato nei riquadri, navigazione uguale su tutte le pagine, meta `description` e `keywords` per i motori di ricerca (appendice del manuale sui meta tag). |
| **Elemento di formattazione nuovo**, commentato | **`box-shadow`** su contenitori (`.contenitore`, `.barra-nav`, `.contenitore2`, `.contenitore3`, tabella) e sulle immagini (classe `.img-ombra`). In `stile.css` è indicata la fonte tecnica (MDN). |
| **Contenuti**: immagine, lista, link interno, link esterno | Immagini `igor.webp` / `angeli.webp`; lista in `terza_pagina.html`; link interni nella nav e nel testo; link esterni (es. Wikipedia, Creative Commons) in più pagine. |
| **Bibliografia/sitografia** in commento | Presente nei commenti HTML e nel commento iniziale di `stile.css`. |

---

## 2. Migliorie estetiche e ombreggiatura

- **Intestazione** unificata (titolo con gradiente leggero e angoli arrotondati).
- **Navigazione** più leggibile su schermi piccoli (link impilati nella `@media`).
- **Ombre**: doppio effetto su alcuni contenitori (ombra “morbida” + accento laterale) e ombra più marcata sulle immagini per separarle dallo sfondo.
- **Correzioni** rispetto alla versione precedente: tag `img` chiuso male in home, `text-align` non valido (`center, justify`), errore `margin left`, parentesi graffa finale di troppo in `stile.css`, tag lista scritto in modo errato (`lI`).

Sfondo: resta `immagine_sfondo.jpg` con le proprietà già previste (`repeat`, `size`, `position`, `attachment`); se il file non c’è nella cartella, si vede comunque il colore di fondo impostato in `#sfondo`.

---

## 3. Preparazione a Bitbucket

1. **Controlla i file sensibili**: `sftp.json` è escluso dal versionamento tramite `.gitignore` (contiene host e passphrase: non va su Bitbucket). Se serve il file in locale, resta solo sulla tua macchina.
2. Inizializza o aggiorna il repository Git nella cartella del progetto, poi collega il remoto Bitbucket, ad esempio:
   - `git init` (se non già fatto)
   - `git add index.html seconda_pagina.html terza_pagina.html quarta_pagina.html stile.css DOCUMENTAZIONE.md .gitignore`
   - `git commit -m "Progetto sito Angelologia: HTML5, CSS, float, CC"`
   - `git remote add origin https://bitbucket.org/TUO_UTENTE/TUO_REPO.git`
   - `git push -u origin main` (o `master`, a seconda del branch predefinito)

3. **Cartella immagini** e **video** per la consegna Drive vanno preparati come da istruzioni del professore (non sono in questo repository se non li aggiungi tu).

---

## 4. Riferimenti al manuale (punti principali)

- **Punto 3**: consegne del progetto sito (pagine, CSS, nav + pseudoclassi, footer, float, commenti, CC, ottimizzazione, elemento nuovo, contenuti, sitografia).
- **Punto 1**: uso di `float` e `clear` per affiancare contenuti.
- **Punto 2**: criteri di ottimizzazione (chiarezza, navigazione, colori, parole chiave con `mark` in home).
- **Appendice**: `DOCTYPE html`, meta `keywords` / `description`, HTML5; tag `mark` usato in `index.html`.

Se il docente chiede esplicitamente anche il tag semantico `<nav>` o `<footer>` oltre alle classi, la struttura attuale già utilizza `<nav>` e `<footer>` con classi per lo stile.

---

*Documento generato per accompagnare il codice del progetto scolastico.*
