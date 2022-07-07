# CAP. 10° : LA TERZA SEQUENZA DI PROGRAMMA

## 10.1. Generalita'

1) All' unita' centrale del sistema Elea 9003 posso~
no essere collegate unita' in linea capaci di fun
zionare simultaneamente e di operare senza inter
rompere lo svolgimento del 10 e del 20 program-
2) Le unita' collegabili sono
- lettori di schede
• perforatori di schede
- lettori di nastro perforato
lettori e perforatori di schede
stampanti
Le varie unita' numerate da 1 a 10 vengono distin
te in fase di elaborazione dal proprio numero in
dicativo.
Nell'uso normale troviamo simultaneamente colle-
gate unita' di diverso tipo anche se teoricamen
te esiste la possibilita di porre in linea die-
ci unita' con medesima funzione.
3) Ciascuna di queste unita' e' diretta da un pro-
prio governo che contiene l' apparecchiatura logi
ca necessaria al suo funzionamento e una memoria
a nuclei sufficiente a contenere i caratteri ne-
cessari per ogni ciclo meccanico di lavoro
una riga stampa,
una scheda,
un blocco di nastro perforato (max. 104 caratteri)
4) L' alternarsi dell' entrata e dell'uscita dei
ca«
ratteri dalle varie memorie, la distribuzione dei
dati alle diverse unita' collegate e la logica
che le regola, sono affidate ad un sincronizzato
203
re che armonizza tutte le operazioni di terzo pro
gramma.

## 10.2. Caratteristiche logiche del 30 programma

1) L'ordine di lavoro alle singole unita' viene tra
smesso dall' unita' centrale, che procede quindi
in parallelo con esse, senza che queste ultime
rallentino ne' intralcino le operazioni interne;
il sincronizzatore provvede a smistare gli ordi-
ni e le informazioni alle diverse apparecchiatu
re; ogni unita' chiamata ad operare esegue il la
voro secondo le peculiari modalita ed il pro
prio tempo meccanico.
Le memorie di transito delle singole unita' di e
strazione vengono fornite delle informazioni in
uscita dall' unita' centrale che provvede pure a
prelevare le informazioni in entrata dalle uni-
ta' di introduzione.
Non e' necessaria ad ogni trasferimento dao a u
nita' centrale un' operazione di azzeramento del-
le memorie di transito in quanto queste vengono
azzerate automaticamente.
2) Durante il collegamento con il calcolatore, le u
nita' di introduzioneed estrazione assumono tre di
versi stati possibili;
"inattiva" l'unita' che pur collegata con l'u-
nita' centrale attraverso il proprio
governo, non Sia avviata;
"avviata"
l'unita' che sia stata chiamata ad
operare almeno una volta mediante
un'istruzione. Lo stato di "avviata"
puo' durare per molti cicli meccani
ci di lavoro;
204
"occupata"
1' unita' che oltre ad essere avvia-
ta sia stata effettivamente messa in
funzione da una istruzione esecuti
va.
Ogni unita' avviata ed occupata passa automatica
mente allo stato di avviata-non occupata al ter
mine di ogni ciclo meccanico di lavoro; passa al
lo stato di inattiva mediante un' apposita istru-
zione di STOP.
La simultaneita' di esecuzione delle operazioni
interne della macchina e del lavoro delle unita'
collegate e' ottenuto mediante una terza sequen-
za di istruzioni eseguibili dall' elaboratore pa-
rallelamente alle sequenze di 1° e 20 programma.
L'uso delle diverse sequenze non comporta intral
ci ne' inconvenienti alla corretta e coerente e-
secuzione delle istruzioni dei singoli programmi.
Esistono prestabilite priorita' sul canale inter
no, tre diversi registri indirizzo istruzioni, e
dispositivi distinti per ogni programma per la
conservazione separata delle seguenti segnalazio
ni circa determinate eventualita' verificabili
nel corso dell' elaborazione: risultato dei con-
fronti ( =, + , > , ' ) e overflow nei registri
e nella memoria.
Si deve inoltre osservare che contrariamente al
le istruzioni di canale esterno che vengono poste pre-
feribilmente sul 2° programma, per sole ragioni
di logica, le istruzioni di comando delle appa
recchiature in linea devono essere raccolte ob-
bligatoriamente sul 30 programma per ragioni fun
zionali. Questa disposizione risulta inoltre 10-
gica specie se si considerano le norme che stabi
liscono le priorita sui canali
205
La priorita' sul canale interno e' riservata :
prima al 30 programma che per l'esecuzione delle
istruzioni che lo riguardano non richiede il ca-
nale interno se non per periodi di tempo assaili
mitati;
quindi al 20 programma che si svolge nella massi
ma parte con impegno del solo canale esterno;
infine al 1° programma che impegna il canale in-
terno sia in fase preparatoria che in fase esecu
tiva.
E' evidente che dette priorita' sono studiate in mo
do da permettere ad ogni programma la massima conti
nuita senza che l'esecuzione degli altri programma
subisca per questo eccessivi tempi di attesa.
Risulta pertanto logico che dovendo i tre programmi
ricorrere al canale interno per il loro svolgimen-
to, su questo canale debba aver la precedenza il pro
gramma che meno lo impegna.
In pratica il 30 programma cede la precedenza sul ca
nale interno
1° ogni qualvolta le memorie di transito dei gover-
ni delle unita' in linea risultino fornite dei ca
ratteri necessari ad un ciclo meccanico di lavo-
ro;
2° ogni qualvolta si verifichi un impedimento all'e
secuzione di una delle istruzioni registrate in
detto programma.
La precedenza al terzo programma invece non viene in
mediatamente ceduta in due particolari casi
1° allorquando sia stata letta su 10 o 20 programma
una istruzione preparatoria tipo PUM, PRN, PIN .
Nel qual caso il canale interno viene ceduto solo
206
dopo l'esecuzione dell'istruzione esecutiva tipo
MEM, + MM ,
- MM , TN, NAN;
2° allorquando sia stata letta ed eseguita su 10 o 20
programma una istruzione di salto. Nel qual caso
il canale viene ceduto solo dopo l'esecuzione del
l'istruzione a cui il salto rinvia.
та terz seauenza di programma
a) puo' essere avviata da una istruzione particola.
re di salto S3P, registrata indifferentemente nel
1° o nel 20 programma;
b) puo' essere frazionata in piu' sequenze singolar
mente avviabili ma non contemporaneamente esegui
bili in quanto l' elaboratore puo' essere impegna
to nell' esecuzione di una sola sequenza di 30 pro
gramma;
c) puo' eseguire istruzioni di qualsiasi genere pur
avendo come funzione specifica i comandi relati-
vi alle apparecchiature in linea.

