# CAP. 7° : ISTRUZIONI RIGUARDANTI L° UNITA CENTRALE

## 7.1. Istruzioni memoria-accumulatore

Queste istruzioni interessano la memoria principale
e 1' accumulatore; nel loro svolgimento impegnano la
unita' aritmetica e logica ed il governo dell' elabo
ratore.
Sia durante la fase preparatoria che in quella ese.
cutiva il canale interno risulta impegnato; a que
sto gruppo di istruzioni potranno percio' sovrappor
si operazioni che impegnano il canale esterno ed il
governo unita a nastro
Queste istruzioni sono normalmente utilizzate
a) per trasferimenti da memoria verso accumulatore
e viceversa di parole segnate o non segnate di
lunghezza conosciuta o sconosciuta, non superio-
re a 100 caratteri, hanno questa funzione le i-
struzioni
MA, AM, AOM
b) per operazioni aritmetiche o algebriche su nume-
ri di lunghezza variabile da 1 a 100 caratteri;
hanno questa funzione le istruzioni
~ MA
- MA, + AM
c) per confronti tra valori assoluti, numeri alge
brici o parole alfanumeriche, di lunghezza non su
periore a 100 caratteri; ha questa funzione l'i-
struzione
CMA
d) per determinare la lunghezza di una parola conte
nuta in accumulatore, escluso l'eventuale segno
79
algebrico.
In quest'ultimo caso e' necessario ricorrere a par
ticolari accorgimenti di programmazione.
Sistema a) Sia registrata mediante istruzione FAM
la lunghezza del numero segnato conte-
nuto in accumulatore, nelle posizioni
p7 e p8 di un'istruzione AM o AoM.
L'opportuna modifica di LL e' ottenibi
le mediante il registro modificatore in
dicato in p2 della stessa istruzione.
E' sufficiente infatti sommare al con-
tenuto di questo registro il valore
10.000 perche' il bit gT passi in quin
ta posizione e la cifra piu' signifi-
cativa incrementi di una unita' la lun
gnezza espressa mediante l'istruzione
FAM.
Sistema b) Si provvede, mediante una istruzione CT,
a registrare all'inizio del ciclo di
elaborazione comprendente l'istruzione
FAM il valore 1 in un determinato regi
stro.
Si invia quindi mediante l'istruzione
FAM la lunghezza del numero segnato con
tenuto in accumulatore sulle posizioni
p3 e p4 di una + CT che permette di som
mare detta lunghezza all' unita' preesi
stente nel registro precedentemente ope
rato.
Si ottiene in questo modo nel registro
la lunghezza esatta del numero algebri
co (valore assoluto + segno) che puo'
essere trasferita mediante M nell' i-
struzione interessata all' uscita del da
to dall' accumulatore.
80
Dispone accumulatore
DA
interno
XXII
Im
A (010001)
10
XXXX
I I
Im
: posizioni non utilizzate
: indirizzo di accumulatore
: Il registro Im puo' modificare l'indirizzo II
: fissa l'inizio dell' accumulatore alla Ilesima
posizione
a) Il contenuto dell' accumulatore rimane immutatc
X,x x x 0 2 # A
DISPONE ACCUMULATOA
198653471
POSIZIONATE
X x x x 0.5 #
1.9 8 6.5.
3.
tat
81
interno
Trasferisce da memoria ad accumulatore
LL
IIII
Im
MA
(011001)
10 + 1
IIII
Im
F
: lunghezza dell' operando da trasferire in accumulatore
indirizzo di memoria dell' operando che deve essere tra-
sferito
il registro Im puo' modificare sia l' indirizzo IIII che
la cifra delle unita' della lunghezza LL
: trasferisce dalla memoria a partire dall'indirizzo IIII
per lunghezza LL e per indirizzi decrescenti all' accumu
latore a partire da
DA
a, La memoria non resta azzerata.
b) I caratteri trasferiti si sostituiscono a quelli precedentemente contenuti nell'ac
cumulatore
c) In corrispondenza dell'ultimo carattere trasferito viene posto un bit gA
d) Se all'indirizzo IIII si trova un segno questo viene registrato nell'apposito regi
stro del segno e l'informazione viene trasferita nell' accumulatore, da DA e per una
lunghezza LL-1 a partire dall'indirizzo di memoria IIII-1.
e) Per questa istruzione valgono le regole relative ai casi di fine su carattere chi:
ve; in accumulatore, invece del carattere chiave, viene trasferito uno zero, ec
1 1.
bit gA posizionato sotto quest'ultimo.
0 8 1 930 2.
TRASFERISCE DA MEMORIA AD ACCUMULATORL
10.00.0.
82
Trasferisce da accumulatore a memoria senza azzeramento
AM
interno
L
† I I I
Im
G (011011)
10 +1
LL
IIII
Im
G
: lunghezza dell' operando da trasferire dall' accumulatore
: indirizzo di memoria a cui l'operando deve essere
sferito
tra-
:il registro Im puo' modificare sia l'indirizzo IIII che
la cifra delle unita' della lunghezza LL
: trasferisce dall' accumulatore a partire da DA, alla me-
moria a partire dall'indirizzo IIII per lunghezza LL
per indirizzi decrescenti
al Tl contenuto dell' accumulatore e del registro del segno. le posizioni del DA:e del
bit gA restano invariate
b) Se la parola contenuta in
accumulatore e' segnata, il segno viene registrato
memoria all'indirizzo IIII e i caratteri contenuti in accumulatore, a partire
in
ds
DA, sono trasferiti in memoria a partire dall'indirizzo IIII-leperlunghezzaLL-1
c) Per questa istruzione valgono le regole relative ai casi di fine su carattere chia
ve : quest'ultimo deve essere contenuto in memoria.
0 6 19.30 1,G
TRASEEPISCI
6 4 0
3.0
REG. N. 1 10.0 0 0.
2
83
Trasferisce da accumulatore a memoria con azzeramento
interno
L
L
II I I
Im
B (010011)
AoM
10 + 1
LL
IIII
Im
: lunghezza dell' operando da trasferire dalle accumula-
tore
: indirizzo di memoria a cui l'operando deve essere tra
sferito
: il registro Im puo' modificare sia l'indirizzo IIII
che la cifra delle unita della lunghezza LL
: trasferisce dall' accumulatore a partire da DA, allame
moria a partire dall'indirizzo IIII per lunghezza LL
e per indirizzi decrescenti
a, Le posizioni di accumulatore interessate al trasferimento vengono azzerate
h; In ognuna di queste posizioni e' posto un bit gA.
c. Il registro del segno passa allo stato "non segnato, in vera grandezza
di Qualora nelle posizioni p7 e p8 fosse registrato il carattere # (diesis) l'e
secuzione di una tale istruzione provoca l' azzeramento totale della
' memoria
principale.
e, Per questa istruzione valgono le regole relative ai casi di fine su.
carattert
ah ave quest'ultimo deve essere contenuto in memoria
0819282
TRASFERISCE DA ACCUMULATORE A МЕИОР
ACCUMULATORE DOPO
ASFERIMENTI
9 4 5 8 974
0000000
10,00,04
84
Somma memoria ad accumulatore, risultato in accumulatore
interno
L
IIII
Im
(010111)
+ MA
10 + 1
LL
IIII
Im
": lunghezza dell' operando registrato in memoria
: indirizzo di memoria dello stesso operando
: il registro Im puo' modificare sia 1' indirizzo IIII che
la cifra delle unita della lunghezza LL
: somma il contenuto della memoria a partire dall'indiriz
20 IIII per lunghezza LL e per indirizzi decrescenti
al contenuto dell' accumulatore compreso tra DA e bit gA
a) Il risultato si trova in accumulatore a partire da DA
b) Il contenuto delle posizioni di memoria interessate dall'istruzione rimane inalte
raco.
c) L'operazione si effettua di regola sommando caratteri numerici.
d) Qualora in uno o in entrambi gli addendi siano presenti caratteri alfabetici, que
sti vengono sommati secondo la logica aritmetica esposta nel manuale.
e) E' sufficiente che uno dei due operandi sia segnato perche' la operazione risulti
a gebrica.
1) Se uno solo degli operandi e' segnato l'altro e considerato positivo.
g) Per questa istruzione valgono le regole relative ai casi di fine su carattere chia
0.6 1.92,1 2,6
SOMMA MEMORIA
REG. N
10,0.0 0 6
ACCUMULATORE ODINA
85
Somma accumulatore a memoria, risultato in memoria
+ AM
interno
LL
Im
X (011110)
10 +1
LL
I I I I
Im
y
: lunghezza dell' operando registrato in memoria e lun"
ghezza massima dell' operando registrato in accumulatore
: indirizzo dell' operando registrato in memoria
:il registro Tm puo' modificare sia l'indirizzo IIII che
la cifra delle unita della lunghezza LL
• somma il contenuto dell° accumulatore compreso tra DA €
bit gA al contenuto della memoria a partire dall'indi
rizzo IIII per lunghezza LLeper indirizzi decrescenti
a) Se LL e maggiore del numero delle posizioni di accumulatore comprese tra DA e bil
gA, le cifre oltre il bit gA non vengono operate.
b) Se LL e' minore del numero delle posizioni di accumulatore comprese tra DA e bit
gA, le cifre oltre la lunghezza LL non vengono operate, e si ha indicazione di
overflow.
c) Il risultato si forma in memoria a partire dall'indirizzo IIII
d) Il contenuto dell' accumulatore rimane invariato.
e) Non si ha passaggio di riporto oltre la lunghezza specificata in LL
il Si ha indicazione di overflow nel caso in cui si dovrebbe avere riporto oltre
lunghezza indicata.
g) L'operazione puo'
essere eseguita anche tra parole segnate con le seguenti limiti
sioni
del segno in accumulatore si tiene conto solo per stabilire se il contenuto d
accumulatore va sommato o sottratto al contenuto delle posizioni di memoria:
se la memoria e' segnata, l'indirizzo IIII deve essere quello del segno:
3 - il segno di memoria non viene preso in considerazione e pertanto rimane immu
cato,
4 - in caso di sottrazione, se il contenuto dell'accumulatore e' › di quello del
la memoria il risultato e' in complemento e si ha indicazione di overflow.
h Per questa istruzione valgono le regole relative ai casi di fine
caratte
chiave.
86
SOMMA ACCUMULATORE A MEMORIA
9 2 4 3
00 0 000C
2 4 2 4
10 0 00
6
3 9 5.6 6
S
MEMORIA PRIMA
87
Sottrae memoria da accumulatore, risultato in accumul.
interno
LL
I I I I
Im
H (011111)
- MA
10 + 1
LL
IIII
Im
H
: lunghezza dell' operando registrato in memoria
: indirizzo di memoria dello stesso operando
:il registro Im puo' modificare sia l'indirizzo IIII che
la cifra dellé unita della lunghezza LL
: sottrae al contenuto dell' accumulatore compreso tra DA
e bit gA il contenuto della memoria a partire dall'indi
rizzo IIII per lunghezza LL e per indirizzi decrescenti
a) Il risultato si trova in accumulatore a partire da DA.
b) Il contenuto delle posizioni di memoria interessate dall'istruzione rimane inalte
rato.
c) L'operazione si effettua sommando al minuendo il complemento del sottraendo.
d) E sufficiente che uno dei due operandi sia segnato perché' l'operazione risult:
algebrica.
e) Se uno solo degli operandi è' segnato l'altro e' considerato positivo.
f, Per questa istruzione valgono le regole relative ai casi di fine su carattere ch.
0 6 10 003 H
DA ACCUMULATORE
1.0.
0.9.2
2 Я
000
ACCUMULATORE PRIMA
DELLELABORAZIONE
8 2
88
Confronta memoria con accumulatore
CMA
interno
LL
IIII
Im
E (011000)
10 +1
LL
IIII
Im
E
: lunghezza del termine di confronto registrato in memo-
ria
: indirizzo di memoria dello stesso operando
: il registro Im puo' modificare sia l'indirizzo IIII che
la cifra delle unita' della lunghezza LL
: confronta il contenuto della memoria a partire da IIII
per lunghezza LL e per indirizzi decrescenti con il con
tenuto dell? accumulatore compreso tra DA e bit ga
a) Il confrontc
eseguito per tutti i caratteri anche non numerici, in base all'or
dine gerarchico dei caratteri (vedi elenco dei caratteri).
b) Nel confronto si tiene conto dei segni se questi sono
per l'informazione contenuta in memoria, il primo carattere chiamato:
- per quella contenuta in accumulatore,il carattere contenuto nel registro del se
se i caratteri + e - sono contenuti nell'informazione diversamente da come det
to prima, risulta >+;
se delle due parole da confrontare una sola è' segnata, quella non segnata
considerata positiva.
c) Il risultato del confronto e' ricordato dall'unita' di governo e puo'
quindi ser
vire a condizionare il proseguimento dell'elaborazione fino a che non viene
fettuato un nuovo confronto (CMA, CMT, CM, CCT).
d) Per questa istruzione valgono le regole relative ai casi di fine
chiave
quest'ultimo deve essere contenuto in memoria
car accert
0 4 0 0 0 0 35
CONFRONTA MEMORIA
COn ACCUmULATOR
REG. N. 3
12,1.9.2
5 2 3 9
89
Fine accumulatore in memoria
FAM
interno
0
IIII
Im
g (010010)
0 1
IIII
Im
: caratteri che determinano il genere di lunghezza ricer
сата
: indirizzo a cui viene portata la lunghezza richiesta
: il registro Im puo' modificare l'indirizzo IIII
: trasferisce all'indirizzo IIII e per indirizzi decre-
scenti il numero di cifre contenute in accumulatore d
DA a bit gA.
a) Se in p7 e p8 vengono registrati i caratteri 0 1 (zero, uno), all'indirizzc
IlI e' trasferito il numero delle cifre significative comprese tra DA e bit gA
b) Se in p7 e p8 vengono registrati i caratteri
0 (punto zero);
all' indirizze
IIII e' trasferito il numero delle cifre significative e non significative com
prese tra DA e bit gA.
c) La lunghezza richiesta viene registrata sempre mediante 2 cifre
d) Se richiedendo il numero di cifre significative (caso "a") non ne risultasse al
cuna, vengono trasferiti all'indirizzo IIII e IIII - 1, i caratteri 0 1 (zero
uno
Esempio della nota d)
0.1 1.9,2,8 #.
• MEMORIA NO CIFRE
ICATIVE DI ACCUMULATORE.
0.0.0.
2 Я
O
190
0.1 1.9.2.8 #
.. 019.28 #,
1 9
2 8
PASFERISCE IN MEMORIA NO CIERA
0.04.529
TRASFERISCE IN MEMORIA NO CIFRE SIGNIFICATIVE
00 4
91
SCHEMA RIASSUNTIVO
Istruzioni Memoria Accumulatore
Аом
Trasferimento
Operazioni aritmetiche
Confronto
Determinazione lunghezza
MA
+MA
СМА
FAM
†AM
Particolarita' dell'Accumulatore
CODICE
SIMBOLICO
PANATA
revod
IN PERIODI DI CIFRA
Capacita' : 100 posizioni.
DA
fissa l'indirizzo dell'accumulatore.
Bit gA
segnale fine-informazione in accumulatore.
Regole
) Non viene spostato se l'operando in memoriaha lun
ghezza uguale al numero di posizioni comprese tra
DA e bit gA
b) Viene posto in corrispondenza dell'ultima
trasferito in accumulatore:
c) Viene posto in corrispondenza della cifra piu' si
gnificativa del risultato.
Registro
da indicazione del segno e della configurazione del
del segno
ricultato in accumulatore
Per le ope la regola di comolementazione e' la seguente: lamac
razioni a.
china esegue la complementazione se il numero di se
ritmetiche : gni "meno" che risulta dall'esame del segno dell'ope
razione, del segno dell'operando in memoria. del se
eno dell'operando in accumulatore e del segno del moï
tiplicatore.
e' dispari.
Dar i segni prevista l'inversione del segno del..
¡'operando complementato: sono poi valide le regole
algebriche sui segni.
Dar i tro.
sferimenti
il registro indichera'
non segnato in vera grandezza dopo una istruzione
AMo una MA che neri audi un numero non segnato.
segnato in vera grandezza dono una istruzione
che onori eu di un numero sernato.
segnato in comolemento.
dota conuno detennio
ne tipo AM.
wino trasferito in vere grandergo rol
segno effettivo:
non segnato in commlemento. il dato
con urliaten
zione tipo AM. viene trasferito tale e guale.
DA
MA
AM
дом
+MA
+ AM
…MA
СМА
FAM
PAN
interno
10
5
CONFIGURAZIONE
Im
Im
=
=

