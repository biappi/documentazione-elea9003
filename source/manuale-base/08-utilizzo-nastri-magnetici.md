```{sectnum}
---
start: 8
---
```

# Utilizzazione dei nastri magnetici


## Caratteristiche generali

Il nastro magnetico come supporto d'informazione per l'elaborazione elettronica
dei dati e' certamente il piu' funzionale : e' veloce, facilmente trasferibile,
garantisce la buona conservazione dei dati ed e' poco costoso.

Puo' essere usato un numero illimitato di volte sia per la lettura dei dati in
esso immagazzinati che per la registrazione di nuove informazioni su quelle
preesistenti.

Viene avvolto su bobine che possono essere conservate col minimo ingombro
portando ad economia di spazio molto rilevanti.

La durata di una registrazione e' in pratica illimitata, e i dati sono molto
meno soggetti ad alterazioni che su altri supporti.

Le operazioni eseguibili su nastro magnetico sono la registrazione di
informazioni, la lettura delle informazioni gia' registrate.

L'esecuzione di dette operazioni e' affidata ad una apposita apparecchiatura
chiamata "unita' a nastro".

Le unita' a nastro sono dotate di due gruppi di te stine magnetiche
rispettivamente per la lettura e la registrazione, e dei dispositivi di
segnalazione di fine nastro e di arresto delle bobine.

Dall'abbinamento delle caratteristiche tecniche funzionali dei nastri e delle
relative unita' dipen dono i seguenti requisiti

- la velocita' di trascinamento del nastro magnetico

- la densita' di registrazione

- la frequenza di registrazione.

Considerando che su una zona di circa 2,54 centimetri sono registrabili 300
caratteri, e che la velocita' di un nastro puo' andare oltre i 370 centimetri
al secondo, appare evidente come sia impossibile arrestare un nastro sotto le
testine di lettura e registrazione tra due specifici caratteri.

Si deve inoltre osservare che sia la lettura che la registrazione su nastro
magnetico sono possibili solo quando esso funzioni a velocita' di regime: tal
velocita' pero' non e' raggiungibile istantaneamente dallo stato di fermo, ne'
il nastro funzionante a velocita' di regime puo' essere bloccato all'istante a
causa della forza d' inerzia contrapposta dalla bobina.

Si e' reso pertanto necessario il raggruppamento del le informazioni registrate
su nastro in blocchi separati da una piccola zona non registrata chiamata "in
terblocco" Questo intervallo consente al nastro di avviarsi e di raggiungere la
velocita' di regime quando la testina di lettura si posiziona sul primo
carattere del blocco, oppure, una volta letto l'ultimo carattere blocco di
posizionare le testine al centro dell'interblocco stesso.

Questo intervallo di circa 2,5 cm e' diviso in tre zone

    _mm. 7.5
    mm. 24.:

dove A e C indicano le zone occorrenti per l'avvio o l' arresto del nastro, e B
indica la zona riservata per il posizionamento delle testine.

In linea di massima si puo' affermare che quanto piu' lunghi sono i blocchi,
tanto minori saranno le zone di nastro e il tempo perduto per gli avvii e gli
arresti.

Il dimensionamento dei blocchi viene effettuato generalmente in rapporto alla
capacita' della memoria di lavoro dell' elaboratore; ovviamente una memoria di
capacita' ridotta implichera' l'impiego di blocchi di piccole dimensioni che
esalteranno gli inconvenienti citati.


## La registrazione e la lettura del nastro

I caratteri rappresentati nella memoria di lavoro mediante sei bit vengono
riprodotti sul nastro magnetico in modo analogo, con la sola variante che in
luogo di nuclei magnetici si hanno aree magnetizzabili.

La registrazione, che avviene sempre in avanti, e' sottoposta a un duplice
controllo un primo controllo e' quello di disparita', dato da un settimo bit
che viene registrato da un' apposita testina in parallelo con i sei bit
raffiguranti il carattere.

Mediante tale controllo si verifica che non vi sia perdita o generazione spuria
di un bit; infatti il numero delle aree effettivamente magnetizzate compresa
quella di controllo, deve essere sempre dispari per ogni carattere;

- un secondo controllo e ottenuto mediante la lettura e l'immediato confronto
  di quanto e' appena registrato con la informazione originaria.

