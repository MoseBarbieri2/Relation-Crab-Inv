## 1.1 Descrizione e requisiti
*Idea della funzione del programma, niente design ne' implementazioni*

Il videogioco consiste nel permettere al giocatore di controllare un carro armato per respingere ondate di entità ostili rappresentate da "granchi alieni" (da qui il nome).
Il videogioco è visualizzato in formato 2D, il carro armato è posizionato nella parte bassa dello schermo mentre le entità ostili appaiono dalla parte alta.
L'obiettivo del gioco è quello di respingere i nemici tramite l'arma del veicolo controllato, eliminandoli prima che possano raggiungere alla posizione del carro armato ed evitandone eventuali proiettili da essi sparati.
La struttura del gioco è basata sul genere "rogue-lite", ossia ogni tentativo concluso (con successo o meno) permetterà al giocatore di utilizzare le ricompense ottenute per migliorare il proprio veicolo in modo da essere meglio preparato per il tentativo successivo.
Le partite seguono una struttura di livelli predefinita che si susseguono al compimento di quello precedente.
È prevista la possibilità di localizzazione, in modo da permettere di cambiare la lingua dei testi mostrati.

### Requisiti funzionali
- Il carro armato controllato dal giocatore deve prevedere il movimento sull'asse laterale (sinistra, destra) e la possibilità di "fare fuoco"
- Le entità ostili cercheranno di raggiungere il punto più basso dello schermo, ergo l'asse del giocatore, o di colpire il carro armato con proiettili
- I tentativi potranno essere salvate a punti di salvataggio in modo da poter riprendere a giocare in un secondo momento
- Sarà possibile utilizzare le risorse acquisite per potenziarsi solo tra un tentativo e l'altro, mai durante un tentativo
- La condizione di vittoria per poter passare al livello successivo (ed eventualmente "vincere il gioco") è quella di eliminare tutte le entità ostili in tempo
- La condizione di sconfitta che terminerà la partita è la fine delle "vite" disponibili al giocatore

### Requisiti non funzionali
- Il gioco non dovrà avere grandi requisiti di risorse di sistema, dovrà essere facilmente eseguibile anche su macchine con prestazioni hardware ridotte
- Il gioco richiederà una tastiera per poter essere utilizzato