## 10.3. Fasi di svolgimento del 30 programma

1) Una istruzione S3P da inizio all'esecuzione del-
la sequenza. Appositi registri, distinti da quel
li con ugual funzione, di 10 e di 20 programma,
conservano gli indirizzi e le segnalazioni rela
tive alle istruzioni di 30 programma.
2) Vengono quindi percorse le istruzioni della se-
quenza secondo le normali modalita' di funziona
mento, ma con i seguenti effetti
a) l'istruzione suo avvia l' unita interessata;
b) l'istruzione TOL esegue un ciclo completo di
lavoro: trasferimento dei caratteri alla me-
moria di transito ed elaborazione relativa
207
c) le altre istruzioni compiono la loro normale
funzione.
3) Ritorno alla 1° istruzione SUO eseguita, nelle se
guenti possibili condizioni
a) l'unita' relativa alla SUO non e occupata; nel
qual caso il salto non viene effettuato e si
eseguono l'istruzione TOL e successive;
b) l'unita' relativa alla SUO e occupata ma al-
meno una delle altre unita' si e' resa dispo-
nibile; nel qual caso viene effettuato il sal
to all'istruzione indicata dalla SUO e la se-
quenza viene percorsa fino alla prossima suo
che si trovi nella condizione c);
c) 1'unita relativa alla SUO e occupata e co-
si' pure tutte le altre unita'; nel qual caso
il 30 programma si arresta su detta istruzio-
ne.
4) Esecuzione infine degli STOP relativi alle uni"
ta' in linea, con i seguenti possibili effetti :
a) se lo STOP viene eseguito quando ancora non e'
letto almeno uno degli altri STOP esistenti
nella sequenza di 3° programma, 1' unita' inte
ressata passa allo stato di •inattiva
senza
che lo svolgimento del programma venga inter
rotto;
b) se lo STOP e' eseguito dopo 1' avvenuta lettu-
radegli altri STOP 1' unita' passaallo stato di inat
tiva ed il programma si arresta.

## 10.4. Funzione e logica delle istruzioni s3P, TOL, STOP

