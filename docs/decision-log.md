# Decision log

## ADR-001 — Repository pubblico separato

**Decisione:** creare un repository documentale separato dal codice dell'applicazione.

**Motivazione:** mostrare competenze di analisi funzionale senza esporre sorgenti, configurazioni, ambienti o dati.

## ADR-002 — Mobile first

**Decisione:** progettare i flussi principali prima per smartphone.

**Alternativa:** adattare successivamente un'esperienza desktop.

**Motivazione:** il limite principale dei fogli Excel era l'utilizzo in mobilità.

## ADR-003 — Separare operatore e conto

**Decisione:** distinguere l'anagrafica dell'operatore dal conto realmente utilizzato.

**Motivazione:** un utente può avere più conti o configurazioni riconducibili allo stesso operatore.

## ADR-004 — Separare risultato e movimenti

**Decisione:** non usare depositi e prelievi per rappresentare il profitto.

**Motivazione:** i flussi finanziari modificano la distribuzione del capitale, non il risultato economico dell'operazione.

## ADR-005 — Esiti inizialmente manuali

**Decisione:** mantenere la conferma manuale degli esiti nell'MVP.

**Alternativa:** integrazione immediata con fonti esterne.

**Motivazione:** validare prima modello, stati e riconciliazione riduce dipendenze e complessità.

## ADR-006 — Automazione progressiva

**Decisione:** introdurre oddsmatcher e generazione dei flussi solo dopo la stabilizzazione del tracker.

**Motivazione:** automatizzare un processo non ancora stabile amplifica errori e rende più difficile verificarli.

## ADR-007 — Nessuna esposizione del sito reale

**Decisione:** il case study pubblico non conterrà collegamenti all'applicazione navigabile.

**Motivazione:** il progetto rimane personale; la finalità pubblica è mostrare il processo di analisi, non offrire un servizio.

## ADR-008 — Strategia per le API quote

**Esigenza:** alimentare in una fase successiva oddsmatcher e flussi assistiti con quote provenienti da fonti esterne.

**Valutazione:** sono stati analizzati provider specializzati considerando copertura di bookmaker e mercati, frequenza di aggiornamento, disponibilità di mercati complessi, limiti di chiamata, costo e scalabilità rispetto al volume d'uso previsto.

**Provider valutato:** OpticOdds è stato incluso nel confronto come possibile fonte dati. La valutazione ha evidenziato che un piano nell'ordine di 79 €/mese con circa 500 richieste può risultare sovradimensionato nel costo e contemporaneamente restrittivo nei volumi per un progetto personale utilizzato inizialmente da un numero molto limitato di utenti.

**Decisione:** non vincolare il dominio del Profit Tracker a uno specifico provider. L'integrazione sarà progettata attraverso un livello di astrazione sostituibile e il provider della Fase 2 verrà selezionato sulla base del miglior rapporto tra copertura, qualità del dato, limiti di consumo e costo effettivo.

**Conseguenza:** la fonte quote potrà essere sostituita senza riprogettare il modello funzionale del prodotto e senza introdurre vendor lock-in prematuro.
