```{sectnum}
---
start: 8
---
```

# Utilizzazione dei nastri magnetici

## Caratteristiche generali

Il nastro magnetico come supporto d'informazione per
l'elaborazione elettronica dei dati e' certamente il
piu' funzionale : e' veloce, facilmente trasferibi-
le, garantisce la buona conservazione dei dati ed e'
poco costoso.
Puo' essere usato un numero illimitato di volte sia
per la lettura dei dati in esso immagazzinati che
per la registrazione di nuove informazioni su quel-
le preesistenti.
Viene avvolto su bobine che possono essere conserva
te col minimo ingombro portando ad economia di spa-
zio molto rilevanti.
La durata di una registrazione e' in pratica illimi
tata, e i dati sono molto meno soggetti ad altera-
zioni che su altri supporti.
Le operazioni eseguibili su nastro magnetico sono
la registrazione di informazioni,
la lettura delle informazioni gia' registrate.
L'esecuzione di dette operazioni e' affidata ad una
apposita apparecchiatura chiamata "unita' anastro"
Le unita' a nastro sono dotate di due gruppi di te-
stine magnetiche rispettivamente per la lettura e la
registrazione, e dei dispositivi di segnalazione di
fine nastro e di arresto delle bobine.
Dall'abbinamento delle caratteristiche tecniche
funzionali dei nastri e delle relative unita' dipen
157
dono i seguenti requisiti
- la velocita' di trascinamento del nastro magnetico
- la densita' di registrazione
- la frequenza di registrazione.
Considerando che su una zona di circa 2,54 centime-
tri sono registrabili 300 caratteri, e che la veloci
ta' di un nastro puo' andare oltre i 370 centimetri
al secondo, appare evidente come sia impossibile ar-
restare un nastro sotto le testine di lettura e regi
strazione tra due specifici caratteri.
Si deve inoltre osservare che sia la lettura che 1a
registrazione su nastro magnetico sono possibili so-
lo quando esso funzioni a velocita' di regime: talt
velocita' pero' non e' raggiungibile istantaneamente
dallo stato di fermo, ne' il nastro funzionante a ve
locita' di regime puo' essere bloccato all'istante a
causa della forza d' inerzia contrapposta dalla bobi
na.
Si e' reso pertanto necessario il raggruppamento del
le informazioni registrate su nastro in blocchi sepa
rati da una piccola zona non registrata chiamata "in
terblocco"
Questo intervallo consente al nastro di avviarsi e di
raggiungere la velocita' di regime quando la testina
di lettura si posiziona sul primo carattere del bloc
co, oppure, una volta letto l'ultimo carattere
blocco di posizionare le testine al centro dell'in-
terblocco stesso.
Questo intervallo di circa 2,5 cm e' diviso in tre zo
ne
158
_mm. 7.5
mm. 24.:
dove A e C indicano le zone occorrenti per l'avvio
o 1' arresto del nastro, e B indica la zona riserva
ta per il posizionamento delle testine.
In linea di massima si puo' affermare che quanto
piu' lunghi sono i blocchi, tanto minori saranno le
zone di nastro e il tempo perduto per gli avvii
f
gli arresti.
Il dimensionamento dei blocchi viene effettuato ge
neralmente in rapporto alla capacita' della memo-
ria di lavoro dell' elaboratore; ovviamente una me-
moria di capacita' ridotta implichera' l'impiego di
blocchi di piccole dimensioni che esalteranno gli
inconvenienti citati.

## La registrazione e la lettura del nastro

