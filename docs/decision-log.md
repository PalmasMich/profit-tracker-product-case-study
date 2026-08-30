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
