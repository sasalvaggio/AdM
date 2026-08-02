# AdM — schede e statistiche Arcieri del Mare

`index.html` è l'applicazione completa: codice, grafica e dati in un file solo, senza
dipendenze esterne e senza chiamate di rete. Viene generata da
`Archery_Expert/build_webapp.py` a partire dall'archivio `DB_gare/db.json`.

**Non modificare `index.html` a mano.** Ogni aggiornamento dell'archivio lo riscrive.
Il ciclo è:

```
cd Archery_Expert
./aggiorna.sh                 # rilegge i PDF nuovi e rigenera tutto
cd webApp/AdM
git add index.html && git commit -m "dati al $(date +%F)" && git push
```

## Indirizzo pubblicato

Impostazioni del repository → Pages → Source: *Deploy from a branch* → `main` / `root`.
L'indirizzo diventa `https://sasalvaggio.github.io/AdM/`.

## Nota sui dati

Sono classifiche federali FITARCO, già pubbliche nei tabulati di gara. Contengono nomi di
atleti minorenni. Il file dichiara `noindex` e il repository ha un `robots.txt` che chiede
ai motori di ricerca di non indicizzare: la pagina resta raggiungibile da chi ha
l'indirizzo, ma non compare nelle ricerche per nome.