I caratteri rappresentati nella memoria di lavoro
mediante sei bit vengono riprodotti sul nastro ma-
gnetico in modo analogo, con la sola variante che
in luogo di nuclei magnetici si hanno aree
magne-
tizzabili.
La registrazione, che avviene sempre in avanti, e'
sottoposta a un duplice controllo
un primo controllo e' quello di disparita', dato
da un settimo bit che viene registrato da un' ap-
159
posita testina in parallelo con i sei bit raffigu
ranti il carattere.
Mediante tale controllo si verifica che non visia
perdita o generazione spuria di un bit; infatti il
numero delle aree effettivamente magnetizzate com
presa quella di controllo, deve essere sempre di-
spari per ogni carattere;
- un secondo controllo e ottenuto mediante la let-
tura e l'immediato confronto di quanto e'
appena
registrato con la informazione originaria.
Risulta evidente l'assoluta garanzia che ne deriva
circa una corretta registrazione dei dati che si vo-
gliono temporaneamente conservare in archivio
bel
successive elaborazioni
Nel caso fosse riscontrato un errore per mezzo dei
suddetti controlli, esiste la possibilita' di appor
tare la necessaria correzione prima che la registra
zione prosegua.
Diversamente dalla registrazione la lettura puo' ay
venire sia avanti che indietro, ed il controllo e'
ottenuto solo mediante la verifica del bit di dispa
rita'
Per scandire i tempi di lettura in corrispondenza di
ogni carattere esiste un bit supplementare chiamato
"bit di temporizzazione" che provoca la lettura del
la zona di nastro in cui esso e' posto.
Come gia' si e' accennato, le unita a nastro magne
tico sono. collegate all' elaboratore tramite uno spe
cifico governo : governo unita' nastro (GUN).
Il GUN e' dotato di tre memorie
a) la memoria di ricerca, di 128 posizioni, che con-
tiene la chiave di ricerca per l'individuazione
di uno specifico blocco di informazioni.
160
DISPOSITIVO DI LETTURA E REGISTRAZIONE FR - 300

Mediante questo accorgimento tecnologico, e' pos
sibile infatti raggiungere qualsivoglia blocco
registrato su di un nastro ed apporvi le modifi
che o gli aggiornamenti richiesti dai particola
ri problemi di lavoro;
b) la memoria di controllo della registrazione, di
256 caratteri, che ha la funzione di contenere i
caratteri registrati ma non ancora riletti;
c) la memoria di trascrizione, la cui capacita' e'
di 2048 posizioni.
Quest'ultima memoria permette di eliminare even
tuali differenze d' impaccamento causate dalle di
verse condizioni tecnologiche di funzionamento
eventualmente verificatesi in successive opera-
zioni di registrazione, e da modo inoltre di evi
tare che in operazioni di trascrizione da nastro
a nastro si sommino tra di loro successive dif-
ferenze di frequenza di impaccamento.

## Organizzazione delle informazioni su nastro magnetico