## 7.2. Istruzioni memoria-memoria

Queste istruzioni interessano soltanto la memoria
principale; nel loro svolgimento impegnano l'unita'
aritmetica e logica ed il governo dell' elaboratore.
La fase preparatoria di una istruzione di
questc
gruppo, come per gli altri tipi d' istruzione, impegna
il solo canale interno, la fase esecutiva invece im
pegna ambedue i canali
A questo gruppo di istruzioni possono percio' sovrap
porsi operazioni eseguibili mediante il solo gover
no unita a nastro.
Esse sono normalmente utilizzate
a) per trasferimenti, da una zona di memoria ad una
altra, di un numero variabile da 1 ad n-2 carat-
teri (n = numero totale delle posizioni di memo
ria); cio' si ottiene mediante le istruzioni
PUM MEM
b) operazioni aritmetiche su parole di lunghezza va
riabile da 1 a n/2 caratteri; hanno queste
tun
zioni. le istruzioni
PUM
† MM PUM
MM
c) confronti tra parole alfanumeriche oppure tra nu-
meri entrambi segnati, di lunghezza variabile da
1 a n/2 caratteri; hanno questa funzione le i-
struzioni
PUM CMM
Per ottenere 1' azzeramento della memoria principale
per un determinato numero di posizioni e' sufficien
te non indicare alcun indirizzo nelle posizioni da
p3 a p6 dell' istruzione PUM riferita ad una MEM.
93
interno
Prepara uscita memoria
L
L
IIII.
- Im
PUM
(001110)
10
LL
IIII
Im
: lunghezza dell' operando
: indirizzo dell' operando in memoria
: il registro Im puo' modificare sia 1' indirizzo IIII che
la cifra delle unita' della lunghezza LL
: prepara l' uscita da memoria di un operando.
a) Se in p% e in p8 e' registrato il carattere# (diesis) la lunghezza dovra' esse
re indicata dall'istruzione MEM. CM. + MM, - MM che segue.
b, Se in pl e p8 e' indicata la lunghezza, nella istruzione MEM, CMM, + MM o
- MM
che segue, in luogo della lunghezza dovranno essere registrati due zeri (00).
c) L'istruzione PUM deve essere immediatamente seguita nel programma dalla istruzio
ne esecutiva
0 6 1 9 2 6 #
÷
1 2 6
94
Trasferisce da memoria a memoria
MEM
esterno ed
interno
LL
III I
I'm
1 (000001)
10 + 1
LL
IIII
Im
: lunghezza dell' operando indicato nella PUM
: indirizzo di memoria a cui l' operando va trasferito
: il registro Im puo' modificare sia 1' indirizzo IIII che
la lunghezza LL
: trasferisce la parola il cui indirizzo e' stato specifi
cato nella PUM in altra zona di memoria a partire dal-
l'indirizzo IIII specificato nella MEM per lunghezza LL
e per indirizzi decrescenti.
a) Per questa istruzione valgono le osservazioni a, b, c, riguardanti la PUM.
b) La zona di memoria specificata dalla PUM rimane inalterata
c) Con temporaneamente a questa istruzione non puo' essere eseguita alcuna istruzione
che occupi almeno uno dei due canali.
d) Per questa istruzione valgono le regole relative ai casi di fine su carattere chia
ve: quest'ultimo deve essere contenuto nella zona di memoria con indirizzo speci
ficato nella MEM.
TRASEEDISCE
## 1.9 2 6 #
61 9 3 4 #
95
Somma memoria a memoria
+ MM
esterno ed
interno
L
IIII
Im
3
(000111)
10 ÷ 1
LL
IIII
Im
: lunghezza dei due operandi
: indirizzo di memoria del secondo operando
: il registro Im puo' modificare sia l'indirizzo III che
la cifra delle unita' della lunghezza LL
: somma il contenuto della memoria a partire dall'indiriz
20 IIII specificato nella PUM al contenuto della memo-
ria a partire dall'indirizzo IIII specificato nella + MM
per lunghezza LL e per indirizzi decrescenti.
a) Per questa istruzione valgono le osservazioni a, b, c, riguardanti la PUM.
b Tl risultato si forma in memoria a partire dall'indirizzo IIII specificato nella
presente istruzione.
c) Se il risultato e' di lunghezza superiore ad LL non vi e' riporto sulla posizio-
ne adiacente e vi e' indicazione di overflow
d) La zona di memoria specificata nella PUM rimane inalterata.
e) L'operazione puo' avvenire solo per parole non segnate.
1) Con temporaneamente a questa istruzione non puo' essere eseguita alcuna istruzio
ne che occupa almeno uno dei due canala
g) Per questa istruzione valgono le regole relative ai casi di fine su carattere chia
ve: quest'ultimo deve essere contenuto nella zona di memoria con indirizzo spe
cilicaco nella
+ MM
0 5
1.9.2,5 #
o 01
96
esterno ed
interno
Sottrae memoria da memoria
IIII
Im
- MM
8
(001111)
10 +
LL
IIII
: lunghezza dei due operandi
indirizzo di memoria del sottraendo
: il registro Im puo' modificare sia l'indirizzo IIII
che la cifra delle unita della lunghezza LL
: sottrae il contenuto della memoria a partire dall'indi
rizzo IIII specificato nella presente istruzione al con
tenuto della memoria il cui indirizzo iniziale e' spe-
cificato nella PUM, per lunghezza IL e per indirizzi de
crescenti.
a) Per questa istruzione valgono le osservazioni a, b, c, riguardanti la PUM.
b) Il risultato si forma in memoria a partire dall'indirizzo IIII specificato nella
presente istruzione.
c) La zona di memoria specificata nella PUM rimane inalterata.
di l'operazione puo' avvenire solo per parole non segnate
e) Qualora il minuendo sia minore del sottraendo il risultato appare in complemento
e si ha indicazione di overtlow.
†) Contemporaneamente a questa istruzione non puo' essere eseguita alcuna istruzio
ne che occupi almeno uno dei due
can all1
g) Per questa istruzione valgono le regole relative ai casi di fine su carattere chi:
ve quest ultimo deve essere contenuto nella zona di memoria con indirizzo
suC
citicato nella - MM.
0 4 1.9.2,5 #.
0.01
9 3 2 #
97
Confronta memoria con memoria
CMM
interno ed
esterno
LL
I LI I
I'm / (001010)
10 +1
L L
IIII
Im
: lunghezza dei due termini di confronto
: indirizzo del 1° termine di confronto
: il registro Im puo' modificare sia 1' indirizzo IIII
che la cifra delle unita di LL
: confronta il contenuto della memoria a partire dall'in
dirizzo IIII con il contenuto della memoria specifica-
to nella PUM per lunghezza LL e per indirizzi decre-
scenti,
a, Per questa istruzione valgono le osservazioni a, b, c, riguardanti la PUM
b. Il 1° termine di confronto e' quello indicato nella presente istruzione.
c) Le regole del confronto sono le stesse della (MA con l'avvertenza che il confron
to puo' avvenire solo fra informazioni entrambe segnate o entrambe non
segnate
d) Per questa istruzione valgono le regole relative ai casi di fine
chiave: quest'ultimo deve essere contenuto nella zona di memoria con
specificato nella CM.
carattere
indirizzo
9.2.7 $ ÷
10 5 1 9 3.
3 #
98
SCHEMA RIASSUNTIVO
Istruzioni Memoria Memoria
Trasferimento
Operazioni aritmetiche
Confronto
PUM
PUM
PUM
PUM
MEM
+MM
..MM
смм
Particolarita' della memoria centrale
cAnice
SIMBOLICO
CANALI
IMOEGNATI
IN PEGIODL DI CIERA
Capacita'
20000 - 40000 posizioni aumentabile a bloc-
chi di 40000 fino a 160000 posizioni.
PUM
est. int.
Memoria a nuclei
magnetici
mi carattere e' materializzato dallo sta-
to di " nuclei magnetici operati in paralle
10.
MEM
+MM
Tempo di accesso
al carattere
10 microsecondi.
-MM
Indirizzabilita al singolo carattere.
смм
Indirizzi
:sono espressi per mezzo di quattro cifre da
0000 a r'99 (vedi tabella del testo).
CON FIGURAZIONE
CARATTEON

