# Organizzazione della programmazione

## 6.1. Struttura della programmazione

Chiamiamo programma una sequenza di disposizioni o
comandi che eseguiti uno di seguito all'altro, por
tano alla soluzione di un problema secondo la logi
ca particolare dell' elaboratore.
L'impostazione di un programma puo' essere ovvia-
mente diversa secondo le caratteristiche dell'ela-
boratore a cui il programma stesso va indirizzato;
e' indispensabile quindi conoscerne i particolari
requisiti, studiarne a fondo le possibili utilizza
zioni, per riuscire a costruire un programma che
sfrutti al massimo le capacita' della macchina.
Oltre che il numero e la struttura dei comandi che
il sistema Elea 9003 e' in grado di interpretare ed
eseguire, si rende necessario conoscere di esso le
peculiari caratteristiche : la simultaneita' opera
tiva o plurisequenzialita di programma, e lo sfrut
tamento massimo del nastro magnetico come principa
le supporto delle informazioni.
E' sulla traccia di queste nozioni, che il program
matore deve risolvere i problemi che gli
vengonc
sottoposti
La stesura della soluzione prescelta deve pertanto
essere espressa mediante un linguaggio comprensibi
le alla macchina : e' percio richiesta al program
matore la conoscenza dei simboli con cui i comandi
devono essere formulati e le regole a cui essi so-
no soggetti.
L'esprimersi nel modo sopradetto significa espri-
mersi in linguaggio macchina.
59
E' tuttavia opportuno notare che esiste il modo di
evitare al programmatore la fatica che questo mezzo
di comunicazione comporta.
E' stato cioe' creato un linguaggio, chiamato lin-
guaggio simbolico, molto piu vicino a quello da noi
abitualmente usato, e che quindi non richiede lo
sforzo mentale continuo di adattamento alla macchi-
na.
E' evidente pero' che il lavoro di cui viene alleg-
gerito 1' uomo non puo' che essere trasferito all'e-
laboratore che viene dotato in questo caso di unpar
ticolare dispositivo che gli permette la traduzione
di questo nuovo linguaggio nei simboli ad esso intel
ligibili.
Nei capitoli che seguono si trovano illustrate le i
struzioni, i comandi cioe' che si possono impartire
alla macchina, se ne elencano le caratteristiche, ed
infine si espongono le norme relative all'utilizza-
zione dei nastri e dei programmi plurisequenziali

## 6.2. La codificazione delle informazioni

Le informazioni - dati, risultati e istruzioni di
programma - sono rappresentate per mezzo di caratte
ri alfanumerici e speciali, la cui codificazione va
ria secondo il supporto utilizzato per la loro regi
strazione.
Per i seguenti supporti : la memoria principale e i
registri del calcolatore, i nastri ed i tamburi ma-
gnetici ed infine la banda perforata, ogni caratte-
re e' rappresentato da un insieme di sette variabi.
li binarie denominate bit: sei bit servono per la
rappresentazione del carattere vero e proprio,
settimo, che viene denominato bit di disparita ,ser
60
61
```
LA CONFIGURAZIONE IN BIT DEI CARATTERI DELL' ELEA 9003
fedcba
ZONA
ZONA dc b a
c e
0000 0001 0011 0111 0100 1000 1001 1011 1111 1100 0010 0101 0110 1010 1101
1110
~
3 4 5 6 7 8 9
#
biA B C DEEGHI
È'SKIMNOPOR
STUVWXYZ
(n *=0
#
o
LA CONFIGURAZIONE DEI CARATTERI DELL'ELEA 9003 SU NASTRO PERFORATO
62
65 4321
ZONA 4 32 1
ZONA
6 5
0001 1001 1000 0100 1100 1010 0110 0101 0011 0010 0000 0:11 1111 1011 1101 1110
..
#
+
5 6 7 8 9
~
o
x
DE EGHIS
u
-
@
>
. Un
.
```
ve per il controllo dell' esatta registrazione delle
informazioni. Piu' precisamente il settimo bit e' 0
o 1 in modo che il numero dei bit 1 che compaiono in
ogni carattere sia dispari. Su banda perforata non
compare il settimo bit.
Tali bit sono materializzati:
- da posizioni di perforazione sulla banda perfora-
ta:
- da nuclei magnetizzabili nella memoria principale
e nei registri del calcolatore;
- da aree di magnetizzazione nei nastri e tamburi ma
gnetici.
I sei bit del codice permettono ovviamente di rap-
presentare 64 caratteri fra cifre decimali, lette-
re, punteggiatura, principali simboli matematici, e
altri caratteri speciali, che solitamente vengono
utilizzati per l'organizzazione delle informazioni.
Per codice del calcolatore: si intende il codice
usato per le memorie a nuclei magnetici e per i na-
stri e tamburi magnetici; per "codice di perforazio
ne: il codice utilizzato nella perforazione della
banda. Le lettere a, b, c, d, e, f, nel codice del
calcolatore, ed i numeri 1, 2, 3, 4, 5, 6 nel codi-
ce di perforazione, indicano la posizione dei diver
si bit nell'ambito del carattere rappresentato.
I singoli caratteri possono essere raggruppati con
diversi criteri in modo da formare parole, elemen-
ti, blocchi, sequenze, ecc. La parola e' formata da
uno o piu' caratteri e identifica una unita' di in-
formazione : una quantita' numerica, un nome, una da
ta, есс
63
Durante l'elaborazione una parola puo' essere iden-
tificata mediante il suo indirizzo iniziale di memo
ria e la sua lunghezza oppure per mezzo del suo ca-
rattere estremo scelto a piacere tra i 64 possibi
li.
un elemento e composto da una o piu parole
eral-
presenta, ad esempio, un fatto contabile o ammini.
strativo, come un movimento bancario o di magazzi
no,
ecc.
Un blocco e' composto da uno o piu' elementi. Una se
auenza e' composta da uno o piu blocchi.

