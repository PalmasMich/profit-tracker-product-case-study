# User flow

## Flusso principale: registrare e chiudere un'operazione

```mermaid
flowchart TD
    A["Nuova operazione"] --> B["Scelta tipologia"]
    B --> C["Inserimento dati essenziali"]
    C --> D{"Dati completi?"}
    D -- No --> E["Salva bozza"]
    D -- Sì --> F["Verifica riepilogo"]
    F --> G["Operazione aperta"]
    G --> H["Registra esito"]
    H --> I["Calcola risultato"]
    I --> J{"Riconciliata?"}
    J -- No --> K["Da verificare"]
    J -- Sì --> L["Conclusa"]
```

## Flusso: promozione e scadenza

```mermaid
stateDiagram-v2
    [*] --> Pianificata
    Pianificata --> Attiva
    Attiva --> DaCompletare
    DaCompletare --> Completata
    Attiva --> Scaduta
    DaCompletare --> Scaduta
    Completata --> [*]
    Scaduta --> [*]
```

## Flusso: deposito e prelievo

```mermaid
flowchart LR
    A["Conto origine"] --> B["Movimento"]
    B --> C{"Confermato?"}
    C -- No --> D["In attesa"]
    C -- Sì --> E["Aggiorna saldi"]
    E --> F["Riconciliazione"]
```

## Eccezioni da gestire

- operazione salvata senza tutti i dati;
- quota o importo modificati dopo la pianificazione;
- evento rinviato o annullato;
- movimento finanziario ancora in attesa;
- differenza tra saldo atteso e saldo dichiarato;
- promozione scaduta con attività non completate;
- modifica retroattiva che cambia il mese di competenza.