Risulta evidente l'assoluta garanzia che ne deriva circa una corretta
registrazione dei dati che si vogliono temporaneamente conservare in archivio
bel successive elaborazioni.

Nel caso fosse riscontrato un errore per mezzo dei suddetti controlli, esiste
la possibilita' di appor tare la necessaria correzione prima che la
registrazione prosegua.

Diversamente dalla registrazione la lettura puo' avvenire sia avanti che
indietro, ed il controllo e' ottenuto solo mediante la verifica del bit di
disparita'.

Per scandire i tempi di lettura in corrispondenza di ogni carattere esiste un
bit supplementare chiamato "bit di temporizzazione" che provoca la lettura
della zona di nastro in cui esso e' posto.

Come gia' si e' accennato, le unita a nastro magnetico sono. collegate all'
elaboratore tramite uno specifico governo : governo unita' nastro (GUN).

Il GUN e' dotato di tre memorie

a) la memoria di ricerca, di 128 posizioni, che contiene la chiave di ricerca
per l'individuazione di uno specifico blocco di informazioni.

Mediante questo accorgimento tecnologico, e' possibile infatti raggiungere
qualsivoglia blocco registrato su di un nastro ed apporvi le modifiche o gli
aggiornamenti richiesti dai particolari problemi di lavoro;

DISPOSITIVO DI LETTURA E REGISTRAZIONE FR - 300

b) la memoria di controllo della registrazione, di 256 caratteri, che ha la
funzione di contenere i caratteri registrati ma non ancora riletti;

c) la memoria di trascrizione, la cui capacita' e' di 2048 posizioni.

Quest'ultima memoria permette di eliminare eventuali differenze d' impaccamento
causate dalle di verse condizioni tecnologiche di funzionamento eventualmente
verificatesi in successive operazioni di registrazione, e da modo inoltre di
evitare che in operazioni di trascrizione da nastro a nastro si sommino tra di
loro successive differenze di frequenza di impaccamento.


## Organizzazione delle informazioni su nastro magnetico

Gruppi di caratteri, a seconda della funzione per la quale sono stati creati,
possono costituire le seguenti unita' di elaborazione

    1°
    20
    30
    4°
    50

    la parola
    la scheda
    il blocco
    la sequenza
    l' informazione

La parola e' l'elemento minimo elaborabile e costituisce un dato.

La scheda comprende una o piu' parole e costituisce l'insieme dei dati relativi
a un documento

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
    GAP SPAZIO INUTILIZZATO

Il blocco e' costituito da un numero variabile di schede ed e' creato in
funzione delle caratteristiche tecnologiche del sistema.

La sequenza e' un insieme di blocchi omogenei.

L'informazione comprende tutte le sequenze relative ad un unico flusso di
elaborazione.

Questi elementi sono individuabili sul nastro attraverso speciali caratteri che
li delimitano.

La parola fa eccezione alla regola in quanto e' reperibile anche senza speciali
caratteri di inizio e fine.

La scheda termina col carattere teta (A) solo quando viene operata mediante la
particolare istruzione NDN.

Il blocco inizia e termina col carattere alfa (a )..

La sequenza termina col carattere punto interrogativo che sostituisce uno dei
due alfa che delimitano l'ultimo blocco della sequenza.

La informazione inizia e termina coi caratteri abbinati "moltiplicato per" ( ©
) ed al fa (d).

Nella creazione dei blocchi si devono inoltre osservare le seguenti norme

1. La lunghezza dei blocchi in trascrizione deve essere al minimo di 3
   caratteri inclusi i caratteri di inizio e fine blocco.

   Per esempio sono blocchi accettabili aga oppure d A

2. Per quanto riguarda l'istruzione NDN i blocchi di
   nastro magnetico devono avere come lunghezza mi
   nima 10 caratteri e come lunghezza massima 5000
   caratteri.

3. Per quanto riguarda l'istruzione TN la lunghez-
   za dei blocchi puo' essere al massimo di 5000 ca
   ratteri.

NB a) Nella casella N° 5 e' indicato solo il tempo necessario alla fase
preparatoria; la durata della fase esecutiva dipende infatti dal numero di
caratteri o di blocchi che si voglio no operare.