## 6.3. La codificazione delle istruzioni

Una istruzione di programma e' codificata per mezzo
di otto caratteri alfanumerici. Questi hanno normal
mente la seguente funzione : il primo - nell'ordine
in cui sono esaminati dall'unita' di governo - indi
ca la funzione F, che definisce di quale tipo di i-
struzione si tratta; il secondo indica il registro
T modificatore, il cui contenuto modifica l'indiriz
2o; i quattro seguenti contengono un indirizzo I ;
gli ultimi due specificano la lunghezza L dell' in
formazione da trattare.
Vi sono pero' molte importanti eccezioni a questa re
gola : ad esempio, per tutte le istruzioni di salto
l'ultimo carattere specifica il tipo di salto; le i
struzioni interessanti memorie e registri hanno la
configurazione
64
LA CONFIGURAZIONE DELLE ISTRUZIONI DELL'ELEA 9003
SPECIFICA
ILTIPO OI OPERAZIUN
INDICAL RE
GISTRU O MUNICIC
• PAPPRESENTALONECARAIERI DA URL
- RARE A PARTIRE DALL'INDIRIZZI
IL TIPO DI OPERAZIONE
• DA L'INDIRIZZO DELLA PAROLA
INDICA IL REGISTRO DEL IT° OPERANDO
DI CARATTERI DA OPERA
i cocci
F
L
• SPECIFICA IL TIPO DI OPERAZIONE
• INDICA IL REGISTRO SU CUI SI OPERA
DA OPERARE SUL PEGISTRO 1
• SPECIFICA IL TIPO DI OPERAZIONE
= INDICA IL REGISTRO T DI MODIFICA
• INDIRIZZO DELL'ISTRUZIONE CUI SI SALTI
= REGISTRO T IN CUI VIENA
DICORDATO LINDI
SI DEVE VERIFICARI
• EEEETTUAT
• TIPO DI OPERAZIONE
DEGISTRO T DI MODIFICA
INDIRIZZO DEL BLOCCO IN MEMORI
UNITA A NASTRO CHIAMATA AD OPERAR
CARATTERE NON CONSIDERATO
65
Qualunque sia il significato degli otto caratteri di
una istruzione, la sua esecuzione si svolge in due
fasi : una fase preparatoria ed una fase esecutiva.
Alcune istruzioni non comportano fase esecutiva.
La fase preparatoria ha una durata di nove periodi
di cifra, che si indicano con i simboli da po a p8;
i periodi da p1 a p8 sono utilizzati per la lettura
e l'analisi dei caratteri dell'istruzione, e per la
predisposizione degli organi interessati all'istru-
zione stessa
In molti casi alcune posizioni dell'istruzione non
hanno significato, e non sono neppure esaminate dal
l'unita' di governo, in queste posizioni si scrive-
ra, per convenzione. la lettera x
Esse possono contenere un carattere qualsiasi, e pos
sono quindi essere utilizzate per la registrazione
di costanti o altre informazioni.
Si e' visto che la posizione p2 dell'istruzione in-
dica il registro T che deve intervenire a modifica-
re l'istruzione stessa, Se non si desidera che que
sta venga modificata e' necessario indicare un regi
stro T inesistente : cio' si ottiene registrando in
p2 il carattere # (diesis), oppure il carattere
(da ... a). E' questo un fatto generale : se in una
istruzione una determinata posizione indica normal-
mente uno fra diversi organi della macchina, e non
si vuole richiamare nessun organo di quel tipo, in
essa si deve registrare un # (diesis).
Le posizioni da p3 a p6 sono normalmente riservate
all'indirizzo, e precisamente
p3 indica le unita' dell'indirizzo
p4 indica le decine dell'indirizzo
66
p5 indica le centinaia dell'indirizzo
p6 indica le migliaia dell'indirizzo.
Le unita' e decine sono sempre espresse mediante ca
ratteri numerici; le centinaia e le migliaia invece
possono essere espresse con caratteri sia numerici
che alfabetici o speciali: cio' permette di indica
re con solo 4 caratteri tutti gli indirizzi della me
moria principale. La tabella N. 3 in appendice ri-
porta la corrispondenza fra i caratteri registrati
in p5 e p6 e le migliaia e centinaia.
Esempi:
L'indirizzo 12012 sara' indicato B012
L'indirizzo 31152 sara' indicato s152
L'indirizzo 42500 sara' indicato 2E00.
L'indirizzo che compare nell'istruzione e' quello del
la posizione di memoria in cui compare il segno o il
carattere meno significativo della parola da opera-
re. L'operazione inizia dall'indirizzo specificato
e procede per indirizzi decrescenti. Cosi' ad esem-
pio l'indirizzo della parola 546ABUL e' 1015
Caratteri
Posizioni di memoria
67
40.000
80.000
POSIZIONI
120.000
POSIZIONI
160.000
POSIZIONI
CARATTERI RAPPRESENTANTI LE MIGLIAIA E LE CENTINAIA NEI DIVERSI GRUPPI DI MEMORIA
DECINE
UNITA MIGLIAIA
UNITA CENTINAI
8 9
12 3 4 56 7 8 9
4 5 6 7 8 9
E FGH
NOPQR
WX Y Z
•ABCDEFGH
U
N
O P
WX Y Z
12
7 8
STUVW X YZ
M NO PQ
R
UV WXYZ
68
Tabella N. 3

