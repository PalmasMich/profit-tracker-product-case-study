# Decision log

## ADR-001 — Separazione tra documentazione e applicazione

**Decisione:** mantenere la documentazione di prodotto in un repository separato dal codice dell'applicazione.

**Motivazione:** applicare una separazione netta delle responsabilità e impedire che sorgenti, configurazioni, ambienti, credenziali o dati reali siano inclusi nel perimetro documentale.

**Conseguenza:** il repository documentale può evolvere indipendentemente dall'applicazione e contiene soltanto artefatti esplicitamente selezionati.

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

## ADR-007 — Applicazione non esposta

**Decisione:** la documentazione non contiene collegamenti all'applicazione navigabile.

**Motivazione:** limitare il perimetro accessibile, proteggere dati e configurazioni operative ed evitare che un ambiente personale venga interpretato o utilizzato come servizio disponibile.

**Conseguenza:** esempi e schermate utilizzano esclusivamente dati di test e non consentono di accedere all'ambiente reale.

## ADR-008 — Strategia per le API quote

**Esigenza:** alimentare in una fase successiva oddsmatcher e flussi assistiti con quote provenienti da fonti esterne.

**Valutazione:** sono stati analizzati provider specializzati considerando copertura di bookmaker e mercati, frequenza di aggiornamento, disponibilità di mercati complessi, limiti di chiamata, costo e scalabilità rispetto al volume d'uso previsto.

**Provider valutato:** OpticOdds è stato incluso nel confronto come possibile fonte dati. La valutazione ha evidenziato che un piano nell'ordine di 79 €/mese con circa 500 richieste può risultare sovradimensionato nel costo e contemporaneamente restrittivo nei volumi per un progetto personale utilizzato inizialmente da un numero molto limitato di utenti.

**Decisione:** non vincolare il dominio del Profit Tracker a uno specifico provider. L'integrazione sarà progettata attraverso un livello di astrazione sostituibile e il provider della Fase 2 verrà selezionato sulla base del miglior rapporto tra copertura, qualità del dato, limiti di consumo e costo effettivo.

**Conseguenza:** la fonte quote potrà essere sostituita senza riprogettare il modello funzionale del prodotto e senza introdurre vendor lock-in prematuro.


## ADR-009 — Validazione con utenti diversi dall'analista

**Contesto:** nelle prime fasi del progetto la stessa persona ricopre il ruolo di utilizzatore e analista. Questo accelera la comprensione del bisogno, ma aumenta il rischio di confermare le proprie assunzioni.

**Decisione:** coinvolgere un piccolo gruppo di utenti che conoscono il processo, raccogliere feedback strutturati ed eseguire una fase di User Acceptance Testing su scenari reali.

**Conseguenza:** l'MVP non verrà considerato validato sulla sola auto-valutazione. Anomalie, difficoltà d'uso e bisogni non coperti emersi durante l'UAT saranno tracciati e prioritizzati.
