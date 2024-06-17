Milestone 0:
Progettare la struttura della logica della nostra applicazione attraverso l’uso di: 
global state, mista, oppure esclusivamente con props ed $emit sulla linea degli esercizi svolti nei giorni precedenti.

Milestone 1:
Creare un layout base con una searchbar (una input e un button) in cui possiamo scrivere completamente o parzialmente il nome di un film. Possiamo, cliccando il  bottone, cercare sull’API tutti i film che contengono ciò che ha scritto l’utente.
Vogliamo dopo la risposta dell’API visualizzare a schermo i seguenti valori per ogni film trovato: 
- Titolo
- Titolo Originale
- Lingua
- Voto

1) creo un collegamento con emit dal bottone search a header;

2) in store mi creo una variante che mi colleghi l'input text all'header;

3) faccio un chiamata get nella componente AppMain in cui avrò la ricerca film;

