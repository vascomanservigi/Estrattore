# Estrattore Casuale Multi-Target

Applicazione web client-side ad alte prestazioni ingegnerizzata per la generazione di campioni casuali da set di dati numerici o testuali. Sviluppato per supportare la didattica, ottimizzare le sessioni di verifica e agevolare la gestione delle dinamiche di gruppo all'interno dell'istituto, il software coniuga un'interfaccia utente pulita a una logica computazionale snella e priva di attriti.

---

## Architettura Funzionale

### Generazione Numerica Vincolata
Il motore di calcolo permette la definizione di un intervallo chiuso [Min, Max] all'interno del quale estrarre subset di dati di cardinalità variabile. Un sistema di validazione nativo impedisce l'esecuzione di cicli logici errati, come l'impostazione di un valore minimo superiore al limite massimo.

### Parsing Testuale Dinamico
L'input per la gestione dei nominativi adotta un modello di separazione basato su interruzione di riga. Il sistema esegue un filtraggio automatico degli spazi vuoti e aggiorna in tempo reale un contatore di elementi attivi, ottimizzando l'esperienza di inserimento di elenchi strutturati (es. registri di classe).

### Controllo dello Stato e Anti-Ripetizione
Attraverso l'implementazione dell'oggetto nativo `Set` di JavaScript, l'applicazione garantisce l'esclusione matematica dei duplicati nelle estrazioni sequenziali. Gli elementi estratti vengono rimossi temporaneamente dal pool principale e mappati graficamente come componenti atomici nell'area dei valori esclusi.

### Storage Locale Persistente
Il modulo di cronologia implementa una pipeline di memorizzazione basata su `localStorage`. Vengono mantenuti in persistenza gli ultimi 15 record di estrazione, ciascuno strutturato con metadati precisi: vettore dei risultati, modalità di esecuzione e timestamp atomico (data e ora dell'evento).

---

## Specifiche Tecniche

L'applicazione è strutturata secondo il paradigma **Zero-Dependency Single File**. Non richiede fasi di compilazione, interpreti lato server o l'installazione di pacchetti software di terze parti.