## 6.4. Modifica automatica delle istruzioni

Per ogni istruzione e' indicato se essa e' modifica
bile automaticamente, nel qual caso il registro T mg
dificatore e' specificato nella posizione p2.
L'operazione di modifica avviene nel modo seguente:
i caratteri che si trovano in posizione p3 p4 p5 p6
p7 dell'istruzione vengono sommati ai caratteri con
tenuti nel T modificatore, dall'inizio di questo fi
no al bit gT per un massimo di cinque posizioni. Le
posizioni p3, p4 e p5 dell'istruzione, cosi' come le
corrispondenti posizioni 1ª, 2a e 3a del T modifica
tore, possono contenere solo cifre decimali; su que
ste posizioni la somma viene effettuata secondo le
regole della aritmetica in base 10 e gli eventuali
riporti passano dalla 1a alla 2a posizione, dalla za
alla 3ª, dalla 3a alla 42, La posizione p6 dell'i-
struzione e la 4ª posizione del T modificatore pos-
sono invece contenere i caratteri alfabetici o spe-
ciali utilizzati per rappresentare le migliaia del-
l'indirizzo fino a 39.000 (da 40.000 a 79.000 , da
80. 000 a 119.000, da 120.000 a 159.000 a seconda del
la capacita' della memoria principale). La addizio
ne di questi due caratteri da come risultato il ca
rattere che rappresenta la somma delle migliaia in-
dicate nei due addendi (tenendo conto dell' eventua-
le riporto dalla 3ª posizione di somma); oppure se
viene superato il trentanovesimo migliaio, il carat
tere che rappresenta la stessa somma diminuito di
quaranta. Non vi e' mai passaggio di riporto alla 52
posizione di somma, ma di tale riporto si tiene con
to sulla 4ª posizione stessa.
In altre parole, la somma sulla 4à posizione si ef-
fettua secondo una aritmetica in base quaranta con
soppressione del riporto; le cifre di tale aritmeti
ca sono elencate nella tabella N. 3
69
ESEMPI D MODIFICA AUTOMATICA DELLE ISTRUZIONI
0 5 4 1 8 7 3 F
B 0 1 5 E F
8 2
2:7 C 3 2
10 5•5 0
U.A.L.
410N 3 3 90
ES. 1 - 20:000 POSIZION
40000
[2 A, 8.2,50 F
112 5 5 0 2 6 F
4:5 8 1 2
3:6 P 2 0 3
11 201 9 5 2°
U.A.L
1 8•H 7 0 5•
ES. 3 - 20:000 POSIZIONI
ES. 4 - 40'000 POSIZION
3 4 B 0 1.5 EF
12 SE 028 F
217 C 3 2
112 BE 00
4 1.5 3 3 9.
1 404 0 0 2•
~ 20'000 POSIZIONI
70
SEGNC
U.A.L
E' chiaro che tali regole permettono lamodifica au
tomatica degli indirizzi entro 40.000 posizioni di
memoria circolare.
L'indicazione delle centinaia nei gruppi di memoria
oltre le 40.000 posizioni si ha mediante caratteri
alfabetici o speciali.
Dal carattere usato per le centinaia l' elaboratore
riconosce il gruppo di appartenenza di un indiriz-
Zo.
Finalmente la 5ª posizione del T modificatore vie-
ne sommata, secondo le regole dell' aritmetica in ba
se 10, alla posizione p7 dell'istruzione; tali po-
sizioni possono quindi contenere solo cifre decima
li. L'eventuale riporto viene sommato al carattere
contenuto nella posizione p8 dell'istruzione.
La modifica automatica non esige alcun tempo sup-
plementare di fase preparatoria: viene poi esegui-
ta l'istruzione modificata (nella quale ovviamente
1' indicazione del T modificatore non ha alcun inte
resse).
Il contenuto del T modificatore non viene alterato
dalla modifica automatica dell'istruzione.

