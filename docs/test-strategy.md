# Strategia di test

## Obiettivo

Verificare che dati, stati e risultati rimangano coerenti lungo l'intero ciclo di vita dell'operazione.

## Livelli di verifica funzionale

### 1. Validazione dei campi

- obbligatorietà;
- formati monetari e date;
- valori nulli, zero e negativi;
- combinazioni incompatibili.

### 2. Transizioni di stato

- percorsi consentiti;
- transizioni bloccate;
- riapertura di un elemento concluso;
- annullamento e ripristino.

### 3. Calcoli e competenza

- risultato per tipologia;
- arrotondamenti;
- mese di competenza;
- modifica retroattiva;
- aggregazione mensile.

### 4. Riconciliazione

- deposito confermato e in attesa;
- prelievo parziale;
- rettifica manuale;
- saldo iniziale importato;
- differenza tra saldo atteso e dichiarato.

### 5. Esperienza mobile

- completamento dei flussi con una mano;
- tastiera numerica appropriata;
- assenza di scroll orizzontale;
- chiarezza degli errori;
- persistenza delle bozze.

## Scenari prioritari

| ID | Scenario | Risultato atteso |
| --- | --- | --- |
| TS-01 | Creazione operazione completa | stato coerente e risultato calcolabile |
| TS-02 | Salvataggio incompleto | bozza esclusa dai consolidati |
| TS-03 | Chiusura senza riconciliazione | stato “Da verificare” |
| TS-04 | Modifica di un importo concluso | avviso e ricalcolo controllato |
| TS-05 | Movimento in attesa | saldo disponibile non alterato definitivamente |
| TS-06 | Promozione scaduta | attività evidenziata come non completata |
| TS-07 | Import duplicato | record duplicati intercettati o segnalati |

## Rischi principali

- doppio conteggio;
- attribuzione al mese errato;
- confusione tra saldo e profitto;
- perdita di precisione negli arrotondamenti;
- modifiche retroattive non tracciate;
- stato visivo non coerente con quello funzionale.

## Exit criteria dell'MVP

- tutti gli scenari prioritari superati;
- nessuna anomalia critica sui consolidati;
- differenze di saldo spiegabili;
- flussi principali completabili da smartphone;
- regressione sui casi già consolidati.
