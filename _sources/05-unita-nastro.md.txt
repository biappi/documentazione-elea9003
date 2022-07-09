# Le unita' a nastro magnetico

## 5.1. Governo delle unita' a nastro

E' questo l'organo mediante il quale si effettua il
collegamento tra unita' a nastro e calcolatore, op
pure fra due unita' a nastro.
Le unita' collegabili al GUN sono al massimo 20.
Le caratteristiche funzionali del GUN permettono di
eseguire la verifica delle registrazioni contempora
neamente alla registrazione stessa e di rilevare e
segnalare all' unita' centrale eventuali errori di
lettura o di registrazione. Il GUN puo' ordinare il
riavvolgimento contemporaneo delle bobine di un nu-
mero qualsiasi di unita' a nastro, e durante il riav
volgimento operare su una unita' in lettura ed una
in registrazione.
Altre e piu' complesse operazioni possono essere ese
guite dal GUN. Esso puo' disporre lo svolgimento di
un nastro magnetico, nell' uno o nell'altro senso, fi
no a far passare un numero di blocchi indicato da
un'istruzione di programma; puo' far trascrivere un
numero di blocchi indicato da una istruzione, da un
nastro in lettura a un nastro in registrazione.
Puo' inoltre ordinare lo svolgimento di un nastro ma
gnetico fino ad arrivare al blocco che contiene una
parola di lunghezza variabile previamente trasferi-
ta in uno speciale registro. Questa operazione, det
ta di ricerca, puo' essere effettuata anche trascri
vendo contemporaneamente i blocchi che non contengg
no la parola cercata ad un nastro in registrazione.
Essa rende possibile la consultazione ed aggiorna-
mento di un nastro archivio a grande velocita' e sen
za che sia impegnato il calcolatore

## 5.2. Nastro magnetico

Il nastro magnetico e una banda di materia plasti
ca (mylar) ricoperto su una faccia da ossido di fer
ro magnetizzabile. si puo' pensare che la superfi-
cie del nastro sia costituita da numerose piccole
aree che possono essere magnetizzate o no. Lo stato
magnetico di ciascuna di queste aree permette dun-
que la rappresentazione materiale di un bit.
Degli 8 bit che vengono utilizzati per ciascun ca
rattere, uno serve per il controllo dell' esattezza
della registrazione e uno per la temporizzazione.
Ogni carattere numerico, alfabetico o speciale e'
quindi rappresentato dalle combinazioni dei 6 bit
restanti secondo il codice impiegato dall'Elea 9003.
I caratteri sono registrati uno di seguito all'al-
tro, in gruppi di capacita' variabile, ma normalmen
te dell'ordine di diverse centinaia o alcune mi-
gliaia di caratteri: tali gruppi, detti blocchi, so
no separati sul nastro da un breve spazio non uti-
lizzato, detto interblocco. La lunghezza dell' inter
blocco e di 1 pollice.
La larghezza del nastro e' di 1,27 cm, la lunghez
za di una bobina e di circa 1100 metri, La densi-
ta' di registrazione e' di ~120 caratteri per centi
metro (corrispondente a 300 caratteri per pollice).
Conseguentemente ogni bobina di nastro puo' contene
re fino a 12.960.000 caratteri.
quio
@MUC
Il nastro viene svolto nell' uno e nell' altro senso,
alla velocita' di 3, 81 mt. al secondo; in un secon
do vengono letti (o registrati) 45.000 caratteri. Il
tempo di lettura di una intera bobina ( 12. 960.000
caratteri ) e quindi inferiore ai 5 minuti.
ALCUNE UNITÀ' A NASTRO MAGNETICO COLLEGATE FR - 400 ._

Per conoscere il numero N di caratteri registrabili
in una bobina di nastro, con blocchi di n caratteri
in media, si deve applicare la formula seguente :
12.960.000• n
N=
Cosi: ad esempio se i blocchi contengono 1000 carat
teri, il numero totale di caratteri registrati
ra' di 9.969.230
Il numero b dei blocchi registrabili su una bobina
dato ovviamente dalla formula analoga
12.960.000
n =
n + 300
Alle due estremita' della bobina il nastro e' metal-
lizzato per una lunghezza opportuna, per avvertire
1' unita' che lo governa della sua prossima fine.
Le unita' a nastro magnetico dell' Elea 9003 sono do
tate di due testine, una per la lettura e una per la
registrazione.
Esse possono leggere il nastro sia quando questo
scorre nel senso detto convenzionalmente "avanti"
sia quando scorre nel senso opposto, detto
"indie-
tro"; la verifica della corretta lettura e' effettua
ta per mezzo del bit di disparita. La registrazio-
ne e' invece verificata rileggendo con latestina di
lettura, che si trova a valle di quella di registra
zione quando il nastro scorre in avanti, quanto ap-
pena registrato, e confrontandolo con 1' informazio-
ne che doveva essere registrata. Come conseguenza,
la registrazione puo' avvenire solo nel senso "avan
tis
Quando 1' unita' riceve l'ordine di iniziare la let-
tura o la registrazione di un blocco impiega un tem
po di 5,7 millisecondi circa per avviare il nastro;
terminata la lettura impiega 4,1 millisecondi per ar
restare il nastro. L'interblocco di 1 pollice di lun
ghezza corrisponde appunto alla lunghezza di nastro
svolta durante questi tempi di decelerazione ed ac
celerazione.
Le unita' a nastro sono capaci di riavvolgere la bo
bina completamente, senza intervento dell' elaborato
re, che si limita ad impartire l'ordine relativo.
I caratteri che distinguono le diverse unita' a na-
stro collegabili al GUN, in numero di 20, sono i se
guenti
1, 2, 3, 4, 5, 6, 7, 8, 9, ~
o, A, B, C, D, E, F, G, H, I,

## 5.3. Organizzazione delle informazioni su nastro magnetico

Il raggruppamento dei caratteri in blocchi, dovuto
alla necessita' di trasferire un numero limitato di
caratteri dal nastro magnetico alla memoria princi-
pale dell' elaboratore, esige d' altra parte - almeno
se si vuole che la lunghezza del blocco sia variabi
le - uno speciale carattere che marchi l'inizio e la
fine di ogni blocco. Tale carattere e', per 1' Elea
9003, il carattere d: ogni blocco deve iniziare
terminare con d
Esiste d'altra parte, in molti casi, la convenienza
di suddividere in sequenze, comprendenti uno o piu'
blocchi, l'intera informazione registrata su nastro:
a questo scopo si fara terminare l'ultimo blocco
56
della sequenza, ed iniziare il primo, con il carat-
tere punto interrogativo" (?) invece che con il ca
rattere d.
Per marcare la fine della informazione registrata su
nastro magnetico viene invece utilizzato il caratte
re "moltiplicato per (#).
Per suddividere un blocco in parti di lunghezza de-
terminata, ai fini di una registrazione o lettura
su indirizzi non consecutivi di memoria, viene usa-
to il carattere 0
57