## 6.5. Lunghezza degli operandi nelle istruzioni interne.

Le istruzioni interne sottoindicate possono speci-
ficare la lunghezza dell' operando, o indicando con
due caratteri numerici posti in p7 e p8 (LL) il nu
mero dei caratteri costituenti l' operando,
oppure
indicando il carattere registrato in memoria dopo
l'ultimo carattere dell' operando stesso.
71
Cio' puo' essere fatto in due modi diversi :
a) il carattere che segue l'ultimo carattere del-
1' operando e' ben determinato e conosciuto dal
programmatore. Esso deve essere allora registra
to nella posizione p8 mentre nella posizione p7
si deve porre
Q: se si vuole che, terminata l'operazione
1' indirizzo del carattere chiave sia trasferi
to nel registro T9 ;
- P: se non interessa che l'indirizzo del ca-
rattere chiave sia trasferito nelle prime 4 pg
sizioni del registro T9.
b) l'ultimo carattere dell'operando e' seguito da
un carattere alfabetico o speciale. La posizio-
ne p8 e' allora non interessante, e nella posi
zione p7 si deve porre
- Z : se si vuole che, terminata l'operazione
l'indirizzo del carattere chiave sia trasferi
to in T9 ;
- Y: se non interessa che l'indirizzo del ca-
rattere chiave sia trasferito nelle prime 4 pg
sizioni del registro T9.
In entrambi i casi l'operazione prosegue fino a che
viene letto un carattere non numerico.
Il carattere chiave letto in memoria e' sempre ri-
generato nella posizione di memoria in cui si tro.
Va.
Agli effetti del calcolo il carattere chiave e' con
siderato uno zero di memoria, o piu' in generale un
numero non significativo, Esso indica sempre la fi
ne della parola in memoria.
72
Se il carattere chiave ricercato si trova all'indi
rizzo IIII, specificato nell'istruzione interessa-
ta. la macchina si arresta su tale posizione ed ir
19 viene registrato detto indirizzo.
Cio' non avviene se il carattere chiave e'
un
gno "piu' " o "meno
Se.
Le istruzioni che operano secondo le modalita' a)
e b) precedentemente indicate sono
MA, AM, AOM, +MA, +AM, -MA, CMA
MEM, +MM,
-MM, CMM
Y, +X, -X;
TOL.
Le istruzioni che operano soltanto nel modo b) so-
no:
MT, TM, ToM, +MT, -MT, CMT ;
XLD, XLN, +LD.
Eventuali eccezioni a queste regole sono riportate
nella descrizione delle singole istruzioni.
Esempio:
Nel caso che si voglia trasferire in accumulatore
mediante un'istruzione MA la parola 519+ registra-
ta in memoria come in figura :
carauterl
Posizioni di memoria
73
la parte lunghezza e indirizzo dell'istruzione puo'
essere espressa

