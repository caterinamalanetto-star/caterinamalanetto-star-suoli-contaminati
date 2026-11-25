# Suoli contaminati in Europa – dataviz Radar QN

Pagine pubblicate su GitHub Pages. Ogni grafico legge il proprio CSV in `data/`: per aggiornarlo basta cambiare il CSV.

- **Siti potenzialmente contaminati stimati, registrati e bonificati nell'Ue**: https://caterinamalanetto-star.github.io/caterinamalanetto-star-suoli-contaminati/registri/
- **Siti registrati per km² di superficie artificiale, per Paese**: https://caterinamalanetto-star.github.io/caterinamalanetto-star-suoli-contaminati/mappa/
- **Siti registrati e pratiche chiuse, per Paese**: https://caterinamalanetto-star.github.io/caterinamalanetto-star-suoli-contaminati/registrare-chiudere/
- **I contaminanti più frequenti nel suolo e nelle acque sotterranee**: https://caterinamalanetto-star.github.io/caterinamalanetto-star-suoli-contaminati/contaminanti/
- **Le scadenze della direttiva europea sul monitoraggio del suolo**: https://caterinamalanetto-star.github.io/caterinamalanetto-star-suoli-contaminati/scadenze/

## Dati e fonti

- `data/registri-aea.csv`: Agenzia europea dell'ambiente, indicatore «Progress in the management of contaminated sites in Europe» (pubblicato il 5 dicembre 2022): 2,8 milioni stimati (proiezione Jrc sui dati 2016), 1,38 milioni registrati, 115.000 bonificati. Nel grafico ogni quadrato vale 5.000 siti; i tre valori sono multipli esatti di 5.000.
- `data/paesi-jrc-2016.csv`: Jrc, «Status of local soil contamination in Europe» (Payá Pérez e Rodríguez Eugenio, 2018), tabella 10 (siti registrati e bonificati, superficie artificiale), tabella 11 (siti registrati per km²) e tabella 12 (quota di siti chiusi = siti in stato 6 + stato 3 sul totale dei registrati, calcolata dal Jrc). Dati nazionali 2016 nella versione Jrc, poi rivista dall'Aea nel 2022 (la versione rivista per Paese non è stata usata).
- `data/contaminanti-jrc-2011.csv`: Jrc, «Progress in the management of contaminated sites in Europe» (van Liedekerke e altri, 2014), figura 9: percentuali scritte nei grafici a torta, dati 2011 (16 Paesi per il suolo, 12 per le acque sotterranee).
- `data/scadenze-direttiva.csv`: direttiva (Ue) 2025/2360, GU L del 26 novembre 2025, articoli indicati nel file.
- `data/europa.geojson`: confini Natural Earth 1:50m (pubblico dominio), ritagliati sull'Europa e semplificati.

## Snippet per il CMS

Vedi `index.html`: per ogni dataviz c'è l'iframe con lo script inline. Se ci sono più dataviz nello stesso articolo, lo script può restare in ognuna (il controllo `__radarQNv2` evita doppioni).