b) Le segnalazioni di macchina relative alle istruzioni SFS, SFI, SN1, SNs,
vengono annullate ad avvenuta lettura dell'istruzione interessata.

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

: indirizzo di memoria a partire dal quale vengono registrati i caratteri da
nastro

: il registro Im puo' modificare sia 1' indirizzo IIII cheil nome del nastro ni

: legge dal nastro montato sull' unita' ni (specificata in p7) alla Memoria,
procedendo in avanti

a) Il trasferimento avviene dal segnale di inizio blocco (o , ? ) al segnale di
fi ne blocco (o, ? .

b) I caratteri di inizio e fine blocco (d, ? ) vengono trasferiti in memoria

c) I caratteri letti sul nastro vengono registrati in Memoria a partire
dall'indirizzo III e per indirizzi crescenti

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

: il registro Im puo' modificare sia l'indirizzo IIII che il nome del nastro ni

: legge dal nastro montato sull'unita' ni (specificata in p7) alla Memoria, procedendo indietro

a) Come la LNa, ma con senso di marciaindietro del nastro e per indirizzi decrescenti.

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

:indirizzo di memoria a partire dal quale vengono registrati i caratteri

:il registro Im puo' modificare sia l'indirizzo IIII che il nome del nastro ns

: registra dalla Memoria, sul nastro montato sull'unita' ns (specificata in
p7), procedendo in avanti

a) Il trasferimento ha inizio dall'indirizzo IIII della Memoria e prosegue fino
al segnale di fine blocco (X . ?'), per indirizzi crescenti.

b) All'indirizzo IIII deve essere registrato il segnale di inizio blocco (d,
?).

c) Il blocco da registrare deve essere di almeno tre caratteri, inclusi i
segnali di inizio e fine blocco

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

: indirizzo di memoria a partire dal quale si trasferisce alla memoria del GUN

: il registro Im puo' modificare l'indirizzo IIII trasferisce dalla memoria
dell' unita' centrale, a parti re dall' indirizzo IIII e per indirizzi
crescenti, alla memoria del GUN, i caratteri comprendenti la parola chia ve che
sara' usata nella ricerca su nastro.

a) La ricerca puo' avvenire con una parola chiave avente al massimo la
lunghezza di 128 caratteri: non e necessario che i caratteri interessati siano
adiacenti purche' le posizioni non interessate alla ricerca siano diesizzate:
il trasferimento della parola chiave dalla memoria al GUN si arresta quando
viene letto un dopo un carattere diverso da d

b) il carattere ("" o "?") che obbligatoriamente inizia ogni blocco di nastro, nor
deve essere considerato; nel senso che la parola chiave non deve contenerlo. ne
deve contenere al suo posto un carattere #.

c) se si desidera che il confronto avvenga con i caratteri registrati su nastro dal
alla (n +m) a posizione di ogni blocco (n +m < 128) la parola da tra.
sferire dovra comprendere inizialmente n car atteri - quindi la parola chiave
di m caratteri.
    e finalmente il carattere l
    esempio': per n = 4
    ####4812318
    a bcd487231n
    impostazione parola chiave
    da trasferire nel cin
    organizzazione del nastro
    nella zona corrispondente
    alla parola chiave.

d) il blocco ricercato sara' quello contenente la parola chiave trasferita nel
gun, in mancanza di questo, il blocco contenente una parola chiave di valore
superiore a quella trasterita

e) se nella ricerca la macchina non incontrasse alcuno di tali blocchi, per
provocare l'arresto dell'unita° a nastro sara° necessario prevedere sul nastro
stesso un ultimo blocco fittizio contenente tanti @ quanti sono i caratteri che
esprimone

    intero codice
    esempi
    parola chiave
    ## 15798
    blocco titt1zic

f) la ricerca e' convalidata per tutti i caratteri che nella parola trasferita
dalla prn sono diversi dal carattere • # • ; si rende quindi possibile la
ricerca automatica di blocchi con chiave spezzata.

    esempio :
    # # # 251 # # 359 # a 0
    168

    trascrivi nastro
    tn
    gun
    n1 ns
    b b b b
    im § (111010)
    10
    ng
    ds
    в в в в
    nome del nastro in lettura
    nome del nastro in scrittura

