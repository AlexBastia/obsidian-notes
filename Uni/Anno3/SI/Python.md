### Referential transparency
Il risultato non cambia cambiando l'ordine delle operazioni. Il flusso non conta (visto nei linguaggi funzionali come Haskell). Si ha che le variabili non cambiano valore, evitando i side effect. Python eredita sta roba con le **entita' immutabili** (come le stringhe costanti, ma la variabile puo' puntare ad altre cose). La cosa strana e' che le liste sono mutabili.

Sta roba aiuta il parallelismo, dato che possiamo eseguire piu' linee di codice alla volta, aspettando di volta in volta i valori necessari da cui dipende. 