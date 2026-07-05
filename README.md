Ecco una versione del file README.md riscritta specificamente per una repository GitHub, con un tono tecnico, pulito e privo di emoji.

Estrattore Casuale per Istituti Scolastici
Applicazione web client-side progettata per l'estrazione casuale di numeri e nomi. Il progetto è pensato per l'utilizzo in contesti didattici e scolastici, offrendo un'interfaccia ad alta leggibilità basata sui font e sulle linee guida della pubblica amministrazione italiana.

Caratteristiche
Estrazione Numerica: Generazione di valori casuali all'interno di un range definito dall'utente (Min/Max) con specifica della quantità di elementi da estrarre contemporaneamente.

Estrazione Nomi: Input testuale multilinea con parsing automatico (un nome per riga) e contatore in tempo reale degli elementi validi inseriti.

Algoritmo di Non Ripetizione: Gestione dello stato degli elementi estratti tramite strutture dati Set per garantire l'esclusione di duplicati nelle estrazioni successive. Gli elementi temporaneamente esclusi vengono mostrati in una sezione di riepilogo dedicata.

Persistenza della Cronologia: Memorizzazione locale delle ultime 15 estrazioni tramite localStorage. Ogni voce registra la modalità, i valori estratti, la data e l'ora dell'operazione.

Layout Responsivo: Interfaccia ottimizzata per la visualizzazione desktop e mobile (media queries per breakpoint a 900px e 640px).

Tecnologie utilizzate
Il progetto è sviluppato in modalità standalone e non richiede dipendenze o package manager per l'esecuzione:

HTML5: Struttura semantica dei componenti.

CSS3: Layout gestito tramite CSS Grid e Flexbox. Utilizzo di Custom Properties per la gestione della palette cromatica.

Vanilla JavaScript (ES6+): Logica di estrazione basata su Math.random(), manipolazione del DOM e gestione dello storage locale.

Risorse Esterne: Google Fonts (Titillium Web) e Material Icons Round.

Installazione e Utilizzo
Trattandosi di un'applicazione esclusivamente client-side, non è necessaria alcuna fase di compilazione o configurazione del server.

Clonare la repository o scaricare il file index.html.

Aprire il file index.html in un qualsiasi browser web moderno.

Bash
git clone https://github.com/tuo-username/nome-repository.git
cd nome-repository
# Aprire il file index.html nel browser
Struttura del Progetto
Il codice è interamente contenuto in un unico file per facilitarne la portabilità:

Stili (CSS): Definiti nel blocco <style> all'interno dell'header. Contengono le definizioni dei token di design e le regole per la responsività.

Interfaccia (HTML): Divisa in una barra superiore istituzionale e un'area principale (main) strutturata su due colonne (Configurazione e Output/Cronologia).

Logica (JS): Posizionata in fondo al documento prima della chiusura del tag </body>. Gestisce gli eventi di interfaccia, la validazione dei dati di input e i cicli di estrazione.
