# Documentazione progetto sito “Angelologia” (4ª ragioneria)

Questo file descrive **cosa è stato fatto** nel codice e **come si collega al manuale** *Uso dei CSS – parte 2* (consegne del **punto 3**: “Consegne del progetto sito”), senza sostituire le indicazioni del docente su hosting Altervista, consegna su Drive e modalità di consegna del corso.

---

## 1. Requisiti del punto 3 del manuale e soddisfazione

| Richiesta del manuale | Come è stata risposta nel progetto |
|----------------------|-------------------------------------|
| Almeno **4 pagine HTML** e **un file CSS** | `index.html`, `seconda_pagina.html`, `terza_pagina.html`, `quarta_pagina.html`, `stile.css`. |
| In ogni pagina **barra di navigazione** con **pseudoclassi** e **piede** (footer) | Barra ripetuta con link interni; in `stile.css` le pseudoclassi dei link sono `a:link`, `a:visited`, `a:hover`, `a:active` (e analoghe nel footer). Piè di pagina con **licenza Creative Commons** e link alla pagina ufficiale della licenza. |
| **Tipi di inserimento CSS** (come da teoria in classe) | **Foglio esterno**: `stile.css` collegato con `<link rel="stylesheet" href="stile.css">`. **Incorporato**: blocco `<style>...</style>` in `index.html` (tag `mark`) e in `terza_pagina.html` (spaziatura voci lista). **Inline**: attributo `style` su vari elementi (es. colori, larghezze immagini). Nel foglio esterno compaiono anche selettori di tag, di classe e pseudoclassi sui link. |
| **Impaginazione con `flex` o altre proprietà** | In `seconda_pagina.html` il contenitore `.layout-visione` usa `display: flex` per affiancare il testo (`.contenitore2`) e la colonna parole chiave (`.contenitore3`). Nessun `float` nel progetto; nessuna regola `@media` (layout fisso come da programma svolto). |
| **Commenti** in HTML e CSS (argomento, layout, parte nuova, fonti, riflessione) | Ogni HTML contiene un commento multi-riga in `<head>` con le cinque voci richieste. In cima a `stile.css` c’è un commento di blocco con motivazioni, layout, elemento nuovo, sitografia. |
| **Licenza Creative Commons** nel piede | Testo e link a **CC BY-NC-SA 4.0** (una delle licenze descritte nel manuale, con più condizioni). |
| **Layout** legato al tema e agli **elementi di ottimizzazione** | Tema spirituale/reflexivo: palette blu/indaco/azzurro, testo giustificato nei riquadri, navigazione uguale su tutte le pagine, meta `description` e `keywords` per i motori di ricerca (appendice del manuale sui meta tag). |
| **Elemento di formattazione nuovo**, commentato | **`box-shadow`** su contenitori (`.contenitore`, `.barra-nav`, `.contenitore2`, `.contenitore3`, tabella) e sulle immagini (classe `.img-ombra`). In `stile.css` è indicata la fonte tecnica (MDN). |
| **Contenuti**: immagine, lista, link interno, link esterno | Immagini `igor.webp` / `angeli.webp`; lista in `terza_pagina.html`; link interni nella nav e nel testo; link esterni (es. Wikipedia, Creative Commons) in più pagine. |
| **Bibliografia/sitografia** in commento | Presente nei commenti HTML e nel commento iniziale di `stile.css`. |

---

## 2. Migliorie estetiche e ombreggiatura

- **Intestazione** unificata (titolo con gradiente leggero e angoli arrotondati).
- **Navigazione** con link in linea nella barra centrale.
- **Ombre**: doppio effetto su alcuni contenitori (ombra “morbida” + accento laterale) e ombra più marcata sulle immagini per separarle dallo sfondo.
- **Correzioni** rispetto alla versione precedente: tag `img` chiuso male in home, `text-align` non valido (`center, justify`), errore `margin left`, parentesi graffa finale di troppo in `stile.css`, tag lista scritto in modo errato (`lI`).

Sfondo: resta `immagine_sfondo.jpg` con le proprietà già previste (`repeat`, `size`, `position`, `attachment`); se il file non c’è nella cartella, si vede comunque il colore di fondo impostato in `#sfondo`.

Per la **consegna del progetto** (come da manuale): oltre ai file del sito, prepara la cartella con immagini e video usati, il video di presentazione delle pagine e il file Word con il link di hosting, secondo le istruzioni del docente.

---

## 3. Riferimenti al manuale (punti principali)

- **Punto 3**: consegne del progetto sito (pagine, CSS, nav + pseudoclassi, footer, impaginazione con flex, commenti, CC, ottimizzazione, elemento nuovo, contenuti, sitografia).
- **Punto 1** (metodi di impaginazione nel manuale): nel progetto si usa **Flexbox** per affiancare contenuti; il manuale cita anche `float` e `Grid` come alternative teoriche.
- **Punto 2**: criteri di ottimizzazione (chiarezza, navigazione, colori, parole chiave con `mark` in home).
- **Appendice**: `DOCTYPE html`, meta `keywords` / `description`, HTML5; tag `mark` in `index.html`; tag semantici `<nav>` e `<footer>` per barra di navigazione e piede del sito.

---

*Documento per accompagnare il codice del progetto scolastico.*