## 7.3. Istruzioni memoria-registri

Queste istruzioni interessano la memoria principale
ed i registri T: nel loro svolgimento impegnano la
unita' aritmetica e logica ed il governo dell' elabo
ratore.
Sia durante la fase preparatoria che in quella ese-
cutiva il canale interno risulta impegnato : a que.
ste istruzioni potranno percio sovrapporsi
onera
zioni che impegnano il canale esterno ed il governo
unita' a nastro
Le istruzioni di questo gruppo sono normalmente uti
izzarc
a) per trasferimenti, da memoria verso registri e vi
ceversa, di parole segnate o non segnate e ner
lunghezza conosciuta o sconosciuta, non superio-
re a 10 caratteri; hanno questa funzione le i-
struzioni:
MT, TM, Том
b) per somme o sottrazioni aritmetiche su numeri di
lunghezza variabile da 1 a 10 caratteri; eventua
li segni algebrici + o -, vengono considerati ca
ratteri qualsiasi; hanno questa funzione le i-
struzioni
+ MT, MT,
TM
c) per confronti tra numeri aritmetici o parole al-
fanumeriche di lunghezza non superiore a 10
ca
ratteri; ha questa funzione l'istruzione
СМт
d) per determinare la lunghezza di una parola conte
nuta in un registro T; ha questa funzione l'i-
struzione
FTM
100
Nota : La lunghezza della parola contenuta in un re
gistro e' sempre espressa dalla istruzione
FTM mediante due caratteri.
Si rende pertanto necessario un accorgimento
di programmazione per posizionare tale lun-
ghezza nell' unica posizione ad essa riserva
ta nelle istruzioni da registro a memoria.
Generalmente tale lunghezza viene registrata
in una zona di comodo della memoria principa
le per essere quindi trasferita per lunghez
za uno (cifra di destra) nella posizione p8
dell'istruzione TM o ToM.
101
interno
Trasferisce da memoria a registro To
L
To
I I I I
Im
MT
X (101001)
10 +1
L
To
I I I I
Im
: lunghezza dell' operando da trasferirsi nel registro To
: registro in cui va trasferito l'operando
: indirizzo di memoria dell' operando da trasferirsi
:il registro Im puo' modificare sia 1' indirizzo IIII che
il nome del registro Io
: trasferisce dalla memoria a partire dall'indirizzo IIII
per lunghezza L e per indirizzi decrescenti, al regi-
stro To
a) I caratteri trasferiti si sostituiscono nel registro To a quelli precedentemente
contenuti nelle posizioni interessate.
b; In corrispondenza del l'ultimo carattere trasferito viene posto un bit gT.
c) Se l'indirizzo IIII contiene il segno della parola, tale segno viene registrato
nella prima posizione del registro To•
d) Il contenuto della memoria rimane inalterato.
e) Per questa istruzione valgono le regole relative ai casi di fine
caratere
chi ave; nel registro T, invece del carattere chiave,
viene trasteritc
111.
zero.
ed il bit ¿™ e' posizionato sotto quest'ultimo.
8 2 1 9 2 83
TRASFERISCE DA MEMORIA A REGISTRO
-REG. N. 3
10.0.0.06
. N.
8.1 4:2.3 6 4.
102
Trasferisce da registro To a memoria senza azzeramento
interno
L
To
I I I I
Im
Y (101011)
TM
10 +1
L
To
IIII
Im
Y
: lunghezza dell' operando da trasferirsi in memoria
: registro da cui l' operando viene trasferito
: indirizzo di memoria a cui viene trasferito l'operando
contenuto nel registro Io
:il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
: trasferisce il contenuto del registro Io in memoria al
l'indirizzo IIII per lunghezza L e per indirizzi decre
scenti.
a) I caratteri trasferiti si sostituiscono in memoria a quelli precedentemente con
tenuti nelle posizioni interessace
b) Il contenuto del registro To rimane in alterato.
c) Per questa istruzione valgono le regole relative ai casi di fine su carattere
chiave: quest'ultimo deve essere contenuto in memoria.
8 2 1 9 2 8 3 Y
TRASFERISCE DA REGISTRI
1,9,2,8
2.1.213.6 8 4 2
1.9.:
10.00.06
103
Trasferisce da registro To a memoria con azzeramento
ToM
interno
L
To
Im
T' (100011)
10 +1
To
TITI
T
: lunghezza dell' operando da trasferirsi in memoria
: registro in cui e' registrato 1' operando
: indirizzo di memoria a cui viene trasferito l' operando
: Il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
: trasferisce dal registro To alla memoria dall'indiriz-
20 IIII per lunghezza L e per indirizzi decrescenti
a) A trasferimento avvenuto le posizioni del registro 1 interessate sono azzerate.
b) In ognuna di queste posizioni e' posto un bit gT.
'c) Per questa istruzione valgono le regole relative ai casi di fine su carattere spe
erale : quest ultimo deve essere contenuto in memoria.
19.0.02
112.3 7.5
REGISTRO DOPO L'AZZERAMENT
REG. N.
112.0.00
0 030
104
Somma memoria a registro To, risultato in registro To
interno
L
To
IIII
Im
U (100111)
+ MI
10 ÷ 1
L
To
IIII
Im
: lunghezza dell' operando registrato in memoria
: registro che contiene il secondo operando
: indirizzo dell' operando registrato in memoria
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro Io
: somma il contenuto della memoria a partire dall' indi
rizzo IIII per lunghezza L e per indirizzi decrescenti
al contenuto del registro To compreso tra la posizione
iniziale e il bit gT
a) Il bit gt viene posto in corrispondenza del carattere piu' significativo del ri-
sutato.
b) Se il risultato in caso di riporto e' di lunghezza maggiore dei due operandi
ha indicazione di overflow.
c) Un eventuale riporto dalla decima posizione invade il registro adiacente
indicazione di overtlow
si ha
d) Se uno degli operandi e' espresso mediante caratteri alfanumerici si puo
gio cita
correttamente su di esso fino a che non esista la necessita di un riporto ol
tre la parte numerica
e) Non e' possibile mediante la presente istruzione ottenere risultati alfanumeric
utilizzabili quali indirizzi di memoria.
1) Per questa istruzione vale solo il caso di fine
caratteze Z o Y deve essere posto in po.
carattere
numerico
il
6 2 1 9.2.8 #U
SOMMA MENDO
REG.
1 113.1.451
s
REG. N.
105
911.0000
interno
Somma registro To a memoria, risult. in memoria
L
To
IIII
Im
(101110)
+ TM
10
L
III I
Im
: lunghezza dell' operando registrato in memoria
registro che contiene il secondo operando
: indirizzo dell' operando registrato in memoria
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
: somma il contenuto del registro Io compreso fra la posi
zione iniziale e il bit gT al contenuto della memoria
partire dall'indirizzo IIII per lunghezza L e per indi
rizzi decrescenti
ah Se l.e?
maggiore del numero delle posizioni del registro T. comprese tra la posi
zione iniziale ed il bit gT, le cifre oltre il bit gT non vengono operate.
minore del numero delle posizioni del registro T. comprese tra la posizio
ne iniziale ed il bit gT, le cifre oltre la lunghezza L non vengono operate e
ha indicazione di overflow.
c) Il risultato si forma in memoria a partire dall'indirizzo IIII.
d) Il registro To rimane invariato.
e) Il risultato non deve superare la lunghezza L.
f) Non si ha l'eventuale riporto oltre la lunghezza L ma solo indicazione
†low
avoi
g) Per questa istruzione valgono le regole relative ai casi di fine su carattert
chiave.
5 3 1 0.0.05
GOMME DEGISTOI
5 4 7
10.0.9,3
106
Sottrae memoria a registro To, risultato in registro To
interno
L
To
IIII
Im
Z (101111)
MT
10 + 1
L
To
IIII
Im
Z
: lunghezza dell' operando registrato in memoria
: registro che contiene il secondo operando
: indirizzo di memoria a partire dal quale e' registrato
il sottraendo
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
: sottrae il contenuto della memoria a partire dall'indi
rizzo IIII per lunghezza L, al contenuto del registro
To compreso fra la posizione iniziale e il bit gT
a) Il bit gT viene posto in corrispondenza del carattere più' significativo del ri
sultato.
bì Se il minuendo e' minore del sottraendo il risultato è' in complemento e si ha
indicazione di overflow.
c) Non e' possibile mediante la presente istruzione ottenere risultati al fanumeri.
ci utilizzabili quali indirizzi di memoria.
d) Se uno degli operandi e' espresso mediante caratteri alfanumerici si puo
opers
re correttamente su di esso fino a che non esista la necessita di un riporto ol
tre la parte numerica.
e) Per questa istruzione valgono le regole relative ai casi di fine
chiave, ponendo in p8 il carattere Z o Y; e evidente che non
so di fine su di un carattere ben determinato.
carattert
possibileil ca
5,2 1,9,3,0 #.
SOTTRAE MEMORIA A REGISTRC
.3.0
19.9 9 9
REG. N. 2
REGISTRO PRIMA
DENNEIBROREZIONI
10,00,25
107
interno
Confronta memoria con registro To
L
To
II I I
Im
W (101000)
CMT
10 + 1
L
T.
IIII
Im
: lunghezza del termine di confronto contenuto in memoria
registro che contiene il secondo termine di confronto
: indirizzo di memoria del termine registrato in memoria
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
confronta il contenuto della memoria a partire dall'in-
dirizzo IIII per lunghezza L, con il contenuto del regi
stro compreso tra la posizione iniziale e il bit gi
a) Per questa istruzione vale cio' che é' stato detto per la MA ad eccezione dei se
gni
"piu' o meno" , che non vengono mai considerati come segni algebrica ma come ca
ratterl.
5 Per questa istruzione valgono le regole relative ai casi di fine su carattert
chiave': quest'ultimo deve essere contenuco in memoria
66 1 9.0.05 W
CONTENUTO REGISTRO T
0.0.3
3 0 4
108
interno
Fine registro To in memoria
IIII
FTM
Io
IIII
Im
To
Im e (100010)
12 + 1
: carattere che determina il genere di lunghezza ricercata
: registro che contiene l'operando di cui si vuole deter.
minore la lunghezza
: indirizzo al quale va trasferita la lunghezza ricercata
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro To
: porta all'indirizzo IIII il numero di cifre contenute nel
registro To dalla posizione iniziale al bit sT.
a) Se in p8 viene registrato il carattere 0 (zero), viene trasferito all'indirizze
III il numero delle cifre significative comprese tra la posizione iniziale del
registro T e il bit gT.
b) Se in p8 viene registrato il carattere. (punto), viene trasferito all'indiriz-
20 IIII il numero delle cifre significative e non significative comprese tra la po
sizione iniziale del registro To e il bit gT.
c) La lunghezza richiesta viene registrata sempre mediante 2 cifre.
d) Se richiedendo il numero di cifre significative (caso "a") non ne risultasse
cuna, vengono trasferiti all'indirizzo III e IIII-1, due zeri (00)
01 1 9.3.0 # 8
TRASFERISCE NO DELLE CIFRE SISNIFICATIVE CONTENUTE NEL REG. T
5.4,2,319,7 6 2
NO
109
SCHEMA RIASSUNTIVO
Istruzioni Memoria Registri
Trasferimento
Operazioni aritmetiche
Confronto
Determinazione lunghezza
MT
†MT
CMT
ETM
TM
+ TM
ToM
- MT
Particolarita' dei Registri
Posizioni
,° dei registri
200
10
Indirizzabilita'. di 5 in 5 posizioni indicando il nome del re
gistro.
Tabella nome registri:
01234567890ABCDEFGHI
E JKLMNOPOR. STUVWXYZ
Capacita' del singolo registro : 10 posizioni.
Modifica Automatica Istruzioni:
a) posizioni dell'istruzione interessata p7 p6 p5 p4 p3 ;
b) posizioni del registro interessato 5 4 3 2 1,
La modifica avviene sommando i caratteri del registro a quelli
della istruzione nelle posizioni suindicate senza riporto tra p6
e p7.
La somma nella 4ª posizione si effettua secondo una aritmetica in
base venti.
Il riporto di p7 si somma al carattere p8 dell'istruzione mentre
l'eventuale riporto di p8 si perde.
Bit gT: analogo al bit gA dell' accumulatore. Per il suo funzio-
namento vedere istruzione ner istruzione.
CODICE
SIMBOLICO
CANALI
IN PERIODI DI CIFRA
MT
сит
FTM
FTM
CON FIGURAZIONE
Tm
Im
CARAtTER
o o

