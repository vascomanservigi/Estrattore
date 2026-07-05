# Estrattore Casuale per Istituti Scolastici

Applicazione web client-side progettata per l'estrazione casuale di numeri e nomi. Il progetto è pensato per l'utilizzo in contesti didattici e scolastici, offrendo un'interfaccia ad alta leggibilità basata sui font e sulle linee guida della pubblica amministrazione italiana.

## Caratteristiche

* **Estrazione Numerica**: Generazione di valori casuali all'interno di un range definito dall'utente (Min/Max) con specifica della quantità di elementi da estrarre contemporaneamente.
* **Estrazione Nomi**: Input testuale multilinea con parsing automatico (un nome per riga) e contatore in tempo reale degli elementi validi inseriti.
* **Algoritmo di Non Ripetizione**: Gestione dello stato degli elementi estratti tramite strutture dati `Set` per garantire l'esclusione di duplicati nelle estrazioni successive. Gli elementi temporaneamente esclusi vengono mostrati in una sezione di riepilogo dedicata.
* **Persistenza della Cronologia**: Memorizzazione locale delle ultime 15 estrazioni tramite `localStorage`. Ogni voce registra la modalità, i valori estratti, la data e l'ora dell'operazione.
* **Layout Responsivo**: Interfaccia ottimizzata per la visualizzazione desktop e mobile (media queries per breakpoint a 900px e 640px).

## Specifiche Tecniche

Il progetto è sviluppato in modalità standalone e non richiede dipendenze o package manager per l'esecuzione:

| Componente | Tecnologia | Utilizzo principale |
| :--- | :--- | :--- |
| **Struttura** | HTML5 | Componenti semantici dell'interfaccia |
| **Stile** | CSS3 | Layout Grid/Flexbox e Custom Properties (variabili) |
| **Logica** | JS (ES6+) | Manipolazione del DOM, `Math.random()` e `localStorage` |
| **Risorse** | Web Fonts | Google Fonts (Titillium Web) e Material Icons Round |

## Installazione e Utilizzo

Trattandosi di un'applicazione esclusivamente client-side, non è necessaria alcuna fase di compilazione o configurazione del server.

1. Clonare la repository o scaricare il file `index.html`.
2. Aprire il file `index.html` in un qualsiasi browser web moderno.

```bash
git clone [https://github.com/tuo-username/nome-repository.git](https://github.com/tuo-username/nome-repository.git)
cd nome-repository