: numero di blocchi da trasferire da nastro a nastro
: il registro im puo' modificare sia il numero bbbb che il nome del nastro ns
: trascrive dall' unita' a nastro ny alla unita' anastro
ns un numero bbbb di blocchi.

a) se la in e immediatamente preceduta da una prn si ha che

1) nelle posizioni p3 + p6 e' registrato il carattere x ;

~ istruzione trascrive da nastro , a nastro un numero imprecisato di blocchi
l'ultimo dei quali e' quello che nelle sue posizioni iniziali contiene una parola uguale o maggiore di quella trasferita nella memoria del gun per
mezzo della prn

b) con unita' lettura inesistente, codificata # n, . # ## # # $, il nastro dell'unita' in registrazione viene cancellato totalmente.

c) se durante la trascrizione dei bbbb blocchi si verifica un errore di registrazione la macchina ne da segnalazione e si arresta nel blocco dove si e verificato
l'errore stesso.

d) la lunghezza di un blocco non puo' superare i 5000 caratteri

    alo
    (al
    169
    est, int, gun
    prepara ingresso da nastro
    x х
    i i i i
    im
    r (111100)
    pin
    10
    x x
    iiii
    im

: posizioni non utilizzate

: indirizzo di memoria a partire dal quale si registra
da n1 (specificato nell'istruzione nan seguente)

: il registro im puo' modificare l'indirizzo iiii
fissa l'indirizzo di memoria a partire dal quale vengono registrati i caratteri letti sul nastro ni

a) l'istruzione pin deve precedere immediatamente la nan

est, int, gun
n1 as
da nastro a nastro no
iiii im e (110000)
nan
10
ni
"s
iiii

: nome del nastro in lettura

: nome del nastro in registrazione

: indirizzo di memoria a partire dal quale si registra su
ns

: il registro im puo' modificare sia l' indirizzo iiii che
il nome del nastro ns

: registra dalla memoria su nastro montato sull' unita' ns
(specificata in p7) e simultaneamente legge dal nastro
montato sull'unita' n (specificata in p8) su una diver
sa zona di memoria.

a) ciascun carattere letto in memoria a partire dall'indirizzo ilil specificato dal
la nav viene trasferito sul nastro ng; ciascun carattere letto dal nastro nj vie
ne registrato in memoria a partire dall'indirizzo iiii specificato dalla pin im-
mediatamente precedente

b) se l'indirizzo specificato dalla pin e' uguale o maggiore di quello indicato dal
la nan, puo' accadere che 1 caratteri prelevati da n vadano a sostituire in
memoria i caratteri che avrebbero dovuto essere piu' tardi registrati su n.
e con le istruzioni pin-nan possono essere operati blocchi di lunghezza variabile.

d) i due nastri funzionano in avanti; l'istruzione ha termine quando sono stati
letti (sul nastro n' e in memoria) entrambi i caratteri di fine blocco.

e) non e' possibile porre ns o ni inesistenti (carattere #)

170
no
da nastro, seguendo una direttrice a nastro
ndn
est, int, gun
n1 ns
iii i
im § (110110)
10 +1
ni
ns
iiii
im

: nome del nastro in lettura

nome del nastro in registrazione

: indirizzo della direttrice

: il registro im puo' modificare sia l'indirizzo iiii che
il nome del nastro as

: registra dalla memoria su nastro montato sull' unita' n e simultaneamente legge dal nastro montato sull'unita'
di sulle stesse zone di memoria.

a) ciascun carattere letto da nastro va ad occupare la posizione di memoria da cui
si e' immediatamente prima prelevato il carattere da registrare.

b) le informazioni vengono lette e registrate a gruppi di caratteri la cui fine e'
contraddistinta dal carattere "" per es

    1234567890

c) i blocchi ed i gruppi corrispondenti devono avere la stessa lunghezza nei due nastri ns e n]

    axxxx00xx00xxx00xx00 xxxxxo

d) la lunghezza di un blocco organizzato per essere operato con landn puo'
variare da 10 a 5.000 caratteri.

