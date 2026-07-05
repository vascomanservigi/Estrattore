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

<details>
<summary><b>Visualizza Schema Logico e Stack Tecnologico</b></summary>

   [ Client Browser ]
           │
   ┌───────┴───────┐
   ▼               ▼
┌─────────────┐ ┌─────────────┐
│  DOM Engine │ │ LocalStorage│ (Cronologia fino a 15 record)
└──────┬──────┘ └─────────────┘
▼
┌─────────────┐
│ Set State   │ (Algoritmo Anti-Ripetizione)
└─────────────┘


| Layer | Stack Tecnologico | Ruolo nel Sistema |
| :--- | :--- | :--- |
| **Interfaccia** | HTML5 Semantico | Definizione strutturale dei pannelli di controllo e di output. |
| **Stile** | CSS3 (Grid & Flexbox) | Design responsivo con architettura a token cromatici (Custom Properties). |
| **Computazione** | JavaScript ES6+ | Gestione degli eventi del DOM, logica `Math.random()` e mutazione di stato. |
| **Asset** | Google CDN | Integrazione del font *Titillium Web* e del set iconografico *Material Icons*. |

</details>

---

## Requisiti e Deployment

<details>
<summary><b>Mostra Guida all'Installazione e Uso Rapido</b></summary>

### Avvio Rapido
L'assenza di un backend proprietario rende l'applicazione immediatamente eseguibile in qualsiasi ambiente sandbox o browser moderno.

1. Clonare localmente la risorsa:
   ```bash
   git clone [https://github.com/tuo-username/nome-repository.git](https://github.com/tuo-username/nome-repository.git)