Gruppi di caratteri, a seconda della funzione per
la quale sono stati creati, possono costituire le
seguenti unita' di elaborazione
1°
20
30
4°
50
la parola
la scheda
il blocco
la sequenza
1' informazione
La parola e' l'elemento minimo elaborabile e costi
tuisce un dato.
La scheda comprende una o piu' parole e costitui-
sce l'insieme dei dati relativi a un documento
161
162
NASTRO NO 1
SPAZIO INUTILITZ
DATI
BLOccO
DATI
NASTRO N° 2
ALLUNAINS TUPASDAZIO INUY
DATI
ORGANIZZAZIONE SU NASTRO
- 10 metodo
OOO DI BLOCCO INDICATIVO
DATI
BLOCCO
BLOCCO
DATI
DATI
GAP
BLOCCO
GAP
ALOCCO
CAD
8
DATI
DATI
minero
GAP
Diarro
? # ?
BLOCCO INDICATIVO
DATI
CAD
BLOCCO
GAP
BLOCCO
DATI
della
DATI
§
8
DATI
DATI
8
?#?
8
CAP
80 a
DATI
DATI
DATI
DATI
GAP
SPAZIO INUTIYY
ALUMINATURA
ALLUMINATURA
&91
ORGANIZZAZIONE SU NASTRO
- 20 metado
NASTRO NO 1
BLOCO INDICATIVO
SPAZIO INUTILIZZATO
DATI
BLOCCO
DATI
DATI
DATI
BLOCCO
GAP
2
?#?
NASTRO N° 2
BLOCCO
GAP
2
2
OATI br DATI
BLOCCO
GAP
SPAZIO INUTILIZZATO
Il blocco e' costituito da un numero variabile di
schede ed e' creato in funzione delle caratteristi-
che tecnologiche del sistema.
La sequenza e' un insieme di blocchi omogenei.
L'informazione comprende tutte le sequenze relative
ad un unico flusso di elaborazione.
Questi elementi sono individuabili sul nastro attra
verso speciali caratteri che li delimitano.
La parola
fa eccezione alla regola in quanto
e' reperibile anche senza speciali
caratteri di inizio e fine.
La scheda
termina col carattere teta (A) so-
lo quando viene operata mediante la
particolare istruzione NDN.
Il blocco
inizia e termina col carattere alfa
(a )..
La sequenza
termina col carattere punto interro
gativo che sostituisce uno dei due
alfa che delimitano l'ultimo blocco
della sequenza
La informazione inizia e termina coi caratteri abbi
nati "moltiplicato per" ( © ) ed al
fa (d).
Nella creazione dei blocchi si devono inoltre osser
vare le seguenti norme
1. La lunghezza dei blocchi in trascrizione deve es
sere al minimo di 3 caratteri inclusi i caratte
ri di inizio e fine blocco.
Per esempio sono blocchi accettabili
aga oppure d A
164
2. Per quanto riguarda l'istruzione NDN i blocchi di
nastro magnetico devono avere come lunghezza mi
nima 10 caratteri e come lunghezza massima 5000
caratteri.
3. Per quanto riguarda l'istruzione TN la lunghez-
za dei blocchi puo' essere al massimo di 5000 ca
ratteri.
NB a) Nella casella N° 5 e' indicato solo il tempo
necessario alla fase preparatoria; la durata
della fase esecutiva dipende infatti dal nu-
mero di caratteri o di blocchi che si voglio
no operare.
b) Le segnalazioni di macchina relative alle i-
struzioni SFS, SFI, SN1, SNs, vengono annul-
late ad avvenuta lettura dell'istruzione in-
teressata.
165
Leggi Nastro, avanti
LNa
esterno, GUN
X n1
IIII Im
* (110010)
10
X
11
T TTT
Im
: posizione non utilizzata
: nome del nastro in lettura
: indirizzo di memoria a partire dal quale vengono regi-
strati i caratteri da nastro
: il registro Im puo' modificare sia 1' indirizzo IIII che
il nome del nastro ni
: legge dal nastro montato sull' unita' ni (specificata in
p7) alla Memoria, procedendo in avanti
a) Il trasferimento avviene dal segnale di inizio blocco (o , ? ) al segnale di fi
ne blocco (o, ? .
b) I caratteri di inizio e fine blocco (d, ? ) vengono trasferiti in memoria
c) I caratteri letti sul nastro vengono registrati in Memoria a partire dall'indiriz
zo Ill e per indirizzi crescenti
Leggi Nastro, indietro
esterno, GUN
X ni
III I Im K (110011)
INi
10
Х
ni
Im
posizione non utilizzata
: nome del nastro in lettura
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del nastro ni
: legge dal nastro montato sull'unita' ni ( specificata
in p7 ) alla Memoria, procedendo indietro
a) Come la LNa, ma con senso di marciaindietro del nastro e per indirizzi decrescer
ti.
166
esterno, GUN
X ns
Registra Nastro
III I Im
RN
M (110100)
Х
ns
IIII
Im
: posizione non utilizzata
: nome del nastro in scrittura
:indirizzo di memoria a partire dal quale vengono regi-
strati i caratteri
:il registro Im puo' modificare sia l'indirizzo IIII che
il nome del nastro ns
: registra dalla Memoria, sul nastro montato sull'unita'
ns (specificata in p7), procedendo in avanti
a) Il trasferimento ha inizio dall'indirizzo IIII della Memoria e prosegue fino al
segnale di fine blocco (X . ?'), per indirizzi crescenti.
b) All'indirizzo IIII deve essere registrato il segnale di inizio blocco (d, ?).
c) Il blocco da registrare deve essere di almeno tre caratteri, inclusi i segnali
di inizio e fine blocco
167
Prepara Ricerca Nastri
PRN
esterno, GUN
IIII
Im
0 (111001)
10
X х
IIII
Im
: posizioni non utilizzate
: indirizzo di memoria a partire dal quale si trasferisce
alla memoria del GUN
: il registro Im puo' modificare l'indirizzo IIII
trasferisce dalla memoria dell' unita' centrale, a parti
re dall' indirizzo IIII e per indirizzi crescenti, alla
memoria del GUN, i caratteri comprendenti la parola chia
ve che sara' usata nella ricerca su nastro.
a) La ricerca puo' avvenire con una parola chiave avente al massimo la lunghezza di
128 caratteri: non e necessario che i caratteri interessati siano adiacenti pul
che' le posizioni non interessate alla ricerca siano diesizzate: il trasferimen•
to della parola chiave dalla memoria al GUN si arresta quando viene letto un
dopo un carattere diverso da d
b) Il carattere ( "" o "?" ) che obbligatoriamente inizia ogni blocco di nastro, nor
deve essere considerato; nel senso che la parola chiave non deve contenerlo. ne
deve contenere al suo posto un carattere # .
c) Se si desidera che il confronto avvenga con i caratteri registrati su nastro dal
alla (n +m) a posizione di ogni blocco (n +m < 128) la parola da tra.
sferire dovra comprendere inizialmente n car atteri - quindi la parola chiave
• di
m caratteri. e finalmente il carattere l
Esempio': per n = 4
```
####4812318
A BCD487231N
impostazione parola chiave
da trasferire nel Cin
organizzazione del nastrc
nella zona corrispondente
alla parola chiave.
d) Il blocco ricercato sara' quello contenente la parola chiave trasferita nel GUN:
, in mancanza di questo, il blocco contenente una parola chiave di valore supe
riore
quella trasterita
'e) Se nella ricerca la macchina non incontrasse alcuno di tali blocchi, per. provoca
re l'arresto dell'unita° a nastro sara° necessario prevedere sul nastro stesso un
ultimo blocco fittizio contenente tanti @ quanti sono i caratteri che esprimone
intero codice
Esempi
parola chiave
## 15798
blocco titt1zic
f) La ricerca e' convalidata per tutti i caratteri che nella parola trasferita dal•
la PRN sono diversi dal carattere • # • ; si rende quindi possibile la ricerca au
tomatica di blocchi con chiave spezzata.
Esempio :
# # # 251 # # 359 # A 0
168
```
Trascrivi Nastro
TN
GUN
n1 ns
B B B B
Im § (111010)
10
ng
Ds
в В В В
nome del nastro in lettura
nome del nastro in scrittura
•: numero di blocchi da trasferire da nastro a nastro
: il registro Im puo' modificare sia il numero BBBB che
il nome del nastro ns
: trascrive dall' unita' a nastro ny alla unita' anastro
ns un numero BBBB di blocchi.
a) Se la IN e immediatamente preceduta da una PRN si ha che
1) nelle posizioni p3 + p6 e' registrato il carattere x ;
~ istruzione trascrive da nastrc , a nastro un numero imprecisato di blocchi
l'ultimo dei quali e' quello che nelle sue posizioni iniziali contiene una pa
rola uguale o maggiore di quella trasferita nella memoria del GUN per
mezzc
della'PRN
b) Con unita' lettura inesistente, codificata # n, . # ## # # $, il nastro del-
l'unita' in registrazione viene cancellato totalmente.
c) Se durante la trascrizione dei BBBB blocchi si verifica un errore di registrazio
ne la macchina ne da segnalazione e si arresta nel blocco dove si e verificatc
1°errore stesso.
d) La lunghezza di un blocco non puo' superare i 5000 caratteri
alo
(al
169
est, int, GUN
Prepara Ingresso da Nastro
X х
I I I I
Im
R (111100)
PIN
10
X X
IIII
Im
: posizioni non utilizzate
: indirizzo di memoria a partire dal quale si registra
da n1 (specificato nell'istruzione NAN seguente)
: il registro Im puo' modificare l'indirizzo IIII
fissa l'indirizzo di memoria a partire dal quale ven-
gono registrati i caratteri letti sul nastro ni
a) L'istruzione PIN deve precedere immediatamente la NAN
est, int, GUN
n1 As
da Nastro a Nastro No
IIII Im E (110000)
NAN
10
ni
"s
IIII
: nome del nastro in lettura
: nome del nastro in registrazione
: indirizzo di memoria a partire dal quale si registra su
ns
: il registro Im puo' modificare sia l' indirizzo IIII che
il nome del nastro ns
: registra dalla memoria su nastro montato sull' unita' ns
(specificata in p7) e simultaneamente legge dal nastro
montato sull'unita' n (specificata in p8) su una diver
sa zona di memoria.
a) Ciascun carattere letto in memoria a partire dall'indirizzo IlIl specificato dal
la NAV viene trasferito sul nastro ng; ciascun carattere letto dal nastro nj vie
ne registrato in memoria a partire dall'indirizzo IIII specificato dalla PIN im-
mediatamente precedente
b) Se l'indirizzo specificato dalla PIN e' uguale o maggiore di quello indicato dal
la NAN, puo' accadere che 1 caratteri prelevati da n vadano a sostituire in
me
moria 1 caratteri che avrebbero dovuto essere piu' tardi registrati su n.
c Con le istruzioni PIN-NAN possono essere operati blocchi di lunghezza variabile.
d) I due nastri funzionano in avanti; l'istruzione ha termine quando sono stati le!
ti (sul nastro n' e in memoria) entrambi i caratteri di fine blocco.
e) Non e' possibile porre ns o ni inesistenti (carattere # )
170
NO
Da Nastro, seguendo una Direttrice a Nastro
NDN
est, int, GUN
n1 ns
III I
Im § (110110)
10 +1
ni
ns
IIII
Im
: nome del nastro in lettura
nome del nastro in registrazione
: indirizzo della direttrice
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del nastro As
: registra dalla memoria su nastro montato sull' unita' n
e simultaneamente legge dal nastro montato sull'unita'
Di sulle stesse zone di memoria.
a) Ciascun carattere letto da nastro va ad occupare la posizione di memoria da cui
si e' immediatamente prima prelevato il carattere da registrare.
b) Le informazioni vengono lette e registrate a gruppi di caratteri la cui fine e'
contraddistinta dal carattere "" per es
1234567890
c) I blocchi ed i gruppi corrispondenti devono avere la stessa lunghezza nei due na
stri ns e n]
axxxx00xx00xxx00xx00 xxxxxo
d) La lunghezza di un blocco organizzato per essere operato con laNDN puo'
re da 10 a 5.000 caratteri.
yari
e) Il primo gruppo è' costituito dal carattere di inizio blocco, seguito immediati
mente o dal primo carattere "o" ed e' quindi composto di due caratteri'; "oo"
oppure dal contenuto della prima informazione ed e' allora composto da un nume
ro di caratteri pari a quelli dell'informazione + 1.
In memoria,
decrescenti,
e
ta lairettrice"
a partire dall'indirizzo IIII (modificabile da Im)
indirizzi
registrata una lista consecutiva di indirizzi di memoria chiama
i Ognuno di questi indirizzi e' l'indirizzo di memoria a partire dal quale, per
inda1221 crescent1, vengono prelevati e sostituiti i caratteri costituent
un gruppo.
2) Il primo indirizzo di destra della direttrice e' l'indirizzo del gruppo
con
tenente l' O di inizio blocco, mentre l'ultimo indirizzo di sinistra corri
sponde o all'indirizzo dell' o di fine blocco o all'indirizzo di
sinistr:
del gruppo che lo contiene.
Il numero (N) degli indirizzi di una direttrice puo' essere quindi costituitc
1 dal numero delle informazioni costituenti il blocco:
2) dal numero delle informazioni costituenti il blocco
più' l'indirizzo del gruppo "°e = di inizio blocco:
N+
171
3) dal numero delle informazioni costituenti il blocco
piu' 'indirizzo dell'∞ di fine blocco
4) dal numero delle informazioni costituenti il blocco
piu' l'indirizzo del gruppo " o
e. di inizio blocco
e l'indirizzo della di fine blocco
AxxOxxxOxxx0xxx0xxxxxx0
Ig
12 з I 15 I6
HOxxxOxxxOxxxOxxxAxxxo
Titz 1s 1s Is Io
dOxxxAxxxAxxxAxxx00
з In Ig
XxxAxxxoxxxAxxxOxxx00
X12
13
Ta 1s 16
6 IgIgIgIgI1.
direttrice
g) I due nastri funzionano in avanti : l'istruzione ha termine quando viene letto il
carattere di fine blocco.
h) Ponendo n , inesistente (carattere ) si esegue solo il trasferimento da ni
vers(
memoria secondo l'ordine stabilito dalla direttrice.
Analogamente, ponendo nj inesistente (carattere#) si esegue solo il trasferimen-
to da memoria verso " secondo l'ordine stabilito dalla direttrice.
172
de e
o
olo E 06
"
o ar
NASTRO IN REGISTRAZIONE
MEMORIA PRINCIPALE
DIRETTRICE
&LI
A do B de C 00
o
06 E
2
NASTRO IN LETTURA
Disponi Unita' e Blocco
DUB
GUN
n
B B B B
Im
N (111000)
10
J
RRRR
Im
N
: nome del nastro interessato
: indicazione del senso di marcia
: numero dei blocchi del nastro interessati dall'istru-
Zione
: il registro Im puo' modificare sia il numero BBBB che
il carattere indicato in J
: fa procedere il nastro montato sull' unita' n (specifi
cata in p8) del numero di blocchi indicato in BBBB, in
avanti o all'indietro, secondo il carattere indicato
in J.
a) Nelle posizioni da p3 a p6 non e' indicato un indirizzo di memoria
b) Se nel carattere indicato in J il bit "a" e' zero, il numero di blocchi e' ugua-
le a BBBB; se invece e' "¡" • il numero di blocchi e' 10.000 + BBBB.
c) Se nel carattere indicato in J il bit "d' e' zero, lo svolgimento avviene in avan
ti '; se invece e' "i" avviene all'indietro.
d) Se durante l' esecuzione della presenta istruzione si verifica un errore, la mac-
china ne da indicazione e procede fino alla fine della conta dei blocch
174
I
esterno, GUN
n
Cancella nastro
711 In P (111011)
KN
10
n
I II I
Im
P
: posizione non utilizzata
: unita' a nastro interessata
: indirizzo di memoria che determina l'inizio dell'opera
zione
: il registro Im puo' modificare sia l' indirizzo IIII che
1 nome del nastro
: cancella il nastro montato sull' unita' n, per una lun
ghezza determinabile in pollici
a) La cancellazione ha luogo durante il tempo impiegato dalla macchina a percorrer
le posizioni di memoria che vanno dall'indirizzo Ill fino al primo carattere
d
(alfa).
b) La porzione di nastro che ne risulta cancellata e' determinabile con la formula
L= N.
v/f
dove
L = lunghezza nastro cancellato, in pollici;
N = numero caratteri intercorrenti fra l'indirizzo IIII ed il primo carattere d
(alfa);
: velocita' del nastro in pollici per secondo:
f = frequenza di lettura della memoria, in caratteri al secondo
c) La KN viene normalmente utilizzata per cancellare una porzione di nastro.
d) Il contenuto della memoria rimane inalterato. All'indirizzo IIII non deve essere
registrato il carattere @ (alfa).
e) Per comodita' di calcolo indichiamo una formula approssimata per determinare lo
spazio di nastro cancellato
L = 2,1 + N. 1,98. 10-3
dove N e' il numero di caratteri intercorrenti tra l'indirizzo IIII ed il primo
espresso in centimetri, con una approssimazione di + 1/2 centimetro.
175
unita' a nastro
X n
Avvolgi Nastro
X X X X
Im
AV
(001101)
10
n
I'm
X Xxx : le posizioni p3, p4, p5, p6, p8 non sono utilizzate
: nome dell' unita' a nastro interessata
: il registro Im puo' modificare il nome dell' unita' ana
stro n
: riavvolge all'indietro la bobina montata sull'unita'
nastro n fino al termine del nastro.
a) L'operazione di riavvolgimento non impegna il 'GUN ma solo l'unita' interessata,
pertanto possibile far eseguire simultaneamente :
1) piu' operazioni di riavvolgimento purche' interessino unita' diverse;
2) una qualsiasi delle istruzioni relative ai nastri, di tipo LN, NDN, PRY,
ecc. purche non interessino l'unita
bì Durante l'operazione di riavvolgimento :
1) una istruzione riguardante la stessa unita' resta bloccata fino a terminat
esecuzione dell'AV;
2) l'eventuale istruzione SNO relativa alla stessa unita' viene eseguita.
c) Se il GUN e' impegnato in una normale operazione, non e' in grado di ricevere
struzioni di riavvolgimento.
176
Salta se fine sequenza
SFS
interno
(111000)
N
Is
I III Im 0
10 0 15
a) Salta se l'ultimo blocco letto da nastro inizia o termina con il carattere "?" di
fine sequenza.
b) L'istruzione non viene eseguita se e' in corso un'eventuale operazione di nastro.
c) La segnalazione relativa a questa istruzione puo' essere , annullata oltre che dal.
la lettura dell'istruzione stessa anche dalla lettura di una istruzione qualsias
di nastro
Salta se fine nastro in lettura
interno
(111011)
PIs
IIII Im 0
SN1
10 0 15
a) Salta se e' terminato il nastro in lettura.
b) L'istruzione non viene eseguita se e' in corso un'eventuale operazione di nastro.
Salta se fine nastro in registrazione
interno
(111111)
Q Is
SNs
I I I I Im 0
10 0 15
a) Salta se e' terminato il nastro in registrazione.
b) L'istruzione non viene eseguita se e' in corso un'eventuale operazione di nastro
177
Salta se fine informazione
SEI
interno
(111101)
Is
.I I I I
I'm 0
10 o 15
a) Salta se l'ultimo blocco da nastro termina con il carattere di fine informazione
11 09
b) L'istruzione non viene eseguita se e' in corso una eventuale operazione di
nas
stro.
c) La segnalazione relativa a questa istruzione puo' essere annullata oltre che dal
la lettura dell'istruzione stessa anche dalla lettura di una istruzione qualsia
Si di nastro
Salta se nastro occupato
SNO
interno
( - - - - ==)
n
Is
II I I
Im 0
10 0 15
a) Salta se l'unita' a nastro "n" e' gia' impegnata
b) Il carattere di eventualita' non e' fisso, ma e' il carattere che contraddistin-
gue l'unita a nastro interessata.
c) La segnalazione di nastro occupato viene annullata dalla lettura del primo saltc
incontrato dopo l'esecuzione della presente istruzione.
178
Salta su Condizione Automatica
SCA
interno
(110101)
(
Is
I I I I
Im 0
10 0 15
Is
IIII
0
:carattere di eventualita'
: registro che ricorda l'indirizzo della posizione p8 del
1' istruzione
: indirizzo dell'istruzione alla quale si deve saltare
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro Is
: salta se si e' verificata una delle seguenti eventuali
ta' : riconoscimento di carattere chiave, unita' nastro
non disponibile, condizione d'errore o condizione ester
na SE4.
a) l'analisi di quale condizione si e verificata va eseguita mediante un sottopro
gramma con il quale si possono ricavare le indicazioni particolari relative a cia
scun organo e al tipo di segnalazione da esso rilevata
b) Generalmente l'istruzione SCA viene posta di seguito a una istruzione di nastro
di tipo LN, NDN, -NAN.
c) La sua esecuzione dipende dall'impegno del canale interno :
se questo e' liberc
a SCA viene eseguita, altrimenti resta bloccata
d) Per la NDN e PIN -NAN la SCA non viene eseguita fino ad ultimata operazione di let
tura e registrazione, permettendo in tal modo alle eventuali segnalazioni di FS,
FI, Ni e Ns di rivelarsi prima dell' effettuarsi della SCA.
e) Questo non avviene per la LN che occupando nell'esecuzione solo il canale esterno
permette all'eventuale SCA che segue d'essere eseguita quando e' ancora in corsc
la lettura del nastro.
S1 puo' pero' ovviare a questo inconveniente facendo precedere la SCA da una del-
le istruzioni che bloccano il proseguimento del programma in cui sono registrate,
fino a terminata esecuzione dell'operazione di nastro in corso.
E' evidente che con una tale organizzazione si ottiene l'esecuzione della dA pro
prio quando le possibili condizioni si siano verificate.
f) Qualora l'istruzione SCA rinviasse ad una istruzione diversa da salto
verrebber‹
annullate tutte le segnalazioni memorizzate per conto dell'istruzione stessa.
g L'esecuzione di uno dei salti e del relativo programmino annulla la segnalazione in
questione.
h) Sfruttando la caratteristica g) e' conveniente far precedere ogni programma da uni
istruzione SCA seguita da istruzione diversa da salto per annullare eventuali se.
gnalazioni rimaste memorizzate da precedenti elaborazioni.
Esempio
SCA
ETs
0016
Im
F
0008
MA
LL
IIII
Im
F
0016
179
SCHEMA RIASSUNTIVO
Memoria - Nastri
Nastro - Memoria - Nastro
Nastro - Nastro
Nastro
Salti
LNa
NDN
TN
DUB
LNi
PIN
SFS
KN
INT
Particolarità' dei Nastri
In formazioni . sono registrate e lette carattere per carattere e
cioe' in serie.
Bit
ad ogni carattere corrispondono
a
bit di sposti
uno accanto all'altro nel senso della larghezza
del nastro l6 hit definiscono un carattere.
:1 70
e' il bit di disparita' e 1'8° il bit di temporiz
harione).
Caratteri
cneciol; dei
nastri
..
X) il carattere "O " segnala l'inizio e la fi.
ne di un blocco:
2141 carattere " ? " inizia e termina il primo
¡altimo blocco di una sequenza;
W) il carattere " @ " inizia e termina il primo
jaltimo blocco di una informazione;
A) il carattere " segra le informazioni co
stituenti un blocco organizzato per essere
operato con la NDN.
Numero dei
conattori
- registrabili in una bobina di nastro con blocchi
di n caratteri in media.
dato dalla seguente
formula:
60 000
n+
-200
Unita' nastro - collegabili al
GIN sono al massimo 20.
I caratteri che le distinguono sono :
193456789~dABCDEFGHI
Istruzioni Nastri
RN
PRN
NAN
AV
SNs
SFI
SCABICECO
CANALI
LNa
LNi
GUIN
RN
PRN
NDN
pIN
~a4 int CIN
NAN
IN
DUB
KN
AV
GIN
ast.. CLIN
uni tal noe.
SES
SNI
SN
SFI
SNO
SCA
interno
SNO
TEMPO
IN PERIODI DI CIFRA
10
900
lo
SCA
CONFIGURAZIONE
~ za
FFFFFFE
CARATTE
i =
.a
o o o