e) il primo gruppo è' costituito dal carattere di inizio blocco, seguito immediatamente o dal primo carattere "o" ed e' quindi composto di due caratteri'; "oo"
oppure dal contenuto della prima informazione ed e' allora composto da un numero di caratteri pari a quelli dell'informazione + 1.

    in memoria,
    decrescenti,
    e
    ta lairettrice"
    a partire dall'indirizzo iiii (modificabile da im)
    indirizzi
    registrata una lista consecutiva di indirizzi di memoria chiama
    i ognuno di questi indirizzi e' l'indirizzo di memoria a partire dal quale, per
    inda1221 crescent1, vengono prelevati e sostituiti i caratteri costituent
    un gruppo.

    2) il primo indirizzo di destra della direttrice e' l'indirizzo del gruppo
    con
    tenente l' o di inizio blocco, mentre l'ultimo indirizzo di sinistra corri
    sponde o all'indirizzo dell' o di fine blocco o all'indirizzo di
    sinistr:

    del gruppo che lo contiene.

    il numero (n) degli indirizzi di una direttrice puo' essere quindi costituitc
    1 dal numero delle informazioni costituenti il blocco:
    2) dal numero delle informazioni costituenti il blocco
    più' l'indirizzo del gruppo "°e = di inizio blocco:
    n+
    171

    3) dal numero delle informazioni costituenti il blocco
    piu' 'indirizzo dell'∞ di fine blocco

    4) dal numero delle informazioni costituenti il blocco
    piu' l'indirizzo del gruppo " o
    e. di inizio blocco
    e l'indirizzo della di fine blocco
    axxoxxxoxxx0xxx0xxxxxx0
    ig
    12 з i 15 i6
    hoxxxoxxxoxxxoxxxaxxxo
    titz 1s 1s is io
    doxxxaxxxaxxxaxxx00
    з in ig
    xxxaxxxoxxxaxxxoxxx00
    x12
    13
    ta 1s 16
    6 igigigigi1.
    direttrice

g) i due nastri funzionano in avanti : l'istruzione ha termine quando viene
letto il carattere di fine blocco.

h) ponendo n , inesistente (carattere ) si esegue solo il trasferimento da ni
vers( memoria secondo l'ordine stabilito dalla direttrice.  analogamente,
ponendo nj inesistente (carattere#) si esegue solo il trasferimen- to da
memoria verso " secondo l'ordine stabilito dalla direttrice.

    de e
    o
    olo e 06
    "
    o ar
    nastro in registrazione
    memoria principale
    direttrice
    &li
    a do b de c 00
    o
    06 e
    2
    nastro in lettura
    disponi unita' e blocco
    dub
    gun
    n
    b b b b
    im
    n (111000)
    10
    j
    rrrr
    im
    n

: nome del nastro interessato

: indicazione del senso di marcia

: numero dei blocchi del nastro interessati dall'istruzione

: il registro im puo' modificare sia il numero bbbb che il carattere indicato
in j

: fa procedere il nastro montato sull' unita' n (specificata in p8) del numero
di blocchi indicato in bbbb, in avanti o all'indietro, secondo il carattere
indicato in j.

a) nelle posizioni da p3 a p6 non e' indicato un indirizzo di memoria

b) se nel carattere indicato in j il bit "a" e' zero, il numero di blocchi e'
uguale a bbbb; se invece e' "¡" • il numero di blocchi e' 10.000 + bbbb.

c) se nel carattere indicato in j il bit "d' e' zero, lo svolgimento avviene in
avanti '; se invece e' "i" avviene all'indietro.

d) se durante l' esecuzione della presenta istruzione si verifica un errore, la
macchina ne da indicazione e procede fino alla fine della conta dei blocchi

    174
    i
    esterno, gun
    n
    cancella nastro
    711 in p (111011)
    kn
    10
    n
    i ii i
    im
    p

: posizione non utilizzata

: unita' a nastro interessata

: indirizzo di memoria che determina l'inizio dell'operazione

: il registro im puo' modificare sia l' indirizzo iiii che 1 nome del nastro

: cancella il nastro montato sull' unita' n, per una lunghezza determinabile in pollici

a) la cancellazione ha luogo durante il tempo impiegato dalla macchina a
percorrere le posizioni di memoria che vanno dall'indirizzo ill fino al primo
carattere d (alfa).