L'istruzione S3P a) comanda l'inizio di una sequen
za di 30 programma;
208
b) attiva tutte le unita che ven-
gono percorse dal 1° ciclo di
30 programma;
c) viene riciclata qualora sia let
ta mentre e gia' in corso
sequenza di 30 programma:
d) puo' riavviare una sequenza di
3° programma non appena ne sia
terminata una precedente.
L'istruzione SUO
permette
a) di avviare l'unita a cui e ri
ferita;
b) l'arresto del programma nel ca
so che nessuna unita sia dispo
nibile;
c) il riavvio del programma ad ogni
segnalazione di unita disponi-
bile.
- Dopo 1' arresto su una suo.
il
riavvio del programma avviene
con la lettura dell' istruzione
stessa
- Nel caso la suo richiamasse una
unita' non collegata, il calco-
latore non esegue la sequenza di
programma relativa a tale uni-
†. а
L'istruzione TOL deve seguire immediatamente nel pro
gramma la SUO relativa.
essa permette :
a) di eseguire l'effettivo trasfe-
rimento dei dati fra la memoria
dell' unita' centrale e le memo»
rie di transito delle unita' in
'linea;
209
b) di predisporre l'unita' in li-
nea all' esecuzione del ciclo
operativo successivo: autoriz
zazione alla prossima lettura,
perforazione o stampa, precedu
ta o seguita dall' azzeramento
della memoria di transito.
L'istruzione STOP appare generalmente al termine di
ogni sequenza d' istruzioni relati
ve ad una unita' in linea.
Essa
permette
a) di riportare una unita' allo
stato di inattiva non
appena
sia stata completata l'opera-
zione per la quale era stata
chiamata;
b) di arrestare il 30 programma
una volta eseguiti tutti gli
STOP delle unita' avviate.
Va rilevato che l'istruzione STOP non arresta il ci.
clo operativo in corso, ma le operazioni atte a pre.
disporre l' unita' in linea al successivo ciclo di
lavoro dopo 1' azzeramento automatico della memoria
di transito.

## 10.5. L'istruzione SP*