## 7.4. - Istruzioni costanti-registri

Queste istruzioni interessano parole costituite da
caratteri o valori fissi (costanti): nel loro svol-
gimento impegnano 1' unita' aritmetica e logica ed il
governo dell' elaboratore.
Sia durante la fase preparatoria che in quella ese
cutiva il canale interno risulta impegnato; a que
ste istruzioni potranno percio' sovrapporsi opera-
zioni che impegnano il canale esterno ed il governo
unita a nastro.
Nella loro posizione p8 e' necessario registrare il
carattere & oppure # ; gli eventuali segni, piu' o
meno, vengono considerati caratteri qualsiasi.
Esse non possono subire modifica automatica ne' per
mettono l' introduzione nei registri T dei caratteri
tE e
sono normalmente utilizzate
a) per trasferimenti nei registri T di costanti di
lunghezza non superiore a 5 caratteri; ha questa
funzione 1' istruzione
ст
b) per somme o sottrazioni aritmetiche di lunghezza
non superiore a 5 caratteri: istruzioni di
gue-
sto tipo sono
+ СТ, - Ст, CTT
c) per confronti tra numeri aritmetici o parole al-
fanumeriche di lunghezza variabile da 1 a 5 ca-
ratteri; istruzione di questo tipo e' la
ССт
111
interno
Trasferisce una costante nel registro To
# C
c c c c
To
CI
9 (001100)
10
#
cc C C C
: posizione non utilizzata
•posizioni riservate alla costante da registrarsi nel re
gistro To
: registro in cui viene registrata la costante
trasferisce nel registro To la costante cCCCC registra-
ta nell'istruzione.
a) Il bit gT viene posto in corrispondenza della 5ª posizione del registro To•
b) Se nelle posizioni p7 e p8 è' registrato il carattere - il trasferimento avviene
solo per la costante CCCC ed il bit gl e posto in 4 posizione
X, 3 2,5,6,1 2,9
TRASFERISCE COSTANTE NEL REGISTRO T
SEGNO
13,2 5,6,1
# 5 # # 1,3 5,9
TRASFEPISCE COSTANTE NEL REGISTRO
15,0,0,1,3
REG. N.
REGISTRO PRIMA
DELL'ELABORAZION
24.00
SEGNO
112
tipo A
interno
Somma una costante a registro Io
c C C C
To
+ CT
+
(000101)
10
c c c c
To
: determinano il tipo d'istruzione
† CT
: costante da sommarsi al contenuto del registro To
registro su cui si opera
somma la costante cCCC al contenuto del registro To
a) Il bit gl si trova nel registro T, prima dell'istruzione in 5° posizione.
b) La somma viene effettuata tra i primi 5 caratteri del registro 1 e la costante
СССС
c) Il risultato e espresso per mezzo di 4 caratteri di cui il 4 puo' essere alfa
betico o speciale.
d) Il contenuto della 5ª Posizione del registro To rimane inalterato.
e) Non vi e indicazione di overflow.
f) Il bit gT viene posto in 4ª posizione.
g) Ponendo 0000 in CCCC e' possibile trasformare un indirizzo espresso con 5 carat
teri numerica 1n1 21 almente contenuto nel registro 1 in un indirizzo di 4 cara!
teri con le migliaia espresse nel modo corretto.
h) E' possibile percorrere tutti i successivi indirizzi di memoria.
889,0,0,01
SOMMA COSTANTE AL CONTENUTL
11.6.0.00
REGISTO0 POIA
DELLELABORAZION
1,1.0,0,0
112
tipo B
interno
Somma una costante a registro To
c c c c
+ CT
(000101)
10
c C с с
To
determinano il tipo di istruzione + CT
costante da sommarsi al contenuto del registro To
registro su cui si opera
: somma la costante cCCC al contenuto del. registro To
a, Il bit g† si trova nel registro o prima dell'istruzione in 4 posizione
b) La somma viene effettuata sui primi quattro caratteri del registro To•
c) Il 4° carattere puo' essere, o risultare dopo la somma, alfabetico o speciale
d) Non vi e' mai riporto sulla quinta posizione del registro To: ne' indicazione
di overtiow
e) Il bit gI rimane in 4ª posizione.
f) E' possibile percorrere tutti i successivi indirizzi di memoria
6: 90001+
DEI DESISTONI
11.0.0.0
11,10.0.0
114
tipo C
Somma una costante a registro Io
Ст
interno
#
#
cc c c
To
+
(000101)
10
# #
cC C c
To
determinano il tipo di istruzione + CT
: costante da sommarsi al contenuto del registro To
registro sn cui si opera
: somma la costante CCCC al contenuto del registro Io.
a) Il bit 8T si trova nel registro To prima dell'istruzione in 4ª posizione.
b) la somma viene effettuata sui primi quattro caratteri del registro T..
c) Non vi e' mai riporto sulla quinta posizione del registro To' ne' indicazione
di overflov
di Il bit &T viene posto in 5° posizione, ed in essa viene generato il carattere
0 (zero).
e) Non e' possibile percorrere tutti i successivi indirizzi di memoria non esister
do interazione tra parte numerica e parte alfabetica.
#9,0,0,01
SOMMA COSTANTE AL CONTENUTO
0,00,0,0
DELLELABORAZIONE
11,10.00
tipo D
Somma una costante a registro Io
ст
interno
# с
C C C C 1
T.
+
(000101)
10
#
To
: posizione non utilizzata
*: costante da sommarsi al contenuto del registro Io
: registro su cui si opera
somma la costante ccccc al contenuto del registro To.
a) La somma viene effettuata tra la costante CCCCC e il contenuto del registro 1
compreso tra la posizione iniziale e il bit gI
b) Nel caso vi fosse riporto oltre la quinta posizione del registro si ha indica
zione di overflow.
'c) Il bit gT dopo l'operazione viene sempre posto in 5ª posizione.
#0 9,0,0,01,+
SOMMA COSTANTE AL CONTENUTO
SEGNO
13,0,0,0.0
dopo
DELLE ABOPAZIONE
11,1,0,0,0
116
interno
Sottrae una costante a registro To
#
C C C c
To
СТ
4 (000100)
10
#
CC C C C
To
4
: posizione non utilizzata
•costante da sottrarsi al contenuto del registro Io
registro su cui si opera
sottrae la costante CCCCC al contenuto del registro To
a L'istruzione » CT puo' essere codificata anche nel seguenti modi:
# #
C C C C
To
C C C C
b) Il tipo con il carattere + in pl e p8 vale solo nel caso che, prima dell'istru-
zione. il bit T sia posto in 4ª posizione
c) Per l'istruzione - CT valgono le stesse osservazioni della + CT.
Esempio della nota b)
÷ : 7.5.0.01.
5,3,0,0
8.8.00
117
Sottrae registro o ad una costante, risultato in To
interno
#
TO
C C C C
I'm
#
(000110)
стт
14
#
To
C C C C
Im
#
: posizione non utilizzata
registro che contiene 11 sottraendo
: minuendo
puo' modificare sia CCCC che il nome del registro To
sottrae il contenuto delle prime quattro posizioni del
registro To alla costante ccCC modificabile da Im•
a) Il risultato della sottrazione e' nel registro To.
b) Il contenuto della quinta posizione di T. rimane inalterato ed il bit gT viene
in ogni caso posto in 4° posizione.
c) Per una corretta esecuzione della presenteistruzione e' necessario che in CCCC
e nel registro To non compaiano caratteri alfabetici o speciali
d) 19) Se Im + CCCC > 9999 il riporto oltre la 4ª cifra non viene considerato;
2°) Se Io > Im + CCCC in To si ha, a seguito dell'operazione, un risultato in
complemento
#2000.01
SOmPAL
•CONTENUTO DEL PEr
0.0.0.0
10,1,9,20
2 (
1.9 2 0
118
interno
Confronta una costante con registro To
#
C C C C
50
5
(001000)
10
#
To
5
: posizione non utilizzata
: 1° termine di confronto
: nel registro To e' registrato il secondo termine di con
fronto
: confronta la costante cCCCC al contenuto del registro
dall'inizio e fino al bit gT per un massimo di 5
To
posizioni.
a) Le regole del confronto sono le stesse della istruzione CMA ad eccezione per quel
che non vengono mai considerati come segni algebri
do che riguarda 1 segni
ci, ma come caratteri.
b) Se si desidera che il confronto non tenga conto di tutte le cinque posizioni del
la costante basta registrare il carattere # nelle posizioni che non interessano.
# 0 # 0 # 1 35
CONERONTOCOSTANTE COI
10001
119
SCHEMA RIASSUNTIVO
Istruzioni Costanti Registri
Trasferimento
Operazioni aritmetiche
Confronto
СТ
+CT
ССт
- Ст
СТТ
Particolarita' delle istruzioni su costanti
canice
SIMAOLICO
IMPEGNAYI
TEMPO
IN PEQIODI DI CIERA
Il registro specificato nella posizione p2 non opera come mo
di ficatore:
fa eccezione la CTT che ha in p2 il registro modifi
catore e in p7 il registro operando.
istruzioni di questo tipo non sono automaticamente modifica.
= 3 = = = 4
ст
interno
= 5
In corrispondenza di p8 va sempre messo il carattere
:
empo necessario all'esecuzione di un'istruzione di questo ti
periodi di cifra, esclusa la CTT alla quale ne sono ne
Do
ceccani
Bit gT : analogo al bit gA dell' accumulatore. Per il suo funzio
namento vedere istruzione per istruzione.
сст
O A =
PoRt0 0 71
CONFIGURAZIONE
• СС
22 a
To

