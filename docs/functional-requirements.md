# Requisiti funzionali

## Epic 1 — Gestire un'operazione

### FR-01 — Creazione

L'utente deve poter creare un'operazione specificando almeno tipologia, data, operatore e importi necessari al calcolo.

**Criteri di accettazione**

- i campi obbligatori sono evidenziati;
- un'operazione incompleta può essere salvata come bozza;
- una bozza non contribuisce ai risultati consolidati;
- gli importi non possono essere negativi, salvo una rettifica esplicita.

### FR-02 — Stato

L'utente deve poter distinguere tra bozza, pianificata, aperta, da verificare, conclusa e annullata.

### FR-03 — Chiusura

Alla chiusura, il sistema deve registrare esito, risultato, data di competenza ed eventuali note di riconciliazione.

## Epic 2 — Gestire promozioni e attività

### FR-04 — Promozione

L'utente deve poter associare una promozione a una o più operazioni e definirne stato, scadenza e attività residue.

### FR-05 — To-do

Il sistema deve mostrare separatamente attività scadute, in scadenza e prive di data.

## Epic 3 — Gestire saldi e movimenti

### FR-06 — Conti

L'utente deve poter registrare più conti associati allo stesso operatore, mantenendo separata l'anagrafica dell'operatore dal conto effettivamente utilizzato.

### FR-07 — Movimenti

Ogni deposito, prelievo o rettifica deve registrare origine, destinazione, data, importo e stato.

### FR-08 — Riconciliazione

Il sistema deve rendere confrontabili saldo registrato, movimenti e saldo dichiarato dall'utente, evidenziando eventuali scostamenti.

## Epic 4 — Consultare risultati

### FR-09 — Dashboard

La dashboard deve mostrare almeno risultato del mese, capitale complessivo, promozioni aperte ed elementi da rendicontare.

### FR-10 — Filtri

L'utente deve poter filtrare operazioni e risultati almeno per periodo, tipologia, operatore e stato.

## Requisiti trasversali

- esperienza mobile-first;
- coerenza dei formati monetari;
- conferma per modifiche che alterano risultati già consolidati;
- distinzione visiva tra dati manuali e calcolati;
- messaggi di errore comprensibili e orientati alla correzione.