Mediante questa istruzione si vuole ovviare all'in-
conveniente generato dall'uso della sola istruzione
S3P normale, che non permette di realizzare un mec-
canismo dinamico di sovrapposizione tra 1° o 20 pro
gramma e 3° programma, basato su uno scambio di ri-
chieste e di segnalazioni.
Caratteristica logica dell'istruzione S3P* e' infat-
ti quella di rendere possibile un ciclo intero di 30
programma ogni qualvolta se ne presenti la necessi-
ta' durante lo svolgimento dei primi due programmi,
permettendo in tal modo di avviare una sequenza re-
lativa ad una unita' in linea temporaneamente inu-
tilizzata.
Differenza rilevante tra l'istruzione S3P e l'istru
Zione S3P* e' che mentre la prima atti va le unita
in linea, la SP* puo' soltanto avviarle.
Ne consegue che
1° tutte le unita' interessate dalla sequenza di 30
programma devono essere attivate dall'istruzione
S3P e conseguentemente percorse durante il 1° ci
clo di 3° programma;
2° una unita' resasi inattiva non puo' essere riat-
tivata se non dopo che tutte le unita' considera
te nel 30 programma siano tornate allo sta-
to di inattive.
Si osservi inoltre che l'uso della istruzione S3P*
richiede 1' impiego nel 30 programma di una istruzig
ne SUO relativa ad una unita' inesistente
(SUO sU
unita' fittizia).
L' istruzione SUO su unita' fittizia deve appa-
rire in testa alla sequenza di istruzioni ed esse-
re letta nel 1° ciclo di 30 programma.

## 10.6. L'organizzazione di un 3° programma che prevede l'uso della istruzione S3P* dovra' pertanto essere legata alle seguenti norme.

1) Sul 1° o 2° programma deve essere registrata una
istruzione S3P che permetta l'attivazione di tut
te le unita' interessate all' elaborazione.
211
2) La S3P deve rinviare direttamente o indirettamen
te all'istruzione SUO su unita' fittizia che si
trova in testa al 30 programma. Solo in questo mo
do l' unita' puo' risultare facente parte del
30
programma.
3) Le sequenze relative ad ognuna delle unita' in li
nea interessate devono essere precedute da un de
viatore che resta aperto durante il primo ciclo
di 30 programma.
4) Se una unita' non e' da utilizzarsi immediatamen
te, il deviatore che ne introduce la sequenza re
lativa deve venir chiuso, cioe' indirizzato al
successivo deviatore, mediante una istruzione ap
posita che lo deve seguire nel programma.
5) Successivi posizionamenti dei deviatori possono
essere disposti da istruzioni registrate indiffe
rentemente in uno dei tre programmi a seconda del
le necessita' di programmazione.
6) L'istruzione SP* non deve rinviare alla Suo
su
unita' fittizia ma all'istruzione che la segue im
mediatamente perche' la lettura della SUO provo
cherebbe la disponibilita' del canale interno per
il 10 o 20 programma.
Ripresa automatica del canale interno da parte del
10, 20 e 30 programma.
- Il 10 o 20 programma riprendono la precedenza se
si verifica nel 30 una delle seguenti eventuali-
ta'
1° tutte le unita' in linea sono allo stato diroc
cupata" e il 30 programma e' fermo sull'istru
zione SUO in corrispondenza della quale tale e
ventualita' si e' verificata (programma che pre
vede il solo uso dell' istruzione S3P);
212
2° tutte le unita' in linea sono allo stato di oc
cupata" ed il 30 programma e' fermo sull'istru
zione SUO su unita' fittizia(programma che
pie
vede l'uso dell' istruzione $3P*).
- Il 30 programma riprende la precedenza se e' presen
te almeno una delle seguenti condizioni :
1° una unita' precedentemente occupata sie' resa di
sponibile;
20 richiesta di ciclo di 30 programma da parte del
1° o 20 programma mediante l'istruzione S3P*;
Nell'organizzazione che prevede l'uso della S3P*no
nostante l'arresto sulla SUO su unita' fittizia, nel
riavvio di un ciclo di 30, detta istruzione non e
considerata e viene invece letta immediatamente la
istruzione che segue;
con l'uso della sola SP l'istruzione SUO da cui
il programma riparte viene viceversa letta ed even
tualmente eseguita.
Automatismo relativo ai segnali di unita' disponibile
Il 30 programma, indipendentemente dall'uso della
S3P*, viene percorso fintanto che perdura la segnala
zione di unita' disponibile.
Questa segnalazione ha tuttavia caratteristiche
verse a seconda dell'organizzazione scelta.
Infatti coll' uso dell'istruzione sUO su unita' fitti
zia, eventuali segnalazioni di unita' disponibile per
mangono solo temporaneamente, di modo che se per una
ragione qualsiasi (chiusura di un deviatore) l'uni.
ta' disponibile non viene occupata durante il ciclo
richiesto, tale segnalazione si perde, e solo un nuo
vo comando originato da una S3P* o da una nuova se-
gnalazione di disponibilita' puo' permettere un
c1.
clo di lavoro all' unita' resasi precedentemente
sponibile.
213
interno
Il II
Im
0
Salta al programma esterno
S3P
(011101)
Is
IIII
Im 0
10 0 15
: carattere di eventualita'
: registro che ricorda l'indirizzo della posizione p8 del
l'istruzione
: indirizzo dell'istruzione posta nella sequenza di pro
gramma esterno alla quale si deve saltare
: il registro Im puo' modificare sia l'indirizzo IIII che
il nome del registro Ts
: salta se si e' verificata l'eventualita
a, L'istruzione posta nel 10 e 20 programma comanda l'inizio di una sequenza di pro
gramma esterno.
, de e gla' in corso una sequenza di programma esterno
1°, la presente istruzione viene riciclata finche' la sequenza in corso non e' tei
manata:
2°1 terminata l'esecuzione della sequenza di programma esterno, la S3P puo'
yaaa
Salta al programma esterno *
S3P
interno
(010101)
=
Is
III I
Im 0
10
: carattere di eventualita
Is
: registro che ricorda l'indirizzo della posizione p8
dell'istruzione
: indirizzo dell'istruzione che segue la suo su unita fit
tizia
Im
: il registro Im puo' modificare l'indirizzo IIII e il no
me del registro Is
0
: salta se si e' verificata l'eventualita' =
a) La presente istruzione suppone ayviata una sequenza di 3 programma mediante una
precedente S3P normale
bj Per essere utilizzata e necessario che la sequenza di 30 programma abbia una SUC
su unita? fittizia
c; Se e' gia' in corso una sequenza di programma esterno la S3P* non blocca il pro
gramma su cui e' posta.
La S3P* viene sempre eseguita anche se e' in corso una sequenza di 3
non blocca mai il programma in cui e'
programma,
posta; permette un ciclo intero di :
gramma ogni qualvolta ne sorga la necessita'
d) Il ciclo di 3° programma ottenuto mediante S3P* parte dall'istruzione successiva
alla SUO su unita' fittizia e si arresta invec su quest ultima
214
interno
Salta se l'unita' U e' occupata
(011010)
%
U
II I I
I'm 0
SUO
10 o 15
%
U
I I II
Im
O
: carattere di eventualita'
: nome dell'unita' in linea
: indirizzo dell'istruzione a cui si deve saltare
:il registro Im puo' modificare sia l'indirizzo IIII che
il nome dell'unita'
U
: salta se si e' verificata l'eventualita'
a) In ogni sequenza di programma esterno compaiono tante SUO quante sono le unita' il
linea interessate.
b) La prima volta che la sequenza viene percorsa nessuna SUO viene eseguita, ma l'u
nita' in linea U, specificata in pl, viene avviata
c) La presente istruzione serve pure a specificare l'unita' interessata dall' istru
zione 10L che segue
interno
L
Trasferisci On Line
L
IIII
Im
J (110001)
TOL
10 + 1
LL
IIII
Im
: lunghezza dell' operando
: indirizzo di memoria dell' operando da trasferirsi
: il registro Im puo' modificare sia l'indirizzo IIII che
la cifra delle unita' della lunghezza LL
: trasferisce dalla memoria principale alla memoria di
transito oppure viceversa, a partire dall'indirizzo
IIII per lunghezza LL e per indirizzi crescenti.
a) L'istruzione trasferisce da oppure a memoria di transito secondo che l'unita
i r
linea specificata dalla SUO immediatamente precedente sia un lettore di schede c
un lettore fotoelettrico di banda perforata, oppure una
re di schede,
stampante o un perforato
215
Salta se errore in unita' in linea
interno, unita'
in linea U
(011110)
I I I I Im 0
SEL
10 o 15
ai Salta se si e' verificato un errore nell'unita' in linea U, specificata in p7
b) La segnalazione di errore su unita' in linea presenta diverse caratteristiche
secondo del genere di apparecchiature nel quale l'errore si verifica; infatti
segnalazione avviene :
per il lettore di schede
: al termine della lettura della scheda successiva
a quella in cui l'errore
verificat.
per il perforatore di schede : al termine della perforazione della 2° scheda sur
cessiva a quella in cui errore si e veriticat
per la stampanti
: terminato un ciclo di stampa (prima della TOL suc
cessiva
Arresto di unita' in linea
STOP
interno
(111001)
XXx X #
O
10
0
U
#
: carattere di eventualita'
: unita' in linea
: posizioni non utilizzate
: posizione non utilizzata
: arresta l'unita' in linea U, specificata in p7.
a) L'unita' in linea U passa allo stato "inattiva'
b) Se una o piu' unita' in linea passano allo stato "inattiva" la sequenza di
pro
gramma esterno continua a svolgersi per le rimanenti.
c) Solo quando tutte le unita' in linea hanno ricevuto la segnalazione di Stop:
30 programma si arresta.
il
d) L'arresto del 30 programma non blocca gli altri programmi eventualmente in cor
e) Lo Stop non arresta immediatamente l'unita' interessata ma solo al termine del•
l'ultimo ciclo meccanico di lavoro
216
SCHEMA RIASSUNTIVO
Istruzioni di 30 programma
Istruzioni
S3P
S3P*
sUO, TOL,
SEL,
STOP
Particolarita' del 30 programma
sap
non puo' essere esequita se el in corso il 30 program
ma.
e viene riciclata con conseguente blocco del pro-
gramma in cui a° registrata.
S3P*
permette un ciclo di 30 programma ogni qualvolta vie-
ne letta, anche se detto programma e' gia' in corso.
SUO
TOL
SEL
STOP
per le particolarita riguardanti queste istruzioni
rimando agli schemi relativi
Unita' collegabili : lettori di schede
perforatori di schede
lettori di nastro perforato
lettori e perforatori di schede
etamnanti.
N. unita' collegabili: 10, omogenee o di tipo diverso.
Stati possibili di una unita' collegata :
inattiva
non avvisto
!I
orviata ma non occupata
occupata
1
avviata e occupata
Priorita' del 30 sul 10 e 20 programma : ogni qualvolta sia dispo
nibile una unita°
a2404*194;
casi seguenti
a) nel 10 o nel 20 sia letta la prima di una istruzione doppia :
pUM.
PIN. PRN
h nel 10 o nel 20 sia letta ed eseguita una istruzione di salto
analcinci
CODICE
SIMBOLICO
S3P
S3P*
suO
TOL
SEL
STOP
CANALI
interno
intor
linea
interno
TEMPO
IN PERIODI DI CIERA
10
10
10 0
10
10 0 15
CONFIGURAZIONE
X
Tm
TIm
#
o
o