## 7.5. Istruzioni per la moltiplicazione

Queste istruzioni interessano lamemoria principale,
i registri T e l' accumulatore; nel loro svolgimento
impegnano l' unita' aritmetica e logica ed il gover-
no dell' elaboratore.
Sia durante la fase preparatoria che in quella ese
cutiva il canale interno risulta impegnato; a que-
sto gruppo di istruzioni potranno percio' sovrappor
si operazioni che impegnano il canale esterno ed il
governo unita' a nastro.
Esse sono normalmente utilizzate :
a) per il trasferimento nella memoria dei registri
T. a partire dalla posizione 00' e per indiriz-
zi crescenti, del moltiplicatore, per lunghezza
conosciuta o sconosciuta variabile da 1 a 100 ca
ratteri; 1' eventuale segno algebrico va a posi.
Zionarsi in un apposito registro del segno;
na
questa funzione l'istruzione
b) per sommare o sottrarre, automaticamente, il ri-
sultato della moltiplicazione al contenuto del-
1' accumulatore; questa funzione e' propria del-
le istruzioni
+ X,
interno
Trasferisce il moltiplicatore nei registri T
LL
IIII
Im
6
(001001)
10
LL
III I
Im
6
: lunghezza del moltiplicatore contenuto in memoria
: indirizzo in memoria del moltiplicatore
: il registro Tm puo' modificare sia l'indirizzo IIII che
la cifra delle unita' della lunghezza LL
: trasferisce la parola contenuta in memoria all'indiriz-
Zo IIII per lunghezza LL nei registri Tapartire da TO.
a) La cifra meno significativa della parola occupa la posizione iniziale 0 del regi
stro 10 e successivamente in ordine progressivo vengono occupate le altre posizio
b1 Possono essere eventualmente invase tutte le posizioni del gruppo di registri com
presi tra 10 e TI.
c) La lunghezza della parola puo' essere al massimo eguale a 100 (LL = 00).
d) Se la parola e' segnata il segno non viene registrato nella prima posizione
TO, ma in un apposito registro.
di
e) Se la parola non e' segnata e non supera lunghezza 10 l'istruzione Y puo'
esseg
sostituita con una qualsiasi delle istruzioni relative ai registri I
f) Per questa istruzione valgono le regole relative ai casi di fine su carattere chia
ve, nel caso di trasterimento lungo piu' di 90, non deve essere usato il registrc
T9.
Nei due esempi che seguono, il moltiplicatore viene trasferito nei registri T tram
tele istruzioni Y ed MT
Come si puo' osservare e' possibile ottenere il trasferimento del segno nell'apposi
to registro solo mediante l'istruzione y
122
11.2 1.9.3.2 # 6
TRASFERISCE DA MEMORIA MOLTIPLICATORE
DALL'INDIRIZZO
5 3 61.27.89
3 0 1.9.3.2 #,X
DALL'T
8.9
122 b.

Moltiplicazione addittiva
interno
T.T.
IIII
Im
=
(010101)
+ X
10
† n0
cifre
Mol.rex(3+1)
LL
IIII
Im
: lunghezza del moltiplicando
indirizzoin memoria del moltiplicando
:il registro Im puo' modificare sia 1' indirizzo IIII
che la cifra delle unita' della lunghezza LL
: somma al contenuto dell' accumulatore il risultato del-
la moltiplicazione.
a) La moltiplicazione viene effettuata tra il contenuto della memoria a partire dal
l'indirizzo IllI e per lunghezza LL, e il contenuto dei registri dalla posizione
o fIo, fino al primo bit gI
b) Il contenuto della memoria e dei registri rimane inalterato.
'c) Affinche' il risultato sia segnato è sufficiente che lo sia il contenuto della
memoria o quello dell' accumulatore
d) Non è' sufficiente che sia segnato solo il moltiplicatore.
e) Per questa istruzione valgono le regole relative ai casi di fine su carattere
chiave.
0 5 1 9 3.2 #=
00000
MEMORI
RISULTATO
4 9 0
2,0
2 0-
123
Moltiplicazione sottrattiva
interno
L
L
IIII
Im . , (011101)
X
10 +п°
ci fre
Mol.re x (3+1
LL
IIII
Im
: lunghezza del moltiplicando
: indirizzo in memoria del moltiplicando
: il registro Im puo' modificare sia l'indirizzo IIII
che le cifre delle unita' della lunghezza LL
: sottrae al contenuto dell' accumulatore il risultato
della moltiplicazione,
a) Per l'istruzione - X valgono le osservazioni fatte per la +X.
0 5 1.9.3.2 #
SOTTRAE ALL'ACCUMULATORL
000.00
• MEMO
1.9
0000
124
SCHEMA RIASSUNTIVO
Istruzioni di Moltiplicazione
Trasferimento
Moltiplicazione
+X
*
Particolarita' della moltiplicazione
CODICE
SIMBOLICO
CANAL
CONFIGURAZIONE
IN PERIODI DI CIERA
De fasi.
Registrazione del moltiplicatore : istruzio-
ne Y
Esecuzione vera e propria : istruzione
-X .
AX,
La moltiplicazione viene eseguita tra due numeri segnati o non
segnati dei quali uno (il moltiplicatore)con
tenuto nei registri T a partire da TO, e l'al
tro (il moltiplicando) in una posizione qual
aiosi di memoria.
Il trasferimento
Il risultato
del moltiplicatore in TO deve necessariamen-
te farsi con la Y solo quando e' un numero
segnato o di lunghezza maggiore di 10.
viene sommato o sottratto al contenuto del-
la accumulatore.
+1 tempo
richiesto per la fase esecutiva delle istru-
L (3 + 1)
il numero delle cifre del moltipli
catore ed 1 il numero delle cifre del moltit
plicando.
interno
10 +(3+1) L
10 +(3+1)L L LILI
'Im
os

