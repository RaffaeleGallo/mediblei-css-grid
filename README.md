# Mediblei — esercizio CSS Grid

Esercizio didattico in HTML e CSS, ispirato al layout BoolTok della consegna e al profilo Instagram di Mediblei. Nessuna dipendenza: aprire `index.html` nel browser.

## Passo 1: struttura iniziale

- `index.html`: documento in italiano, viewport, CSS collegato, placeholder del profilo e sezione Post.
- `css/style.css`: reset di base, contenitore centrato e stile del placeholder.
- `.gitignore`: esclude i file di servizio di macOS.

Controllo nel browser: il titolo Mediblei deve apparire dentro un blocco grigio, seguito da Post. Riducendo la finestra il contenitore deve mantenere spazio ai lati.

Commit suggerito: `chore: imposta struttura HTML e CSS iniziale`

## Passo 2: la griglia

Il contenitore `.posts-grid` contiene sei `.post`, che sono i suoi figli diretti.

- `display: grid` attiva Grid sul contenitore.
- `grid-template-columns: repeat(3, 1fr)` crea tre colonne della stessa larghezza, dividendo lo spazio disponibile dopo il gap.
- `gap: 8px` crea spazio tra le celle, sia in orizzontale sia in verticale.
- Non serve definire le righe: Grid crea automaticamente la seconda riga per i post 4, 5 e 6.
- `min-height: 180px` rende visibili i riquadri anche senza immagini.

Controllo nel browser: sotto Post devono comparire 1, 2, 3 nella prima riga e 4, 5, 6 nella seconda. Il placeholder del profilo resta in alto.

Prova nel browser: cambia temporaneamente `repeat(3, 1fr)` in `repeat(2, 1fr)` e osserva le tre righe; poi ripristina tre colonne prima del commit.

Commit suggerito: `feat: aggiunge griglia a tre colonne con sei post`

## Passo 3: immagini nella griglia

I numeri sono sostituiti da sei immagini scaricate dal profilo Instagram Mediblei e salvate nella cartella `img/`. La pagina può mostrarle anche senza connessione.

- `.post` resta il figlio diretto della griglia; l'immagine è contenuta al suo interno.
- `aspect-ratio: 4 / 5` determina l'altezza del riquadro in base alla sua larghezza.
- `min-width: 0` permette alla cella di restringersi anche quando contiene un'immagine grande.
- `width: 100%` e `height: 100%` fanno occupare all'immagine tutto il riquadro.
- `object-fit: cover` conserva le proporzioni, ritagliando l'eccesso quando necessario.
- `display: block` elimina lo spazio di base tipico delle immagini inline.
- Il padding dei riquadri numerati viene rimosso per portare la foto fino ai bordi.

Controllo: sei immagini in due righe da tre, senza deformazioni. Prova temporaneamente `aspect-ratio: 1 / 1` per vedere il ritaglio, poi ripristina `4 / 5`. Con `object-fit: contain` vedresti invece tutta l'immagine, ma potrebbero restare spazi vuoti.

Le locandine sono contenuti dei post originali usati nell'esercizio, non annunci di nuovi eventi. Per leggere eventuali parti ritagliate, aprire il file originale in `img/`.

### Fonti delle immagini

- `incipit.jpg`: https://www.instagram.com/mib_mediblei/p/DgIb8-4CPGh/
- `saluti-dallo-spazio.jpg`: https://www.instagram.com/mib_mediblei/p/DdrI8IBiLjO/
- `laboratorio-nina.jpg`: https://www.instagram.com/mib_mediblei/p/DdJmw8moPI6/
- `cinematti.jpg`: https://www.instagram.com/mib_mediblei/p/Dcbg9ebILu9/
- `capolettera-angelo-ruta.jpg`: https://www.instagram.com/mib_mediblei/p/Db7-HGUoNQW/
- `tre-soste.jpg`: https://www.instagram.com/mib_mediblei/p/DbqzYA0IHc7/

Commit suggerito: `feat: inserisce immagini Mediblei nella griglia`

## Percorso concordato

1. Struttura iniziale e placeholder superiore.
2. Sei riquadri numerati in tre colonne con `display: grid`, `grid-template-columns` e `gap`.
3. Foto locali dei post e `object-fit: cover`.
4. Profilo: logo fornito, nome, biografia e collegamento Instagram.
5. Colori, spaziature e adattamento agli schermi piccoli.
6. Bonus separato con `grid-column` / `grid-row` e `span`.

Una fase per volta: i commit vengono eseguiti dallo studente.
