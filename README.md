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

Milestone 2:
Trasformiamo la stringa statica della lingua in una vera e propria bandiera della nazione corrispondente, gestendo il caso in cui non abbiamo la bandiera della nazione ritornata dall’API (le flag non ci sono in FontAwesome) [per ogni film].

Allarghiamo poi la ricerca anche alle serie tv. Con la stessa azione di ricerca dovremo prendere sia i film che corrispondono alla query, sia le serie tv, stando attenti ad avere alla fine dei valori simili (le serie e i film hanno campi nel JSON di risposta diversi, simili ma non sempre identici)
Qui un esempio di chiamata per le serie tv:
https://api.themoviedb.org/3/search/tv?api_key=e99307154c6dfb0b4750f6603256716d&language=it_IT&query=scrubs


1) aggiunto flags per lingua;

2) creo chiamate get per serie e film;