## 6.6. Registrazione del programma

Perche' possano essere esaminate ed eseguite dalla
unita' centrale, le istruzioni di programma devono
essere registrate nella memoria principale.
Il modo normale di leggere una informazione in memo
ria principale e' di leggerla - carattere per carat
tere - per indirizzi decrescenti; l'indirizzo del-
l'informazione in memoria e' pertanto l' indirizzo
del suo estremo carattere di destra.
Conseguentemente, le istruzioni in memoria principa
le sono registrate come e' indicato dalla figura; il
carattere F, che sara' esaminato per primo dall' uni
ta' di governo, occupa la posizione di memoria ad in
dirizzo piu' elevato; il carattere Tla posizione di
indirizzo immediatamente minore, e cosi' di segui-
to.
Se dopo l'istruzione n deve essere eseguitalaistru
Zione n+1, questa dovra' essere registrata in memo
74
ria alla destra della precedente.
FIL
ISTRITIONE n
Il programma puo' essere registrato in una zona qual
siasi della memoria; questa puo' infatti contenere
indifferentemente dati da elaborare, risultati o i-
struzioni di programma, in ogni sua posizione. Sup-
poniamo di registrare il programma nelle prime posi-
zioni di memoria, a partire dall'indirizzo 0001: il
carattere F della prima istruzione avra' quindi lo
indirizzo 0008, il carattere F della seconda istru-
zione l'indirizzo 0016, e cosi' via.
Da quanto si e' detto precedentemente, risulta chia
ro che, perche' l'organo di governo esegua una i-
struzione deve rivolgersi all'indirizzo del caratte
re F di quella istruzione (dunque nel caso anzidet-
to, successivamente agli indirizzi 0008, 0016, ecc.).
Tale indirizzo si dice brevemente indirizzo dell'i-
struzione.
75
Ad ogni istruzione e' stato dato anche un codice sim
bolico piu' facile da ricordarsi mnemonicamente
quindi piu' comodo nella prima stesura di unprogram
ma Cosi' ad esempio l'istruzione per confrontare
fra di loro due zone di memoria che ha come codice
di funzione il carattere •/. viene indicata con il
codice simbolico CMM.
Il programma normalmente viene svolto eseguendo suc
cessivamente le istruzioni una dopo l'altra nell'or
dine in cui sono registrate in memoria a partire da
quella indicata all' avvio sul quadro di controllo;
speciali organi di governo contengono 1' indirizzo
dell'istruzione. Si possono svolgere pero contempo
raneamente tre diversi programmi sequenziali come sa
ra' meglio specificato in seguito.
Questo modo di procedere sequenzialmente puo' esse-
re variato mediante apposite istruzioni (istruzioni
di "salto:) che permettono di eseguire sequenze di-
verse sia sistematicamente sia in funzione di even-
ti rilevati durante l'elaborazione, sia a seguito
di condizioni impostate direttamente sul quadro di
controllo. Vi sono 90 diversi tipi di istruzione di
cui 38 di salto. Le istruzioni di salto: specifica
no tra l' altro l'indirizzo della prossima istruzio-
ne da eseguire
76
LEGENDA
Schema istruzioni
, Funzione
• codice simbolico
- organi impegnati durante
la fase esecutiva
- configurazione
tempo, in periodi di cifra,
necessario all'esecuzione
dell'istruzione (Fasi a e 1).
Configurazioni istruzioni
=
memoria - registri
costante
- registri
salti
memoria - accumulatore
antono.
n ne no.c
nastri
Accumulatore
Registri T
Memoria:
contenuto,
malizz
77