b) la porzione di nastro che ne risulta cancellata e' determinabile con la
formula l = n.  v/f dove l = lunghezza nastro cancellato, in pollici; n =
numero caratteri intercorrenti fra l'indirizzo iiii ed il primo carattere d
(alfa);

: velocita' del nastro in pollici per secondo:

f = frequenza di lettura della memoria, in caratteri al secondo

c) la kn viene normalmente utilizzata per cancellare una porzione di nastro.

d) il contenuto della memoria rimane inalterato. all'indirizzo iiii non deve essere
registrato il carattere @ (alfa).

e) per comodita' di calcolo indichiamo una formula approssimata per determinare lo
spazio di nastro cancellato

l = 2,1 + n. 1,98. 10-3

dove n e' il numero di caratteri intercorrenti tra l'indirizzo iiii ed il primo
espresso in centimetri, con una approssimazione di + 1/2 centimetro.

175
unita' a nastro
x n
avvolgi nastro
x x x x
im
av
(001101)
10
n
i'm
x xxx : le posizioni p3, p4, p5, p6, p8 non sono utilizzate

: nome dell' unita' a nastro interessata

: il registro im puo' modificare il nome dell' unita'a nastro n

: riavvolge all'indietro la bobina montata sull'unita' nastro n fino al termine
del nastro.

a) l'operazione di riavvolgimento non impegna il 'gun ma solo l'unita'
interessata, pertanto possibile far eseguire simultaneamente :

1) piu' operazioni di riavvolgimento purche' interessino unita' diverse;

2) una qualsiasi delle istruzioni relative ai nastri, di tipo ln, ndn, pry,
ecc. purche non interessino l'unita bì durante l'operazione di riavvolgimento:

1) una istruzione riguardante la stessa unita' resta bloccata fino a terminata
esecuzione dell'av;

2) l'eventuale istruzione sno relativa alla stessa unita' viene eseguita.

c) se il gun e' impegnato in una normale operazione, non e' in grado di
ricevere struzioni di riavvolgimento.

    176
    salta se fine sequenza
    sfs
    interno
    (111000)
    n
    is
    i iii im 0
    10 0 15

a) salta se l'ultimo blocco letto da nastro inizia o termina con il carattere
"?" di fine sequenza.

b) l'istruzione non viene eseguita se e' in corso un'eventuale operazione di
nastro.

c) la segnalazione relativa a questa istruzione puo' essere , annullata oltre
che dalla lettura dell'istruzione stessa anche dalla lettura di una istruzione
qualsiasi di nastro

    salta se fine nastro in lettura
    interno
    (111011)
    pis
    iiii im 0
    sn1
    10 0 15

a) salta se e' terminato il nastro in lettura.

b) l'istruzione non viene eseguita se e' in corso un'eventuale operazione di nastro.

    salta se fine nastro in registrazione
    interno
    (111111)
    q is
    sns
    i i i i im 0
    10 0 15

a) salta se e' terminato il nastro in registrazione.

b) l'istruzione non viene eseguita se e' in corso un'eventuale operazione di nastro

    177

    salta se fine informazione

    sei
    interno
    (111101)
    is
    .i i i i
    i'm 0
    10 o 15
    11 09

a) salta se l'ultimo blocco da nastro termina con il carattere di fine
informazione

b) l'istruzione non viene eseguita se e' in corso una eventuale operazione di
nastro.

c) la segnalazione relativa a questa istruzione puo' essere annullata oltre che
dalla lettura dell'istruzione stessa anche dalla lettura di una istruzione
qualsiasi di nastro


salta se nastro occupato
sno
interno
( - - - - ==)
n
is
ii i i
im 0
10 0 15

a) salta se l'unita' a nastro "n" e' gia' impegnata

b) il carattere di eventualita' non e' fisso, ma e' il carattere che
contraddistin- gue l'unita a nastro interessata.

c) la segnalazione di nastro occupato viene annullata dalla lettura del primo
salto incontrato dopo l'esecuzione della presente istruzione.