## 7.6. Istruzioni per la ricerca in memoria

Le istruzioni di ricerca interessano la memoria prin
cipale; nel loro svolgimento impegnano l'unita' arit
metica e logica ed il governo dell' elaboratore.
Sia nella fase preparatoria che in quella esecutiva
il canale interno risulta impegnato. A questo grup-
po di istruzioni potranno percio' sovrapporsi istru-
zioni interessanti il canale esterno ed il governo
unita' a nastro.
Queste istruzioni consentono di trovare
1'indirizzo
della posizione di memoria che contiene un carattere
determinato oppure un carattere appartenente ad
1in a
classe fissa, e di ricordarlo in un registro T.
La ricerca viene effettuata da una posizione inizia-
le di memoria, procedendo sia per indirizzi crescen-
ti (RIa) sia per indirizzi decrescenti (RIi).
L'indirizzo della posizione di memoria contenente il
carattere ricercato viene registrato nelle prime quat
tro posizioni del registro T9.
La ricerca avviene confrontando il contenuto della me
moria con il carattere posto in R.
Di questo carattere possono essere interessati dal
confronto tutti o parte dei bit.
Il numero e la posizione dei bit da confrontare ven-
gono allora determinati dai bit 1 di un secondo
ca.
rattere posto in c.
Se ne deduce che se il carattere posto in C
p'
Q
(111111) tutti i bit di R vengono confrontati con i
bit dei caratteri esistenti in memoria, e che un so..
lo carattere puo' dare eguaglianza nel confronto: il
carattere identico ad R.
126
Se invece il carattere posto in C e' diverso da Q,
per l'esclusione di almeno un bit dal confronto, si
crea un gruppo di caratteri pari alla potenza di 2
elevato ad esponente uguale al numero dei bit o di c
fedcb
Esempio: In p8 sia posto il carattere F (0 1100 1)
e in p7 sia posto il carattere € (1 10000)
La macchina ricerchera' un carattere che abbia i
bit "e" ed fr rispettivamente uguali a "i" e "0".
Il numero dei caratteri aventi queste caratteristi
che e' 24
= 16
127
Ricerca avanti
RIa
interno
R C
IIII
Im
2 (000011)
15 + 1
R
: carattere o classe di carattere ricercati
: carattere che condiziona i bit di R interessati dalla
ricerca
IIII
: indirizzo da cui si inizia la ricerca
ricerca a partire dall'indirizzo IIII e procedendo per
indirizzi crescenti l'indirizzo della prima posizione
di memoria nella quale sia registrato un carattere ap.
partenente alla classe individuata da R e C.
a) L'indirizzo della posizione di memoria contenente il carattere ricercato viene rt
gistrato nelle prime quattro posizioni del registro T9.
b) Se 11 carattere ricercato si trova all'indirizzo TITT indicato nella istruzione
Viene registrato in T9 l'indirizzo IIII.
c) Se il carattere posto in C e' Q (lllll1), tutti i bit intervengono nella ricerc
e viene quindi cercato solo il carattere posto in R
d) Se il carattere posto in C e' diverso da Q, si ricerca una classe
caratteri
che abbiano in comune i bit corrispondenti indicati da C.
e) Il carattere "" indicato nella casella riservata alla durata dell'istruzione si
riferisce al numero di caratteri confrontati prima di raggiungere quello desiderato.
Ricerca indietro
RIi
interno
RC
I I I I
Im
7 (001011)
15
R
carattere o classe di caratteri ricercati
: carattere che condiziona i bit di R interessati dalla
ricerca
: indirizzo da cui si inizia la ricerca
: ricerca a partire dall'indirizzo IIII e procedendo per
indirizzi decrescenti l'indirizzo della prima posizio
ne di memoria nella quale sia registrato un carattere
appartenente alla classe individuata da Re C.
a) Valgono le osservazioni fatte a proposito della Ria.
128
SCHEMA RIASSUNTIVO
Istruzioni di Ricerca
Istruzioni
RIa
RIi
Particolarita' istruzioni di ricerca
CODICE
SIMBOLICO
CANALI
IMOGENATI
TElDa
IN PEDIODI DI CIERA
Funzione
consentono di determinare l'indirizzo della posizio
no di memoria che contiene un dato carattere o un ca
rattere appartenente ad una classe fissata: lindi.
rizzo del carattere al trasferito nel registro T9
RIa interno
Ta ricerca viene effettuato da una posizione iniziale per indi
pinne cresconti o decroscenti.
la ricerca viene eseguita confrontando il contenuto della memo
ria con il carattere posto in p8 dell'istruzione:
vengono interessati dal confronto soltanto i bit cor
rispondenti a quelli che nel carattere posto in pi
sono uguali ad 1.
Tempo
15 + 1 periodi di cifra dove l e il numero di
co.
ratteri confrontati prima di raggiungere quello de.
siderato.
RIi
CONFIGURAZIONE

## 7.7. Le istruzioni per le operazioni logiche

Il calcolatore e' capace di eseguire operazioni lo-
giche, bit per bit, secondo 1' algebra di Boole, fra
un operando proveniente da memoria e un altro prove
niente da un registro T.
L'operazione puo' eseguirsi sia tra i bit diretti,
sia tra i bit "negati che si ottengono prendendo i
bit componenti un carattere e scambiando gli 1
coT
o e gli 0 con 1.
Cosi' ad esempio del carattere F i bit diretti sono
011001, i bit negati sono 100110.
La lunghezza degli operandi nelle operazioni logi-
che non puo' essere superiore a 10.
Anche queste istruzioni possono operare su dati di
lunghezza sconosciuta con fine determinabile da pa-
rola chiave; sono pero' previsti solo i due casi di
fine su segno o carattere alfabetico.
Il carattere indicativo del tipo di fine, deve esse
re specificato nella posizione p8 dell'istruzione
E' evidente che se l'istruzione comporta l'uso del
T9 non e' possibile la fine con trasferimento del-
l'indirizzo della parola chiave. Occorre pure ricor
dare che queste istruzioni hanno significato se la
lunghezza e' ≤ 10; quindi il segno o carattere al
fabetico non deve trovarsi in memoria oltre la deci
ma posizione toccata.
Si tenga pero' conto che se la parola del registro
e' piu' corta di quella di memoria si ha fine prima
della comparsa del carattere chiave, e in T9 si tra
sferisce eventualmente l'indirizzo dell'ultimo ca-
rattere di memoria operato.
130
Se invece la fine avviene per il carattere specia-
le, l'ultimo periodo operativo e' precedente alla
comparsa di detto carattere. Nel periodo del carat-
tere chiave si ha scrittura in T di un zero con pal
linaccio (g).
131
interno
Moltiplicazione logica diretta
L
To
IIII
Im ! (100101)
XLD
10 + 1
L
: lunghezza degli operandi
To
: registro in cui si trova il secondo operando
IIII
: indirizzo di memoria del primo operando
:il registro Tm puo' modificare sia l'indirizzo IIII che
il nome del registro operando To
: effettua la moltiplicazione logica, bit per bit tra i
bit diretti dei caratteri costituenti la parola conte-
nuta in memoria di lunghezza L ed i bit diretti dei ca
ratteri contenuti nelle prime L posizioni del registro
To'
a) Il risultato si forma in To•
) Il contenuto della memoria rimane inalterato.
c) Le regole secondo le quali si esegue la moltiplicazione logica diretta sono date
dalla seguente tabella:
2°
d) Per questa istruzione valgono le regole relative ai casi di fine carattere chia
ve.
132
interno
Moltiplicazione logica negata
To
I I I I
Im
&
XLN
(101101)
10 +1
L
To
IIII
Im
: lunghezza degli operandi
registro in cui si trova il secondo operando
: indirizzo di memoria del primo operando
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro operando To
: effettua la moltiplicazione logica bit per bit, tra i
bit negati dei caratteri costituenti la parola contenu
ta in memoria e di lunghezza L e i bit negati dei ca-
ratteri contenuti melle prime L posizioni di To'
a) Il risultato si forma in lo°
b contenuto della memoria rimane in alterato
c) Le regole secondo le quali si esegue la moltiplicazione logica negata sono date
dalla seguente tabella
1°
d rer questa istruzione
annave
regol relative ai casi di fine su carattere
133
Somma logica diretta
interno
L
II I I
Im
V (100100)
+ LD
10 + 1
To
IIII
Im
: lunghezza degli operandi
: registro in cui si trova il secondo operando
indirizzo di memoria del primo operando
: puo' modificare sia l'indirizzo IIII che il nome del
registro operando To
: effettua la somma logica, bit per bit, tra i bit diret
ti dei caratteri costituenti la parola contenuta in me
moria e di lunghezza L ed i bit diretti dei caratteri
contenuti nelle prime L posizioni del registro Io.
a) Il risultato si forma in 1.
b I contenuto della memoria rimane inalterato.
c) Le regole secondo le quali si esegue la somma logica diretta sono date dalla se
guente tabella :
20
1°
d) Per questa istruzione valgono le regole relative ai casi di fine su caratter
cnsave
SCHEMA RIASSUNTIVO
Operazioni logiche
Somma
Moltiplicazione
+ LD
XLD
XI.N
Particolarita' delle operazioni logiche
CODICE
SIMBOLICO
IMPEGNATI
TEMPO
IN PERIODI DI CIFRA
Oper andi
Operazioni
: uno in memoria e uno in un registro T.
secondo l'algebra di Bole bit per bit: le ope.
razioni possono avvenire sia tra bit diretti che
tra bit negati.
XLD
interno
10 +1
XLN
Bit diretti .bit operati con il valore attuale nella configu
orione del carattere.
+LD
Bit negati : ottenuti dai bit diretti invertendo il valore de
gli "1" con non e degli "on con
Lunghezza de
gli operandi ': non puo' essere superiore a 10.
Risultato :nel registro T. gia' contenente uno degli ope-
candi.
CONFIGURAZIONE
CARATTERE
Im

