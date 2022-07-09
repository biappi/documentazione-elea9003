```{sectnum}
---
start: 5
---
```

# Le unita' a nastro magnetico


## Governo delle unita' a nastro

E' questo l'organo mediante il quale si effettua il collegamento tra unita' a
nastro e calcolatore, oppure fra due unita' a nastro.

Le unita' collegabili al GUN sono al massimo 20.

Le caratteristiche funzionali del GUN permettono di eseguire la verifica delle
registrazioni contemporaneamente alla registrazione stessa e di rilevare e
segnalare all' unita' centrale eventuali errori di lettura o di registrazione.
Il GUN puo' ordinare il riavvolgimento contemporaneo delle bobine di un numero
qualsiasi di unita' a nastro, e durante il riavvolgimento operare su una unita'
in lettura ed una in registrazione.

Altre e piu' complesse operazioni possono essere eseguite dal GUN. Esso puo'
disporre lo svolgimento di un nastro magnetico, nell' uno o nell'altro senso,
fino a far passare un numero di blocchi indicato da un'istruzione di programma;
puo' far trascrivere un numero di blocchi indicato da una istruzione, da un
nastro in lettura a un nastro in registrazione.

Puo' inoltre ordinare lo svolgimento di un nastro magnetico fino ad arrivare al
blocco che contiene una parola di lunghezza variabile previamente trasferita in
uno speciale registro. Questa operazione, detta di ricerca, puo' essere
effettuata anche trascrivendo contemporaneamente i blocchi che non contengano
la parola cercata ad un nastro in registrazione.

Essa rende possibile la consultazione ed aggiornamento di un nastro archivio a
grande velocita' e senza che sia impegnato il calcolatore.


## Nastro magnetico

Il nastro magnetico e una banda di materia plastica (mylar) ricoperto su una
faccia da ossido di ferro magnetizzabile. si puo' pensare che la superficie del
nastro sia costituita da numerose piccole aree che possono essere magnetizzate
o no. Lo stato magnetico di ciascuna di queste aree permette dunque la
rappresentazione materiale di un bit.

Degli 8 bit che vengono utilizzati per ciascun carattere, uno serve per il
controllo dell' esattezza della registrazione e uno per la temporizzazione.

Ogni carattere numerico, alfabetico o speciale e' quindi rappresentato dalle
combinazioni dei 6 bit restanti secondo il codice impiegato dall'Elea 9003.

I caratteri sono registrati uno di seguito all'altro, in gruppi di capacita'
variabile, ma normalmente dell'ordine di diverse centinaia o alcune migliaia di
caratteri: tali gruppi, detti blocchi, sono separati sul nastro da un breve
spazio non utilizzato, detto interblocco. La lunghezza dell'interblocco e di 1
pollice.

La larghezza del nastro e' di 1,27 cm, la lunghezza di una bobina e di circa
1100 metri, La densita' di registrazione e' di ~120 caratteri per centimetro
(corrispondente a 300 caratteri per pollice).

Conseguentemente ogni bobina di nastro puo' contenere fino a 12.960.000 caratteri.

    quio
    @MUC

Il nastro viene svolto nell' uno e nell' altro senso, alla velocita' di 3,81
mt. al secondo; in un secondo vengono letti (o registrati) 45.000 caratteri. Il
tempo di lettura di una intera bobina (12.960.000 caratteri) e quindi
inferiore ai 5 minuti.

    ALCUNE UNITÀ' A NASTRO MAGNETICO COLLEGATE FR - 400 ._

Per conoscere il numero N di caratteri registrabili
in una bobina di nastro, con blocchi di n caratteri
in media, si deve applicare la formula seguente:

    12.960.000• n
    N=

Cosi: ad esempio se i blocchi contengono 1000 caratteri, il numero totale di caratteri registrati
ra' di 9.969.230

Il numero b dei blocchi registrabili su una bobina
dato ovviamente dalla formula analoga

    12.960.000
    n =
    n + 300

Alle due estremita' della bobina il nastro e' metallizzato per una lunghezza
opportuna, per avvertire l' unita' che lo governa della sua prossima fine.

Le unita' a nastro magnetico dell' Elea 9003 sono dotate di due testine, una
per la lettura e una per la registrazione.

Esse possono leggere il nastro sia quando questo scorre nel senso detto
convenzionalmente "avanti" sia quando scorre nel senso opposto, detto
"indietro"; la verifica della corretta lettura e' effettuata per mezzo del bit
di disparita. La registrazione e' invece verificata rileggendo con la testina
di lettura, che si trova a valle di quella di registrazione quando il nastro
scorre in avanti, quanto appena registrato, e confrontandolo con l'
informazione che doveva essere registrata. Come conseguenza, la registrazione
puo' avvenire solo nel senso "avanti".  Quando l' unita' riceve l'ordine di
iniziare la lettura o la registrazione di un blocco impiega un tempo di 5,7
millisecondi circa per avviare il nastro; terminata la lettura impiega 4,1
millisecondi per arrestare il nastro. L'interblocco di 1 pollice di lunghezza
corrisponde appunto alla lunghezza di nastro svolta durante questi tempi di
decelerazione ed accelerazione.

Le unita' a nastro sono capaci di riavvolgere la bobina completamente, senza
intervento dell' elaboratore, che si limita ad impartire l'ordine relativo.

I caratteri che distinguono le diverse unita' a nastro collegabili al GUN, in
numero di 20, sono i seguenti

    1, 2, 3, 4, 5, 6, 7, 8, 9, ~
    o, A, B, C, D, E, F, G, H, I,


## Organizzazione delle informazioni su nastro magnetico

Il raggruppamento dei caratteri in blocchi, dovuto alla necessita' di
trasferire un numero limitato di caratteri dal nastro magnetico alla memoria
principale dell' elaboratore, esige d' altra parte - almeno se si vuole che la
lunghezza del blocco sia variabile - uno speciale carattere che marchi l'inizio
e la fine di ogni blocco. Tale carattere e', per l' Elea 9003, il carattere d:
ogni blocco deve iniziare terminare con d

Esiste d'altra parte, in molti casi, la convenienza di suddividere in sequenze,
comprendenti uno o piu' blocchi, l'intera informazione registrata su nastro: a
questo scopo si fara terminare l'ultimo blocco

della sequenza, ed iniziare il primo, con il carattere punto interrogativo" (?)
invece che con il carattere d.

Per marcare la fine della informazione registrata su nastro magnetico viene
invece utilizzato il carattere "moltiplicato per" (#).

Per suddividere un blocco in parti di lunghezza determinata, ai fini di una
registrazione o lettura su indirizzi non consecutivi di memoria, viene usato il
carattere 0.