178
salta su condizione automatica
sca
interno
(110101)
(
is
i i i i
im 0
10 0 15
is
iiii
0

:carattere di eventualita'

: registro che ricorda l'indirizzo della posizione p8 dell' istruzione

: indirizzo dell'istruzione alla quale si deve saltare

: il registro im puo' modificare sia l'indirizzo iiii che il nome del registro
is

: salta se si e' verificata una delle seguenti eventuali

ta' : riconoscimento di carattere chiave, unita' nastro non disponibile,
condizione d'errore o condizione esterna se4.

a) l'analisi di quale condizione si e verificata va eseguita mediante un
sottoprogramma con il quale si possono ricavare le indicazioni particolari
relative a ciascun organo e al tipo di segnalazione da esso rilevata

b) generalmente l'istruzione sca viene posta di seguito a una istruzione di nastro
di tipo ln, ndn, -nan.

c) la sua esecuzione dipende dall'impegno del canale interno: se questo e'
libero la sca viene eseguita, altrimenti resta bloccata

d) per la ndn e pin -nan la sca non viene eseguita fino ad ultimata operazione
di lettura e registrazione, permettendo in tal modo alle eventuali segnalazioni
di fs, fi, ni e ns di rivelarsi prima dell' effettuarsi della sca.

e) questo non avviene per la ln che occupando nell'esecuzione solo il canale
esterno permette all'eventuale sca che segue d'essere eseguita quando e' ancora
in corsc la lettura del nastro.

s1 puo' pero' ovviare a questo inconveniente facendo precedere la sca da una
del- le istruzioni che bloccano il proseguimento del programma in cui sono
registrate, fino a terminata esecuzione dell'operazione di nastro in corso.

e' evidente che con una tale organizzazione si ottiene l'esecuzione della da
pro prio quando le possibili condizioni si siano verificate.

f) qualora l'istruzione sca rinviasse ad una istruzione diversa da salto
verrebbero annullate tutte le segnalazioni memorizzate per conto
dell'istruzione stessa.

g) l'esecuzione di uno dei salti e del relativo programmino annulla la
segnalazione in questione.

h) sfruttando la caratteristica g) e' conveniente far precedere ogni programma
da uni istruzione sca seguita da istruzione diversa da salto per annullare
eventuali se.  gnalazioni rimaste memorizzate da precedenti elaborazioni.

    esempio
    sca
    ets
    0016
    im
    f
    0008
    ma
    ll
    iiii
    im
    f
    0016
    179
    schema riassuntivo
    memoria - nastri
    nastro - memoria - nastro
    nastro - nastro
    nastro
    salti
    lna
    ndn
    tn
    dub
    lni
    pin
    sfs
    kn
    int

    particolarità' dei nastri
    in formazioni . sono registrate e lette carattere per carattere e
    cioe' in serie.
    bit
    ad ogni carattere corrispondono
    a
    bit di sposti
    uno accanto all'altro nel senso della larghezza
    del nastro l6 hit definiscono un carattere.
    :1 70
    e' il bit di disparita' e 1'8° il bit di temporiz
    harione).
    caratteri
    cneciol; dei
    nastri
    ..
    x) il carattere "o " segnala l'inizio e la fine di un blocco:
    2141 carattere " ? " inizia e termina il primo
    ¡altimo blocco di una sequenza;
    w) il carattere " @ " inizia e termina il primo
    jaltimo blocco di una informazione;
    a) il carattere " segra le informazioni co
    stituenti un blocco organizzato per essere
    operato con la ndn.
    numero dei
    conattori
    - registrabili in una bobina di nastro con blocchi
    di n caratteri in media.
    dato dalla seguente
    formula:
    60 000
    n+
    -200
    unita' nastro - collegabili al
    gin sono al massimo 20.
    i caratteri che le distinguono sono :
    193456789~dabcdefghi
    istruzioni nastri
    rn
    prn
    nan
    av
    sns
    sfi
    scabiceco
    canali
    lna
    lni
    guin
    rn
    prn
    ndn
    pin
    ~a4 int cin
    nan
    in
    dub
    kn
    av
    gin
    ast.. clin
    uni tal noe.
    ses
    sni
    sn
    sfi
    sno
    sca
    interno
    sno
    tempo
    in periodi di cifra
    10
    900
    lo
    sca
    configurazione
    ~ za
    ffffffe
    caratte
    i =
    .a
    o o o