## 7.8. Istruzioni relative al tavolo di comando

Queste istruzioni possono interessare con la memo
ria principale o il fotolettore o la telescrivente;
durante il loro svolgimento impegnano l'unita' arit
metica e logica ed il governo dell' elaboratore.
Appartengono a questo gruppo
le istruzioni CM (da telescrivente o fotolettore a
memoria), MS (da memoria a telescrivente).
La CM, sia durante la fase preparatoria che in quel
la esecutiva, tiene impegnato il canale interno; a
questa istruzione potranno percio' sovrapporsi ope
razioni che impegnano il canale esterno ed il
verno unita' a nastro.
La MS impegna il canale interno per tutto il tempo
richiesto dalla fase preparatoria; durante la fase
esecutiva invece quest'ultimo viene impegnato dal-
l'istruzione ogni settimo di secondo per il tempo
necessario al trasferimento di un carattere.
Le istruzioni di questo gruppo sono normalmente u-
tilizzate:
a) per introdurre nella memoria principale, median
te telescrivente, parole di lunghezza variabile
da 1 a 100 caratteri, oppure mediante fotoletto
re, parole di lunghezza qualsiasi;
b) per estrarre dalla memoria principale, mediante
telescrivente, parole di lunghezza variabile da
1 a 100 caratteri.
136
interno
Da tavolo di comando o da fotolettore a memoria
L
L
I I I I
Im
%
(011010)
CM
10
LL
IIII
Im
: lunghezza dell'informazione da trasferirsi in memoria
: indirizzo a partire dal quale i caratteri registrati ven
gono trasferiti in memoria
: il registro Im puo' modificare sia l'indirizzo IIII che
la cifra delle unita' di LL
: legge da tastiera o da fotolettore verso memoria,
a) La scelta fra tastiera e fotolettore e' fatta mediante la chiave TAST - FL posti
sul tavolo al comando.
b) La lettura da tastiera avviene per LL caratteri via via che i rispettivi
vengono premuti.
tasti
caTettura da totoettore avviene
1) per un numero di caratteri pari a quello indicato in LL:
2) ponendo ## al posto di LL la lettura avviene per tutti i caratteri registra
ti su banda perforata fino al primo carattere o (che viene anch'esso registra
to in memorial.
d) Sono previsti anche per questa istruzione i due casi di fine su carattere chiav
(non si ha pero' trasferimento in T9 dell'indirizzo del carattere chiave).
e) Il senso di registrazione in memoria e' per indirizzi crescenti
) Il tempo indicato nella casella della durata dell'istruzione si riferisce solo al
la fase preparatoria; la fase esecutiva avviene alla velocità' di 800 caratteri
al secondc
137
Trasferisce da memoria a telescrivente
MS
interno
LL
fILI Im 0 (010000)
10
L L
IIII
Im
: lunghezza dell'informazione da stampare
: indirizzo di memoria in cui e registrato il 1° caratte
re da trasferire
:il registro Im puo' modificare sia l'indirizzo IIII che
la cifra delle unita' della lunghezza LL
: scrive con la telescrivente LL caratteri a partire da
quello che si trova all'indirizzo IIII e per indirizzi
crescenti,
a) Nello svolgimento del programma in cui e' posta l'istruzione si intercalano pe-
riodi di telescrivente, in ognuno dei quali si comanda la stampa di un caratte-
re letto in memoria.
b) Alla fine del trasferimento si esegue automaticamente un ritorno carrello e in-
terlinea; se LL e' maggiore di 72, si torna automaticamente a capo.
c) Se durante l'esecuzione di questa istruzione viene eseguito lo STOP, questa non
Viene interrotta ma prosegue fino alla fine.
d) Il tempo indicato nella casella della durata dell'istruzione, si riferisce alla
fase preparatoria; la fase esecutiva avviene alla velocita' di 7 caratteri al se
condo
138
SCHEMA RIASSUNTIVO
Istruzioni relative al tavolo di comando
Trasferimento
См
MS
Particolarita' istruzioni relative al tavolo di comando
CODICE
SIMBOLICO
CANALI
IN PERIODI DUCIERA
Funzione
consentono di introdurre o di estrarre dei dati
in o da memoria principale.
L'introduzione : puo' avvenire tramite latelescrivente per un mas
simo di 100 caratteri, oppure per mezzo del fo-
talattore fino al primo carattere o perforato
su nastro.
см
intern
L'estrazione : avviene solo mediante telescrivente per un nume
ro di caratteri non superiore a 100.
uS
Tempo
10 periodi di cifra per la fase preparatoria: la
fase esecutiva viene eseguita alla velocita'
800 caratteri al secondo ner la CM, usando il fo
tolettore. e di 7 caratteri al secondo ner la MS
CONEIGURAZIONE
Im
a

## 7.9. Istruzioni di salto

La successione delle istruzioni di programma puo' do
ver essere alterata al verificarsi di certe eventua
lita'. A questo scopo servono le istruzioni di sal.
to, il cui carattere di funzione e' 0 (zero), che agi
scono sul registro indirizzo istruzioni.
Al leggere una istruzione di salto il calcolatore de
a) esaminare se si e' o no verificata una determina
ta eventualita'.
Questa viene indicata al calco-
latore per mezzo del carattere p8, che serve dun
que a distinguere un' istruzione di salto da una
altra, e che in seguito sara indicata con lalet
tera E. Se la eventualita' in esame non si e' ve
rificata il calcolatore esegue l'istruzione imme
diatamente seguente l'istruzione di salto; si di
ce allora che il salto non e' stato eseguito;
b) se la eventualita' osservata si e' verificata, ese
guire l'istruzione di indirizzo IIII (modificabi
le da Tm) indicato dalla istruzione di salto. si
dice allora che il salto e' stato eseguito;
c) ricordare, se necessario, l'indirizzo dell'istru
zione di salto, per ritornare al programma da cui
si e' saltati, dopo aver eseguito altre istruzio
ni. Tale necessita' si presenta quando una stes-
sa sequenza di istruzioni (o sottoprogramma) puo'
essere chiamata da diversi punti del programma
principale. In p7 della istruzione di salto side
ve allora indicare il registro Is in cui si desi
dera venga ricordato l'indirizzo dell'istruzione
stessa; in Ts viene registrato, per la precisio-
ne, l'indirizzo in memoria del carattere p8 di ta
le istruzione, e solo nel caso che il salto sia
stato eseguito.
140
Hanno questa funzione le seguenti istruzioni:
SC=, SC # , SC>, SC<, SR=, SR*, SA=, SA>, SA<, SOM,
STO, SEj, SEz, SEg, SEq, SI, SIN, SN, STOP.
141
Salta se uguale da confronto
SC =
interno
(101001)
X Is
IIII Im 0
10 o 15
a) Salta se nell'ultimo confronto, eseguito per conto del programma in cui la istr
zione
posta, la memoria e' risultata uguale al secondo termine di conironto.
interno
Salta se diverso da confronto
(101011)
Y. Is
III I
SC#
I'm
10 o 15
a) Salta se nell'ultimo confronto, eseguito per conto del programma in cui la istru
zione
posta, la memoria e risultata diversa dal secondo termine di confronto
142
interno
Salta se maggiore da confronto
(100001)
s'Is
III I
sc'>
I'm 0
10 0 15
a Salta se nel ultimo contronto.
eseguito per conto del programma in cui la istru,
Zione e posta, la memoria e risultata maggiore del secondo termine di confron
co.
b) Nel caso di conironto tra due zone di memoria operazioni PUM, MM, salta se
risultata maggiore la zona di memoria specificata dalla M
Salta se minore da confronto
Sc'<
interno
(100011)
T
Is
I I I I
Im 0
10 o 15
a) Salta se nell'ultimo confronto, eseguito per conto del programma in cul la istru
zione e posta, la memoria e risultata minore del secondo termine di confronto.
b) Nel caso di confronto fra due zone di memoria (operazioni PUM, CMM), salta se
risultata minore
zona di memoria specificata dalla CM.
143
Salta se il Risultato e' uguale a zero
SR
interno
(100010)
Is
IIII Im 0
10 0 15
a) Salta se e' uguale a zero il risultato dell'ultima istruzione, eseguita per con
to del programma in cui l'istruzione di salto e' posta, del tipo
+X
-X, MA, MT, +MT, -MT, XLD, XIN, +LD, +CT, -CT, CT, +MM,
-MM, Y, +AM, +TM.
b) Per risultato di una istruzione MA, MT, CT, Y si intende l'informazione trasferi
ta da dette istruzioni.
c) L'indicazione di risultato uguale a zero e' annullata, oltre che dalle preceden.
ti istruzioni,
anche dalla Aoe To.
interno
Salta se il Risultato e' diverso da zero
(100000)
Is
IIII Im 0
SR $
10 0
15
Salta se e' diverso da zero il risultato dell'ultima istruzione, eseguita per co
to del programma in cui l'istruzione di salto e posta, del tipo †MA, +^, -MA
-X, MA, MT, +MT, -MT, XLD, XI.N, +LD,
+CT, -CT,
CT, +MM,
+AM,
b) Per risultato di una istruzione MA, MT, CT, Y si intende 1' informazione
tra.
sterita da dette istruzioni.
c) L'indicazione di risultato diverso da zero e' annullata, oltre che dalle prece
denti 1struzioni, anche dalla AM e ToM
144
Salta se l' Accumulatore e' uguale a zero
SA= 0
interno
(100100)
Is
IIII
Im 0
10 0 15
a) Salta se, a seguito dell'ultima istruzione eseguita del tipo +MA, +X,
- MA,
- X, MA, 1' accumulatore è' risultato uguale
a zero
b) L'indicazione di accumulatore uguale a zero viene annullata quando si esegue una
successiva istruzione del tipo anzidetto o una istruzione AM.
Salta se l' Accumulatore e' maggiore di zero
SA > 0
interno
(100111)
y Is
I I I I
Im 0
10 0 15
a) Salta se, a seguito dell'ultima istruzione eseguita del tipo + MA,
- X, MA, ]' accumulatore è'
+X,
.MA,
risultato maggiore di zero.
b) L'indicazione di accumulatore maggiore di zero viene annullata quando si esegue
una successiva istruzione del tipo anzidetto o una istruzione AoM.
Salta se 1' Accumulatore e' minore di zero
SA '<O
interno
(101000)
w
Is
II I I
Im 0
10 o 15
a) Salta se, a seguito dell'ultima istruzione eseguita del tipo
a X, MA. ' accumulatore e' risultato minore di zero.
+ MA,
+X,
. MA,
b) L'indicazione di accumulatore minore di zero viene annullata quando si esegue una
successiva istruzione del tipo anzidetto od una istruzione AoM
145
interno
Salta se vi e' stato Overflow in Memoria
(101100)
Ts
IIII
SOM
I'm 0
10 0 15
a) Salta se si e' avuto overflow in memoria a seguito dell'ultima istruzione
ese.
guita per conto del programma in cui l'istruzione di salto e' posta, del
C1Dc
"MM, +AM, +IM
b) Le condizioni che provocano il segnale di overflow sono specificate istruzione
per iscruzione
Salta se non vi e' stato Overflow in registro T
STO
interno
(101111)
Z Is
Im 0
10 o 15
a) Salta se non si e' avuto overflow nel registro T operato dalla ultima istruzio
ne, eseguita per conto del programma in cui l'istruzione di salto e' posta, del
tipo +MT, -MT, +CT, -CT.
b) Le condizioni che provocano il segnale di overflow sono specificate istruzione
per 1struzione
146
interno
Salta su condizione esterna 1
(111110)
T
Is
IIII
Im 0
SE1
10 0 15
a) Salta su condizione esterna l. L'esecuzione del salto e' subordinata al posizio
namento della levetta l posta sul tavolo di comando. Il posizionamento viene ef-
fettuato manualmente dal operatore.
interno
Salta su condizione esterna 2
(111010)
Is
III I Im 0
SE2
10 0 15
a) Salta su condizione esterna 2 . Come SE per levetta 2
Salta su condizione esterna 3
interno
(100101)
Is
IIII Im 0
SE3
10 0 15
a) Salta su condizione esterna 3 . Come SE per levetta 3 .
interno
Salta su condizione esterna 4
(101101)
Is
I I I I
Im 0
SBA
10 0 15
a) Salta su condizione esterna 4 . Come SE- per levetta 4
147
Non salta
(In 7
SN
interno
(111100)
RIs
XX x x
Im 0
10
a) Non salta mai, ma immagazzina nel registro Is l'indirizzo del carattere p8 della
istruzione.
b) Le posizioni p3 : p6 non vengono prese in considerazione.
interno
Salta incondizionatamente
(100110)
Ts
SI
IIII Im 0
15
a) Salta in qualsiasi caso.
148
Salto invariante
SIN
interno
(100110)
)
cC C c
Is
19
a) Questa e' diversa dalle altre istruzioni di salto, in quanto non indica l'indiriz
zo della prossima istruzione da eseguire, ma l' addendo CCCC (non modificabile) di
sommare al contenuto del registro indirizzo istruzioni
b) Si noti che :
1) il suo carattere di Funzione non e' zero. ma ~ (approssimato);
2) non vi e' registro 1m modificatore; in p2 e pl deye essere indicato il medesi.
mo registro
3) in
1s contrariamente agli altri salti viene immagazzinato l'indirizzo di p2 del
l'istruzione.
c) Per effettuare un salto ad una istruzione registrata M istruzioni oltre la SIN,
in CCCC si deve porre un numero uguale
(8 M) + 1
Dovendo ad esempio eseguire la terza istruzione oltre la SIN, si avr
СССС = 0008 . 3 ÷ 0001 = 0025
d) Il registro 1s deve sempre essere indicato
e) Il tempo di esecuzione e' di 19 periodi di cifre anziche' di 15
Arresto
STOP
interno
(111001)
X
X X X X
# 0
10
a) Pone termine allo svolgimento del programma nel quale l'istruzione e' posta
b) Se l'istruzione e' posta nel 1° programma, questo ha termine, mentre lo svolgimen
to del 2° programma puo' proseguire.
c) Se si ha lo STOP nel 2° programma, questo ha termine mentre il 1° programma puo'
proseguire
d) L'istruzione STOP non arresta l'esecuzione della istruzione MS eventualmente in
corso
149
SCHEMA RIASSUNTIVO
Salti su confronti
Salti su risultati
Salti su contenuto accum.
Salti in overflow
Salti su condizioni est.
Salti- speciali
SC=
SR=
SA=
SOM
SEj
SI
SCt
SR+
SA >
STO
BIS
SN
Particolarita' dei salti
Istruzioni di salto
sC'>
SA'<
SEg
SIN
CODICE
SIMBOLICO
IMPEGNATI
SCk<
SEA
STOP
TEMPA
IN PERIODI DI CIERA
Funzione
Eventualita
alterare la successione delle istruzioni di pro
gramma 'se e' verificata una certa eventualita'.
viene indicata all' elaboratore per mezzo del ca
rattere p8 dell'istruzione di salto.
Registro Ts
ricorda l'indirizzo del carattere p8 dell'istru
zione di salto solo nel caso che il salto venga
eseguito.
Salta, se l'eventualita
verificata, all'istruzione di indi
rigo TITT indicato nell'istruzione di salto.
Tempo di esecuzione':
15 periodi di cifra.
Non salta, se l'eventualita' non si è' verificata, ed esegue l'i-
struzione immediatamente successiva del program
ma.
Tempo di esecuzione': 10 periodi di cifra.
SC=
sC*
SC'>
SC'<
SR=
SRA
SA=
SA'>
SA'<
SOM
STO
SEy
SE2
SEg
SEA
ST
SN
SIN
STOP
interno
10 o
10
10 o
10 o
15
15
10
15
10 o
15
10 0
15
x
CONFIGURAZIONE
Im
yyyy
racc
X х х х

