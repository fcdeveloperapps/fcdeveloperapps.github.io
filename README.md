# fcdeveloperapps.github.io

Sito per la condivisione delle app di fcdeveloperapps (pubblicato con GitHub Pages).

- `index.html` – vetrina con l'elenco delle app
- `venezia/` – app "Venezia: Monumenti & altro" (`com.monumenti.venezia`)
  - `venezia/index.html` – rimanda a Google Play
  - `venezia/i/index.html` – pagina dei link condivisi dall'app (`/venezia/i/?d=...`): mostra l'itinerario e i
    pulsanti "Apri nell'app" e "Scarica da Google Play". La codifica di `d` è la stessa di `src/condivisione.js`
    nel repository dell'app.
- `.well-known/assetlinks.json` – (da aggiungere) dichiara a Android che i link `/venezia/...` appartengono
  all'app, così si aprono direttamente nell'app senza passare dal browser. Serve l'impronta SHA-256 del
  certificato di firma dell'app (Google Play Console → Configurazione → Integrità dell'app → Firma dell'app).
- `.nojekyll` – serve perché GitHub Pages pubblichi anche la cartella `.well-known`.