## 10.7. Esempio di 30 sequenza con uso della sola SP

Generalita'

.Nell'esempio seguente si fa riferimento ad una se
quenza di 30 programma avviata dal 1°mediante $3P.
- La sequenza e' costituita da 2 cicli fondamentali
riferentisi rispettivamente a 2 unita'.
Nel caso
specifico, unita' 1, 2.
L'unita' 1 e' supposta essere un perforatore di
schede, l'unita' 2 un lettore di schede.
- Sono supposte gia' preparate le zone di memoria
che saranno operate nelle istruzioni TOL (una per
ognuno dei sopraddetti cicli).
- I registri T utilizzati sono Ij, T2 ( rispettiva.
mente associati alle unita' 1, 2), che servono sia
per la conta del numero di schede, sia per la mo-
difica dell'indirizzo della TOL per passare da una
zona predisposta per una scheda, alla successiva.
- Schede da perforare (unita' 1) : 6 su 80 colonne=
480 caratteri.
Schede da leggere (unita'
2): 20 su 40 colonne=
800 caratteri.
Le informazioni da perforare si trovano a partire
dall'indirizzo 7000 e successivi in senso crescente.
Le informazioni lette sulle schede vengono registra
te a partire dall'indirizzo 7500 e successivi in
senso crescente.
Il programma occupa in memoria la zona compresa tra
gli indirizzi 993 e 1128 (in totale 136 caratteri).
11 programma
La sequenza e' fornita da due parti: una aciclica e
una ciclica.
218
SCHEMA DI 3° PROGRAMMA CON USO DELL' ISTRUZIONE S3P
2• PROGRAMMA
1° PROGRAMMA
C. т
C т
PREPARAZIONE
DELLE ZONE DA
3• PRAGRAMMA
sU0
TOL
SEL
+ C T
ALTRE ELABORAZIONI
STOP
UNITA 2
§ C #
STOP
SUO
TOL
SEL
+ C T
C C T
S C#
STOP
219
ISTRUZIONE
COD.SIMB.
INDIRIZZO
ISTRUZIONE
RIFERIM
; #
1000
#
S3 P
9000
# 0
7000
# 0
750 0
2
% 1
10 7 2
#
8 0
10000
al sottoprogramma di errore
# 0
00 8 0
# #
7 5 6 0
У #
1 0 7 2
#
01
XX X X
#
% 2
10 1 6
#
4 0
0000
al sottoprogramma di errore
# 0
00 4 0
2
# #
8 3 4 0
2
У #
1 0 7 2
X X X X
#
) #
10 7 2
#
C т
C т
sU 0
TOL
SEL
+ C T
S C #
STOP
SUO
TOL
SEL
+ C T
5
O
o
S C #
STOP
SI
1000
1008
1016
1 0 2 4
1032
1040
1048
•1 0 5 6
1064
10 7 2
1080
1088
10 9 6
11 0 4
1112
11 2 0
11 2 8
220
a) La prima parte e' composta da 2 istruzioni cTme
diante le quali si portano gli indirizzi delle
zone impegnate per la prima elaborazione ester-
na, rispettivamente nei registri T1, T2, (ad o-
gni ciclo si somma in T una quantita' pari al nu
mero di caratteri per scheda).
b) La seconda comprende le due sequenze relative al
le unita' in linea interessate.
Percorrendo per la prima volta le 2 sequenze si
attivano le 2 unita' chiamate e si avvia,
ber
ogni unita', un primo ciclo meccanico operativo.
Piu' precisamente
Istruz. SUO
Non effettua il salto non essendo la
unita' 1 occupata.
La SUO ha l' effetto di avviare la
unita' e di predisporre il sincroniz
zatore al trasferimento che viene ef
fettuato nella successiva istruzio-
ne TOL, da memoria dell'unita' cen-
trale a memoria di transito dell'u-
nita' 1.
Istruz. TOL
Trasferisce le informazioni relati-
ve alla prima scheda da perforarsi,
da Memoria principale (a partire dal
l'indirizzo 0000 modificato da T, e
successivi in senso crescente) a me
moria di transito dell'unita' 1. Es
sendo 7000 il contenuto di T1 1' in-
dirizzo iniziale e' 7000.
Effettuato il trasferimento, si av-
via un ciclo meccanico operativo del
l'unita' 1, mentre l'unita' centra-
le passa ad eseguire contemporanea-
mente le successive istruzioni del
programma.
221
Istruz. SEL
Istruz. +CT
Istruz. CCT
Istruz. SC+
222
Se l'eventualita' si verifica salta
al sottoprogramma di errore che prov
vede a ripristinare le condizioni e
sistenti prima del ciclo meccanico
durante il quale l'errore si e' ve-
rificato, affinche' l' operazione pos
sa ripetersi in modo corretto.
Addiziona 80 (n° caratteri di
scheda) al registro T1.
1in z
Confronta il contenuto T, con 560
(n° totale dei caratteri da perfora
re + 80). Dal confronto risulta che
I, non e' uguale alla costante spe-
cificata nell'istruzione.
Effettua il salto all'istruzione suo
successiva, scavalcando lo STOP re-
lativo all'unita' 1 perche' ancora
mancano le condizioni d'arresto.
Il ciclo relativo all'altra unita'
e' analogo a quello sopra descritto.
Dal SC+ dell'unita' 2 si ritorna al
la SUo della unita' 1, e se e' anco
ra in corso il ciclo operativo
questa unita' la condizione di sal-
to e' verificata; ma, essendo occu-
pate in questo caso entrambe le uni
ta' attivate, il salto non viene ef
fettuato, e lo svolgimento del
30
programma si arresta.
Arrestandosi il 30 programma il pri
mo prosegue a partire dall'istruzio
che che immediatamente segue la S3P.
Il 10 programma procede allora fino
a che almeno una delle unita' occu-
pate abbia terminato il ciclo opera
Istruz. SUO
(relativa al
la unita' 1)
Istruz. SUO
(relativa al
la unita' 2)
Istruz. TOL
Istruz. SEL
Istruz. +CT
Istruz. CCT
Istruz. SC+
Istruz. SUO
(relativa al
la unita' 1)
tivo utile e si sia resa disponibile.
Allorquando questa eventualita' si ve
rifica il 10 programma si arresta
il 30 prosegue dal punto in
cui si
era arrestato.
Supponendo che l' unita' resasi dispo
nibile sia la 2 si avra
L'unita' 1 e' ancora occupata, salta
alla istruzione SUO relativa all'uni-
ta' 2.
L'unita'
2 e' disponibile,
assenar
1' unita' gia' attivata si predispone
il sincronizzatore al trasferimento
che viene effettuato nella successiva
TOL.
Trasferisce il contenuto della secon
da scheda alla memoria di transito e
quindi alla memoria principale. L'in
dirizzo iniziale e' ora 7500÷40=7540.
(solite condizioni).
Addiziona 40 in To.
Il confronto non da ancora uguaglian
Za.
Essendosi avuta disuguaglianza
precedente confronto, il salto
ne effettuato.
dal
vie-
L'unita' 1 e' ancora occupata, si ar
resta il 30 programma.
Se l' unita' 1 si fosse nel frattempo
resa disponibile, si sarebbe
invece
223
percorso il rispettivo ciclo e l'ar-
resto del 30 programma si sarebbe ef
fettuato solo sulla suO dell' unita
2.
Allorche' il contenuto di Ti: aumen-
tato di 80 ad ogni + CT relativa, e'
= 560 (quando cioe' tutte le 6 schede sono
state perforate e ci si e' predispo-
sti per una successiva scheda, percor
rendosi il ciclo relativo all'unita'
si avra
Istruz. SC+
Istruz. STOP
Verificatasi ora l' uguaglianza, l'i-
struzione STOP relativa all' unita' 1
non viene scavalcata.
Arresta l'unita' 1 al termine del-
l'ultimo ciclo meccanico di lavoro .
Il programma prosegue passando al ci
clo relativo alla unita 2 sino ache
anche le operazioni di lettura siano
terminate.
L'esecuzione dello STOP dell' unita' 2
arrestera' infine il 30 programma.

## 10.8. Esempio di 30 sequenza con uso della SP*

Generalita'
- Nell' esempio seguente si fa riferimento ad una se-
quenza di 30 programma che pur essendo avviata da
una istruzione SP, ha le singole unita' occupate
mediante l'istruzione S3P*
- La sequenza e' costituita da 2 cicli fondamentali
riferentisi rispettivamente a 2 unita' : unita'
e  2
L'unita' 1 e' supposta essere un perforatore di
schede, l'unita' 2 una stampante in linea.
224
SCHEMA DI 3° PROGRAMMA CON USO DELL' ISTRUZIONE S3P *
PROGRAMMA
3° PROGRAMMA
TsM
T6M
SU0#4
= SN
ELABORA
NACK
POS/ZIONA + (= SH)
ELABORA
TONA ST
POSIZIONA S (=SH)
S3P
SONO TERMINATE LE OPERAL.
UNITA 2
= SN
-SUO
TOL
SEL
TiM
T2M
= SI
= SN
sUO.
TOL
SEL
T3M
TaM
SI
STOP
STOP
-O)
S3P
STOF
PASIZIONA Y = SN
POSIZIONA CE SN
POSIZIONA Y = S/
POSIZIONA O = SI.
POSITIONA O= SI
POSIZIONA 13 2 31
225
- Le zone di memoria interessate dalle istruzioni
TOL vengono preparate mediante sequenze d'istru
zioni di 1° programma indicate sommariamente con
la dicitura •Elabora zona SK (scheda)"
zona ST (stampa)".
- Ognuna di queste sequenze e' preceduta da un
de.
viatore che viene aperto dal 3° programma ad ef
fettuato trasferimento alla memoria unita' in li-
nea di ogni scheda elaborata.
- I registri utilizzati Ti, T2, Tg, T4, associati a
coppie alle unita' 1 e 2, servono per il posizio-
namento dei deviatori "& "e "ß "del primo program-
ma,
•y"e =б : del terzo.
- Il numero delle schede da perforare e da stampar-
si e' imprecisato ma determinabile mediante oppor
tune istruzioni di programma raccolte sotto la de
scrizione generica "sono terminate le operazioni
relative al 3° programma?».
Il programma
La sequenza di 3° programma e' composta
da
parti di cui la prima e l'ultima acicliche.
quattro
a) La prima parte a cui rinvia l'istruzione S3P com
prende due istruzioni TM che aprono rispettiva-
mente i deviatori "y= e »5 * per permettere la
attivazione delle unita' in linea interessate nel
corso dell' elaborazione.
b) La seconda parte e' introdotta dal deviatore y:
che troviamo aperto ogni qualvolta dal 1°program
ma si esige la periorazione di una scheda.
c) La terza parte e' introdotta dal deviatore
65 .
che troviamo aperto ogni qualvolta dal 1°program
ma si esige la stampa di una riga.
226
d) La quarta parte comprende due istruzioni di STOP
relative alle due unita' in linea, condizionate
all'alternativa di fine elaborazione posta
nel
1° programma.
Si hanno pertanto le seguenti operazioni:
Istruzione S3P
(1° programma)
rinvia all'istruzione IgM e IgM
permettendo l'attivazione delle
unita' in linea.
Istruzione TsM
(3° programma)
= apre il deviatore sy. permet-
tendo il ciclo relativo alla u-
nita' 1.
Istruzione. TgM = apre il deviatore "5 .
permet-
tendo il ciclo relativo alla u-
nitar
Istruzione SUO
(# )
= (riferita ad unita' inesistente).
Questa istruzione come si e' det
to ha solo una funzione tecni-
ca : su di essa termina ogni ci
clo di 30 programma; da essa il
ciclo riprende a segnalazione di
unita disponibile.
Istruzione SI o SN = funge da deviatore; viene alter
nativamente trasformata median-
te apposite istruzioni in istru
Zione SI O SN.
Istruzione SUO
= avvia l' unita' 1 e predispone il
sincronizzatore al trasferimen-
to.
Istruzione TOL
= esegue un primo trasferimento da
memoria principale a memoria di
transito e avvia un ciclo mecca
nico di lavoro.
227
Il primo programma, come si e' detto, comprende 2
sequenze interessate rispettivamente alla prepara-
zione dei dati da trasferire su schede perforate e
a stampa.
In ognuna di esse, oltre che le istruzioni di ela-
borazione vera e propria, appaiono un deviatore, un
posizionatore di deviatore, e una istruzione S3P*
con le seguenti funzioni
deviatore dn
(12
sequenza)
: condiziona l'elaborazione di
una nuova scheda all' avvenuto
trasferimento della scheda pre
cedente, nella memoria dell'u
nita' in linea.
Puo' essere costituito da una
istruzione SI che rinvia ad
una istruzione qualsiasi di
servizio (es. CT) che la pre
ceda immediatamente.
posizionatore " Y' : apre il deviatore " y " che per
(1ª sequenza)
mette 1' entrata in ciclo del-
la sequenza di 3 programma re
lativa all' unita' 1.
istruzione S3P*
(1a sequenza)
: avvia un ciclo di 30 program-
ma con conseguente esecuzione
della sequenza relativa all'u
nita
1.
Il deviatore ß , il posizionatore d e la S3P*del
la seconda sequenza hanno funzioni analoghe a quel
le su descritte, ma relativamente all'unita' 2.
Opportune istruzioni di 1° programma permettono in
fine l'avvio del 30 programma sui 2 STOP che ne con
dizionano 1' arresto.
Lo STOP di 1° eseguito immediatamente dopo la SP*
arresta invece il primo programma.
228
Istruzione SEL
Istruzione TiM
Istruzione TzM
Istruzioni:
SI, SUO, TOL,
SEL, Тзм, Тдм
(relative alla
unita' 2)
Istruzione STOP
(1° unita')
Istruzione STOP
(2° unita')
= in caso di errore, salta al sot
toprogramma di errore che prov
vede a riprodurre le condizio-
ni esistenti prima del ciclo
meccanico durante il quale l' er
rore si e' verificato, affin-
che' l'operazione possa ripe-
tersi in modo corretto, (le ca-
ratteristiche dell' istruzione
SEL sono esposte nello schema
relativo).
= trasforma l'istruzione devia-
tore: (SI o SN) precedentemen-
te considerata, in salto effet
tivo; chiude cioe' il deviato-
re "y' che puo' essere riaperto so
lo da una istruzione posta nel
1° programma.
= stessa funzione della TiM,
in a
relativamente al deviatore d° po
sto nel 1° programma il cui po
sizionamento condiziona l' ela-
borazione di una eventuale sche
da da perforare.
= per queste istruzioni valgono
le considerazioni fatte per il
gruppo precedentemente descrit
to ma relativamente all'unita'
in linea N° 2:stampante in li-
nea.
lette di seguito mediante $3P*
di 1° programma permettono 1c
arresto del 3° programma.
229