## 7.10. Istruzioni di salto su errore

La probabilita' di un errore nel movimento di un ca-
rattere tra i vari organi dell' elaboratore e' estre-
mamente piccola.
E' tuttavia indispensabile cautelarci anche contro
questa evenienza con appositi dispositivi di macchi-
na che segnalino il verificarsi dell'errore.
Questi segnalatori nell' Elea 9003 esistono di fatto
ed i loro segnali sono rilevabili mediante apposite i
struzioni di salto.
Dette istruzioni inserite opportunamente nel program
ma permettono di ricorrere a programmi di correzione
ogni qualvolta si verifichi un errore nel corso di u
na elaborazione.
Tale errore evidentemente non puo' essere di natura
logica o imputabile ad inesattezze, a inversioni
o
scambi di dati, o a difetti di quadratura, rilevabi-
li e correggibili con tecniche di altro genere.
Gli errori in questione possono essere imputati esclu
sivamente all' imperfetto funzionamento dell' elabora-
tore in un determinato caso.
151
Salta se errore qualsiasi
SE
interno
(110110)
Is
IIII
Im 0
10 o 15
a) Salta se e' stato commesso un errore qualsiasi
b) Oltre agli errori rilevati dai salti su errore del tipo SEMI, SEUM, SEME,
SEU, SEN, SEL, rileva se vi e' stato errore nel lettore fotoelettrico
di
perforata, collegato al tavolo di comando.
SEA,
bande
c) Se l'istruzione SE rimanda ad una istruzione che non sia di salto, la
segn al a.
zione di errore qual si asi
viene annullata.
interno
Salta se errore in uscita da memoria
(110000)
E
Is
IIII
SEUM
Im
10 0 15
a) Salta se e stato rilevato un errore nell'estrazione dalla memoria attraverso i.
canale interno.
b) La
rilevazione dell'errore avviene per mezzo del controllo di disparita
152
interno
Salta se errore in memoria, canale interno
(110010)
* Ts
IIII
SEMI
Im 0
10 0 15
a) Salta se e' stato rilevato un errore nella introduzione in memoria attraverso il
canale interno.
b) La rilevazione dell'errore avviene per mezzo del controllo di disparita'
interno
Salta se errore in memoria, canale esterno
(110001)
J
Is
IIII
SEME
Im 0
10 o 15
a) Salta se e' stato rilevato un errore nella introduzione in memoria attraverso il
canale esterno.
b) La rilevazione dell'errore avviene per mezzo del controllo di disparita
153
interno
Salta se errore in accumulatore
(110011)
K
Is
IIII
Im 0
SEA
10 o 15
a) Salta se e' stato rilevato un errore nella estrazione dall'accumulatore.
b) La rilevazione avviene per mezzo del controllo di disparita'
interno
Salta se errore in unita' aritmetica
(110111)
LIs
III I
I'm 0
SEU
10 o 15
a) Salta se l'unita' aritmetica e logica ha commesso un errore.
b) La rilevazione puo' avvenire per mezzo
1) del controllo di disparita
2) della prova del 3 ;
3) o dalla presenza di configurazioni speciali in operazioni aritmetiche.
interno, GUN
Salta se errore in unita' a nastro magnetico
(110100)
M
Is
I I I I
Im 0
SEN
10 o 15
a) Salta se una unita' a nastro magnetico ha commesso un errore
b) La rilevazione avviene per mezzo del controllo di disparita
c) Per le unita' che registrano in avanti la rilevazione avviene inoltre per mezzo
del controllo di registrazione per rilettura e confronto.
d) L'istruzione non viene eseguita se e' in corso una eventuale operazione
stro
dl na
154
SCHEMA RIASSUNTIVO
Istruzioni
SE
SEMI
SEUM
SEME
Particolarita' dei salti su errori
Funzione
controllo della corretta elaborazione delle
informazioni; il salto viene eseguito se
10
orrore si al verificato.
Caratteristiche'.
'indicazione di un tipo di errore viene
seryata dal'istante in cui
si
rileyato fino alla fine della esecuzione del
¡Piatenniono di colto di col tipo di erro-
re, oppure fino alla esecuzione di una istru
ione di salto relativa a piu° tipi di erro-
che compare in queste istruzioni e' general-
mente l'indirizzo della prima istruzione
un sottoprogramma di segnalazione di errore
o di correzione di errore.
Per le istruzioni
SCA e SE la prima istruzione del sottoprogram
ma elaborativo deve gasare necessariamente
un'istruzione di salto,
Salti su errori
SEA
SEU
SEN
SEL
CODICE
SIMBOLICO
CANALI
IMPEGNATI
IN PEGIONI DI CIERA
CONFIGURAZIONE
SE
SEMI
SEUM
SEME
SEA
SEU
SEN
SEL
interno
int. GUN
int. uni-
ta'linea
10 o 15
§ Is
10 o 15
10 o 15
10 o 15
10 o 15
10 o 15
10 o 15
Ts
TE
Is
Is
Ts
=
.45
10 0 15
Im
CARATTERE

(o'
UNITA' A NASTRO MAGNETICO FR - 400 .-
