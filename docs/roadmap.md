# Roadmap di prodotto

## Principio

L'evoluzione procede dalla qualità del dato verso l'automazione. Ogni fase dipende dalla stabilità di quella precedente.

## Fase 1 — Profit Tracker

**Obiettivo:** creare la fonte dati unica.

- tracking di singole, multiple e casino;
- promozioni, memo e scadenze;
- saldi, movimenti e riconciliazioni;
- import iniziale;
- dashboard e report mensili.

## Fase 2 — Ricerca quote

**Obiettivo:** ridurre la ricerca manuale delle opportunità.

- oddsmatcher on demand;
- confronto delle opportunità;
- filtri per mercato e tipologia;
- controllo del consumo delle fonti esterne.

## Fase 3 — Flussi avanzati

**Obiettivo:** collegare ricerca, configurazione e tracking.

- generazione assistita di singole e multiple;
- flussi punta-banca e punta-punta;
- gestione del lock delle bancate;
- sincronizzazione con il Profit Tracker;
- refresh controllato della sessione.

## Fase 4 — Multipla progressiva

**Obiettivo:** gestire end-to-end un processo composto da più eventi e decisioni successive.

- configurazione della progressione;
- monitoraggio di ogni step;
- ricalcolo delle azioni successive;
- gestione di interruzioni ed eccezioni;
- tracciamento unitario del risultato finale.

## Dipendenze

```mermaid
flowchart TD
    A["Modello dati stabile"] --> B["Tracking affidabile"]
    B --> C["Quote esterne"]
    C --> D["Generazione assistita"]
    D --> E["Multipla progressiva"]
```

## Criterio di avanzamento

Una fase può essere considerata pronta quando i flussi principali sono verificati, le eccezioni critiche sono gestite e il risultato rimane riconciliabile.
