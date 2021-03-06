```{sectnum}
---
start: 10
---
```

# La terza sequenza di programma


## Generalita'

1. All' unita' centrale del sistema Elea 9003 possno essere collegate unita' in
   linea capaci di funzionare simultaneamente e di operare senza interrompere
   lo svolgimento del 10 e del 20 programma

2. Le unita' collegabili sono
   - lettori di schede
   - perforatori di schede
   - lettori di nastro perforato
   - lettori e perforatori di schede
   - stampanti

   Le varie unita' numerate da 1 a 10 vengono distinte in fase di elaborazione
   dal proprio numero in dicativo.

   Nell'uso normale troviamo simultaneamente collegate unita' di diverso tipo
   anche se teoricamente esiste la possibilita di porre in linea dieci unita'
   con medesima funzione.

3. Ciascuna di queste unita' e' diretta da un proprio governo che contiene l'
   apparecchiatura logica necessaria al suo funzionamento e una memoria a nuclei
   sufficiente a contenere i caratteri necessari per ogni ciclo meccanico di
   lavoro: una riga stampa, una scheda, un blocco di nastro perforato (max. 104
   caratteri).

4. L' alternarsi dell' entrata e dell'uscita dei caratteri dalle varie memorie,
   la distribuzione dei dati alle diverse unita' collegate e la logica che le
   regola, sono affidate ad un sincronizzatore che armonizza tutte le operazioni
   di terzo programma.


## Caratteristiche logiche del 30 programma

1. L'ordine di lavoro alle singole unita' viene trasmesso dall' unita'
   centrale, che procede quindi in parallelo con esse, senza che queste ultime
   rallentino ne' intralcino le operazioni interne; il sincronizzatore
   provvede a smistare gli ordini e le informazioni alle diverse
   apparecchiature; ogni unita' chiamata ad operare esegue il lavoro secondo
   le peculiari modalita ed il proprio tempo meccanico.

   Le memorie di transito delle singole unita' di estrazione vengono fornite
   delle informazioni in uscita dall' unita' centrale che provvede pure a
   prelevare le informazioni in entrata dalle unita' di introduzione.

   Non e' necessaria ad ogni trasferimento dao a unita' centrale un'
   operazione di azzeramento delle memorie di transito in quanto queste vengono
   azzerate automaticamente.

2. Durante il collegamento con il calcolatore, le unita' di introduzione ed
   estrazione assumono tre diversi stati possibili;

   - "inattiva" l'unita' che pur collegata con l'unita' centrale attraverso il
     proprio governo, non sia avviata;

   - "avviata" l'unita' che sia stata chiamata ad operare almeno una volta
     mediante un'istruzione. Lo stato di "avviata" puo' durare per molti cicli
     meccanici di lavoro;

   - "occupata" l' unita' che oltre ad essere avviata sia stata effettivamente
     messa in funzione da una istruzione esecutiva.

    Ogni unita' avviata ed occupata passa automaticamente allo stato di
    avviata-non occupata al termine di ogni ciclo meccanico di lavoro; passa al
    lo stato di inattiva mediante un' apposita istruzione di STOP.

    La simultaneita' di esecuzione delle operazioni interne della macchina e
    del lavoro delle unita' collegate e' ottenuto mediante una terza sequenza
    di istruzioni eseguibili dall' elaboratore parallelamente alle sequenze di
    1?? e 20 programma.

    L'uso delle diverse sequenze non comporta intralci ne' inconvenienti alla
    corretta e coerente esecuzione delle istruzioni dei singoli programmi.

    Esistono prestabilite priorita' sul canale interno, tre diversi registri
    indirizzo istruzioni, e dispositivi distinti per ogni programma per la
    conservazione separata delle seguenti segnalazioni circa determinate
    eventualita' verificabili nel corso dell' elaborazione: risultato dei
    confronti (=, !=, >, <) e overflow nei registri e nella memoria.

    Si deve inoltre osservare che contrariamente al le istruzioni di canale
    esterno che vengono poste preferibilmente sul 2?? programma, per sole
    ragioni di logica, le istruzioni di comando delle apparecchiature in linea
    devono essere raccolte obbligatoriamente sul 30 programma per ragioni
    funzionali. Questa disposizione risulta inoltre logica specie se si
    considerano le norme che stabiliscono le priorita sui canali.

La priorita' sul canale interno e' riservata:

- prima al 30 programma che per l'esecuzione delle istruzioni che lo riguardano
  non richiede il canale interno se non per periodi di tempo assai limitati;

- quindi al 20 programma che si svolge nella massima parte con impegno del solo
  canale esterno; infine al 1?? programma che impegna il canale interno sia in
  fase preparatoria che in fase esecutiva.

E' evidente che dette priorita' sono studiate in modo da permettere ad ogni
programma la massima conti nuita senza che l'esecuzione degli altri programma
subisca per questo eccessivi tempi di attesa.

Risulta pertanto logico che dovendo i tre programmi ricorrere al canale interno
per il loro svolgimento, su questo canale debba aver la precedenza il programma
che meno lo impegna.

In pratica il 30 programma cede la precedenza sul canale interno:

1. ogni qualvolta le memorie di transito dei governi delle unita' in linea
   risultino fornite dei caratteri necessari ad un ciclo meccanico di lavoro;

2. ogni qualvolta si verifichi un impedimento all'esecuzione di una delle
   istruzioni registrate in detto programma.

La precedenza al terzo programma invece non viene immediatamente ceduta in due
particolari casi:

1. allorquando sia stata letta su 10 o 20 programma una istruzione preparatoria
   tipo PUM, PRN, PIN.  Nel qual caso il canale interno viene ceduto solo dopo
   l'esecuzione dell'istruzione esecutiva tipo MEM, +MM, -MM , TN, NAN;

2. allorquando sia stata letta ed eseguita su 10 o 20 programma una istruzione
   di salto. Nel qual caso il canale viene ceduto solo dopo l'esecuzione
   dell'istruzione a cui il salto rinvia.

L?? terza seauenza di programma:

1. puo' essere avviata da una istruzione particolare di salto S3P, registrata
   indifferentemente nel 1?? o nel 20 programma;

2. puo' essere frazionata in piu' sequenze singolarmente avviabili ma non
   contemporaneamente eseguibili in quanto l' elaboratore puo' essere impegnato
   nell' esecuzione di una sola sequenza di 30 programma;

3. puo' eseguire istruzioni di qualsiasi genere pur avendo come funzione
   specifica i comandi relativi alle apparecchiature in linea.


## Fasi di svolgimento del 30 programma

1) Una istruzione S3P da inizio all'esecuzione della sequenza. Appositi
registri, distinti da quelli con ugual funzione, di 10 e di 20 programma,
conservano gli indirizzi e le segnalazioni relative alle istruzioni di 30
programma.

2) Vengono quindi percorse le istruzioni della sequenza secondo le normali
modalita' di funzionamento, ma con i seguenti effetti

    a) l'istruzione suo avvia l' unita interessata;

    b) l'istruzione TOL esegue un ciclo completo di lavoro: trasferimento dei
    caratteri alla memoria di transito ed elaborazione relativa

    c) le altre istruzioni compiono la loro normale funzione.

3) Ritorno alla 1?? istruzione SUO eseguita, nelle seguenti possibili condizioni

    a) l'unita' relativa alla SUO non e occupata; nel qual caso il salto non
    viene effettuato e si eseguono l'istruzione TOL e successive;

    b) l'unita' relativa alla SUO e occupata ma almeno una delle altre unita'
    si e' resa disponibile; nel qual caso viene effettuato il salto all'istruzione
    indicata dalla SUO e la sequenza viene percorsa fino alla prossima suo che si
    trovi nella condizione c);

    c) 1'unita relativa alla SUO e occupata e cosi' pure tutte le altre unita';
    nel qual caso il 30 programma si arresta su detta istruzione.

4) Esecuzione infine degli STOP relativi alle unita' in linea, con i seguenti
possibili effetti:

    a) se lo STOP viene eseguito quando ancora non e' letto almeno uno degli altri
    STOP esistenti nella sequenza di 3?? programma, l' unita' interessata passa allo
    stato di "inattiva" senza che lo svolgimento del programma venga interrotto;

    b) se lo STOP e' eseguito dopo 1' avvenuta lettu-
    radegli altri STOP 1' unita' passaallo stato di inat
    tiva ed il programma si arresta.


## Funzione e logica delle istruzioni s3P, TOL, STOP

L'istruzione S3P

1. comanda l'inizio di una sequenza di 30 programma;

2. attiva tutte le unita che vengono percorse dal 1?? ciclo di 30 programma;

3. viene riciclata qualora sia letta mentre e gia' in corso sequenza di 30
programma:

4. puo' riavviare una sequenza di 3?? programma non appena ne sia terminata una
precedente.

L'istruzione SUO permette

1. di avviare l'unita a cui e riferita;

2. l'arresto del programma nel caso che nessuna unita sia disponibile;

3. il riavvio del programma ad ogni segnalazione di unita disponibile.

- Dopo l'arresto su una SUO il riavvio del programma avviene con la lettura
  dell' istruzione stessa

- Nel caso la suo richiamasse una unita' non collegata, il calcolatore non
  esegue la sequenza di programma relativa a tale unita'.

L'istruzione TOL deve seguire immediatamente nel programma la SUO relativa.
Essa permette:

1. di eseguire l'effettivo trasferimento dei dati fra la memoria dell' unita'
    centrale e le memorie di transito delle unita' in 'linea';

2. di predisporre l'unita' in linea all' esecuzione del ciclo operativo
    successivo: autorizzazione alla prossima lettura, perforazione o stampa,
    preceduta o seguita dall' azzeramento della memoria di transito.

L'istruzione STOP appare generalmente al termine di ogni sequenza d' istruzioni
relative ad una unita' in linea.
Essa permette:

1. di riportare una unita' allo stato di inattiva non appena sia stata
   completata l'operazione per la quale era stata chiamata;

2. di arrestare il 30 programma una volta eseguiti tutti gli STOP delle unita'
   avviate.

Va rilevato che l'istruzione STOP non arresta il ciclo operativo in corso, ma
le operazioni atte a predisporre l' unita' in linea al successivo ciclo di
lavoro dopo l'azzeramento automatico della memoria di transito.


## L'istruzione SP\*

Mediante questa istruzione si vuole ovviare all'inconveniente generato dall'uso
della sola istruzione S3P normale, che non permette di realizzare un meccanismo
dinamico di sovrapposizione tra 1?? o 20 programma e 3?? programma, basato su uno
scambio di richieste e di segnalazioni.

Caratteristica logica dell'istruzione S3P\* e' infatti quella di rendere
possibile un ciclo intero di 30 programma ogni qualvolta se ne presenti la
necessita' durante lo svolgimento dei primi due programmi, permettendo in tal
modo di avviare una sequenza relativa ad una unita' in linea temporaneamente
inutilizzata.

Differenza rilevante tra l'istruzione S3P e l'istruzione S3P\* e' che mentre la
prima attiva le unita in linea, la SP\* puo' soltanto avviarle.  Ne consegue
cheA

1?? tutte le unita' interessate dalla sequenza di 30 programma devono essere
attivate dall'istruzione S3P e conseguentemente percorse durante il 1?? ciclo di
3?? programma;
2?? una unita' resasi inattiva non puo' essere riattivata se non dopo che tutte
le unita' considerate nel 30 programma siano tornate allo stato di inattive.

Si osservi inoltre che l'uso della istruzione S3P\* richiede 1' impiego nel 30
programma di una istruzione SUO relativa ad una unita' inesistente (SUO su
unita' fittizia).

L' istruzione SUO su unita' fittizia deve apparire in testa alla sequenza di
istruzioni ed essere letta nel 1?? ciclo di 30 programma.


## L'organizzazione di un 3?? programma che prevede l'uso della istruzione S3P\* dovra' pertanto essere legata alle seguenti norme.

1) Sul 1?? o 2?? programma deve essere registrata una istruzione S3P che permetta
l'attivazione di tutte le unita' interessate all' elaborazione.

2) La S3P deve rinviare direttamente o indirettamente all'istruzione SUO su
unita' fittizia che si trova in testa al 30 programma. Solo in questo modo l'
unita' puo' risultare facente parte del 30 programma.

3) Le sequenze relative ad ognuna delle unita' in linea interessate devono
essere precedute da un de viatore che resta aperto durante il primo ciclo di 30
programma.

4) Se una unita' non e' da utilizzarsi immediatamen te, il deviatore che ne
introduce la sequenza relativa deve venir chiuso, cioe' indirizzato al
successivo deviatore, mediante una istruzione apposita che lo deve seguire nel
programma.

5) Successivi posizionamenti dei deviatori possono essere disposti da
istruzioni registrate indiffe rentemente in uno dei tre programmi a seconda del
le necessita' di programmazione.

6) L'istruzione SP\* non deve rinviare alla SUO su unita' fittizia ma
all'istruzione che la segue immediatamente perche' la lettura della SUO
provocherebbe la disponibilita' del canale interno per il 10 o 20 programma.

Ripresa automatica del canale interno da parte del 10, 20 e 30 programma.

 - Il 10 o 20 programma riprendono la precedenza se si verifica nel 30 una
   delle seguenti eventualita'

    1. tutte le unita' in linea sono allo stato di "occupata" e il 30 programma
    e' fermo sull'istruzione SUO in corrispondenza della quale tale eventualita'
    si e' verificata (programma che prevede il solo uso dell' istruzione S3P);

    2. tutte le unita' in linea sono allo stato di "occupata" ed il 30
    programma e' fermo sull'istruzione SUO su unita' fittizia (programma che
    prevede l'uso dell' istruzione $3P\*).

- Il 30 programma riprende la precedenza se e' presente almeno una delle
  seguenti condizioni:

    1. una unita' precedentemente occupata sie' resa disponibile;

    2. richiesta di ciclo di 30 programma da parte del 1?? o 20 programma
    mediante l'istruzione S3P\*;

Nell'organizzazione che prevede l'uso della S3P\* nonostante l'arresto sulla
SUO su unita' fittizia, nel riavvio di un ciclo di 30, detta istruzione non e'
considerata e viene invece letta immediatamente la istruzione che segue;

con l'uso della sola SP l'istruzione SUO da cui il programma riparte viene
viceversa letta ed even tualmente eseguita.

Automatismo relativo ai segnali di unita' disponibile Il 30 programma,
indipendentemente dall'uso della S3P\*, viene percorso fintanto che perdura la
segnala zione di unita' disponibile.
Questa segnalazione ha tuttavia caratteristiche diverse a seconda
dell'organizzazione scelta.

Infatti coll' uso dell'istruzione SUO su unita' fittizia, eventuali
segnalazioni di unita' disponibile permangono solo temporaneamente, di modo che
se per una ragione qualsiasi (chiusura di un deviatore) l'unita' disponibile
non viene occupata durante il ciclo richiesto, tale segnalazione si perde, e
solo un nuovo comando originato da una S3P\* o da una nuova segnalazione di
disponibilita' puo' permettere un ciclo di lavoro all' unita' resasi
precedentemente disponibile.

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

: registro che ricorda l'indirizzo della posizione p8 dell'istruzione

: indirizzo dell'istruzione posta nella sequenza di programma esterno alla
quale si deve saltare

: il registro Im puo' modificare sia l'indirizzo IIII che il nome del registro
Ts

: salta se si e' verificata l'eventualita a, L'istruzione posta nel 10 e 20
programma comanda l'inizio di una sequenza di programma esterno.  Se e' gia' in
corso una sequenza di programma esterno

1. la presente istruzione viene riciclata finche' la sequenza in corso non e'
terminata;

2. terminata l'esecuzione della sequenza di programma esterno, la S3P puo'

    Salta al programma esterno 
    S3P
    interno
    (010101) =
    Is
    III I

Im

: carattere di eventualita

Is

: registro che ricorda l'indirizzo della posizione p8 dell'istruzione

: indirizzo dell'istruzione che segue la suo su unita fittizia

Im

: il registro Im puo' modificare l'indirizzo IIII e il nome del registro Is

: salta se si e' verificata l'eventualita' =

a) La presente istruzione suppone avviata una sequenza di 3 programma mediante
una precedente S3P normale

b) Per essere utilizzata e necessario che la sequenza di 30 programma abbia una
SUO su unita? fittizia

c) Se e' gia' in corso una sequenza di programma esterno la S3P\* non blocca il
programma su cui e' posta.

La S3P\* viene sempre eseguita anche se e' in corso una sequenza di 3
programma, non blocca mai il programma in cui e' posta; permette un ciclo
intero di : gramma ogni qualvolta ne sorga la necessita'

d) Il ciclo di 3?? programma ottenuto mediante S3P\* parte dall'istruzione
successiva alla SUO su unita' fittizia e si arresta invece su quest ultima

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

: il registro Im puo' modificare sia l'indirizzo IIII che il nome dell'unita'

: salta se si e' verificata l'eventualita'

a) In ogni sequenza di programma esterno compaiono tante SUO quante sono le
unita' in linea interessate.

b) La prima volta che la sequenza viene percorsa nessuna SUO viene eseguita, ma
l'unita' in linea U, specificata in pl, viene avviata

c) La presente istruzione serve pure a specificare l'unita' interessata dall'
istruzione 10L che segue

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
in linea specificata dalla SUO immediatamente precedente sia un lettore di schede o
un lettore fotoelettrico di banda perforata, oppure una
stampante o un perforatore di schede.

    Salta se errore in unita' in linea
    interno, unita'
    in linea U
    (011110)
    I I I I Im 0
    SEL
    10 o 15

a) Salta se si e' verificato un errore nell'unita' in linea U, specificata in
p7

b) La segnalazione di errore su unita' in linea presenta diverse
caratteristiche secondo del genere di apparecchiature nel quale l'errore si
verifica; infatti segnalazione avviene: per il lettore di schede

: al termine della lettura della scheda successiva a quella in cui l'errore
verificat.  per il perforatore di schede

: al termine della perforazione della 2?? scheda successiva a quella in cui
errore si e veriticato per la stampante

: terminato un ciclo di stampa (prima della TOL successiva)

    Arresto di unita' in linea
    STOP
    interno
    (111001)
    XXx X #
    O
    10
    0
    U #

: carattere di eventualita'

: unita' in linea

: posizioni non utilizzate

: posizione non utilizzata

: arresta l'unita' in linea U, specificata in p7.

a) L'unita' in linea U passa allo stato "inattiva"

b) Se una o piu' unita' in linea passano allo stato "inattiva" la sequenza di
programma esterno continua a svolgersi per le rimanenti.

c) Solo quando tutte le unita' in linea hanno ricevuto la segnalazione di Stop:
il 30 programma si arresta.

d) L'arresto del 30 programma non blocca gli altri programmi eventualmente in
corso

e) Lo Stop non arresta immediatamente l'unita' interessata ma solo al termine
delll'ultimo ciclo meccanico di lavoro

    216
    SCHEMA RIASSUNTIVO
    Istruzioni di 30 programma
    Istruzioni
    S3P
    S3P\*
    sUO, TOL,
    SEL,
    STOP

    Particolarita' del 30 programma
    sap

    non puo' essere esequita se el in corso il 30 programma.  e viene riciclata con
    conseguente blocco del programma in cui a?? registrata.

    S3P\*
    permette un ciclo di 30 programma ogni qualvolta viene letta, anche se detto
    programma e' gia' in corso.

    SUO
    TOL
    SEL
    STOP

    per le particolarita riguardanti queste istruzioni
    rimando agli schemi relativi

    Unita' collegabili: lettori di schede
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
    Priorita' del 30 sul 10 e 20 programma : ogni qualvolta sia disponibile una unita'
    a2404\*194;
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
    .


## Esempio di 30 sequenza con uso della sola S3P

Generalita'

Nell'esempio seguente si fa riferimento ad una sequenza di 30 programma avviata
dal 1?? mediante S3P.

 - La sequenza e' costituita da 2 cicli fondamentali riferentisi
   rispettivamente a 2 unita'.  Nel casospecifico, unita' 1, 2.

L'unita' 1 e' supposta essere un perforatore di schede, l'unita' 2 un lettore
di schede.

 - Sono supposte gia' preparate le zone di memoria che saranno operate nelle
   istruzioni TOL (una per ognuno dei sopraddetti cicli).

 - I registri T utilizzati sono Ij, T2 (rispettiva mente associati alle unita'
   1, 2), che servono sia per la conta del numero di schede, sia per la
   modifica dell'indirizzo della TOL per passare da una zona predisposta per
   una scheda, alla successiva.

 - Schede da perforare (unita' 1) : 6 su 80 colonne = 480 caratteri.  Schede da
   leggere (unita' 2): 20 su 40 colonne = 800 caratteri.

Le informazioni da perforare si trovano a partire dall'indirizzo 7000 e
successivi in senso crescente.

Le informazioni lette sulle schede vengono registrate a partire dall'indirizzo
7500 e successivi in senso crescente.

Il programma occupa in memoria la zona compresa tra gli indirizzi 993 e 1128
(in totale 136 caratteri).

Il programma

La sequenza e' fornita da due parti: una aciclica e una ciclica.

    SCHEMA DI 3?? PROGRAMMA CON USO DELL' ISTRUZIONE S3P
    2??? PROGRAMMA
    1?? PROGRAMMA
    C. ??
    C ??
    PREPARAZIONE
    DELLE ZONE DA
    3??? PRAGRAMMA
    sU0
    TOL
    SEL
    + C T
    ALTRE ELABORAZIONI
    STOP
    UNITA 2
    ?? C #
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
    ?? #
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
    ?? #
    1 0 7 2
    X X X X
    #
    ) #
    10 7 2
    #
    C ??
    C ??
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
    ???1 0 5 6
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

a) La prima parte e' composta da 2 istruzioni cT mediante le quali si portano gli indirizzi delle
zone impegnate per la prima elaborazione esterna, rispettivamente nei registri T1, T2, (ad ogni ciclo si somma in T una quantita' pari al numero di caratteri per scheda).

b) La seconda comprende le due sequenze relative alle unita' in linea interessate.

Percorrendo per la prima volta le 2 sequenze si attivano le 2 unita' chiamate e si avvia,
per ogni unita', un primo ciclo meccanico operativo.

Piu' precisamente

Istruz. SUO

Non effettua il salto non essendo la unita' 1 occupata.

La SUO ha l' effetto di avviare la unita' e di predisporre il sincronizzatore
al trasferimento che viene effettuato nella successiva istruzione TOL, da
memoria dell'unita' centrale a memoria di transito dell'unita' 1.

Istruz. TOL

Trasferisce le informazioni relative alla prima scheda da perforarsi, da
Memoria principale (a partire dal l'indirizzo 0000 modificato da T, e
successivi in senso crescente) a memoria di transito dell'unita' 1. Essendo
7000 il contenuto di T1 1' indirizzo iniziale e' 7000.  Effettuato il
trasferimento, si avvia un ciclo meccanico operativo del l'unita' 1, mentre
l'unita' centrale passa ad eseguire contemporaneamente le successive istruzioni
del programma.

Istruz. SEL

Istruz. +CT

Istruz. CCT

Istruz. SC+

Se l'eventualita' si verifica salta al sottoprogramma di errore che provvede a
ripristinare le condizioni e sistenti prima del ciclo meccanico durante il
quale l'errore si e' verificato, affinche' l' operazione possa ripetersi in
modo corretto.

Addiziona 80 (n?? caratteri di scheda) al registro T1.

1in z

Confronta il contenuto T, con 560 (n?? totale dei caratteri da perforare + 80).

Dal confronto risulta che I, non e' uguale alla costante specificata
nell'istruzione.

Effettua il salto all'istruzione SUO successiva, scavalcando lo STOP relativo
all'unita' 1 perche' ancora mancano le condizioni d'arresto.

Il ciclo relativo all'altra unita' e' analogo a quello sopra descritto.

Dal SC+ dell'unita' 2 si ritorna alla SUO della unita' 1, e se e' ancora in
corso il ciclo operativo questa unita' la condizione di salto e' verificata;
ma, essendo occupate in questo caso entrambe le unita' attivate, il salto non
viene effettuato, e lo svolgimento del 30 programma si arresta.

Arrestandosi il 30 programma il primo prosegue a partire dall'istruzioche che
immediatamente segue la S3P.

Il 10 programma procede allora fino a che almeno una delle unita' occupate
abbia terminato il ciclo opera.

Istruz. SUO (relativa alla unita' 1)

Istruz. SUO (relativa alla unita' 2)

Istruz. TOL

Istruz. SEL

Istruz. +CT

Istruz. CCT

Istruz. SC+

Istruz. SUO (relativa alla unita' 1)

tivo utile e si sia resa disponibile.

Allorquando questa eventualita' si verifica il 10 programma si arresta il 30
prosegue dal punto in cui si era arrestato.

Supponendo che l' unita' resasi dispo nibile sia la 2 si avra L'unita' 1 e'
ancora occupata, salta alla istruzione SUO relativa all'unita' 2.

L'unita' 2 e' disponibile,assenar 1' unita' gia' attivata si predispone il
sincronizzatore al trasferimento che viene effettuato nella successiva TOL.

Trasferisce il contenuto della seconda scheda alla memoria di transito e
quindi alla memoria principale. L'indirizzo iniziale e' ora 7500 ?? 40= 7540
(solite condizioni).

Addiziona 40 in To.

Il confronto non da ancora uguaglianza.

Essendosi avuta disuguaglianza precedente confronto, il salto viene effettuato.

L'unita' 1 e' ancora occupata, si arresta il 30 programma.  Se l' unita' 1 si
fosse nel frattempo resa disponibile, si sarebbe invece percorso il rispettivo
ciclo e l'arresto del 30 programma si sarebbe effettuato solo sulla SUO dell'
unita 2.

Allorche' il contenuto di Ti: aumentato di 80 ad ogni +CT relativa, e' = 560
(quando cioe' tutte le 6 schede sono state perforate e ci si e' predispo sti
per una successiva scheda, percorrendosi il ciclo relativo all'unita' si avra

Istruz. SC+

Istruz. STOP

Verificatasi ora l' uguaglianza, l'istruzione STOP relativa all' unita' 1 non
viene scavalcata.

Arresta l'unita' 1 al termine dell'ultimo ciclo meccanico di lavoro.

Il programma prosegue passando al ciclo relativo alla unita 2 sino a che anche
le operazioni di lettura siano terminate.

L'esecuzione dello STOP dell' unita' 2 arrestera' infine il 30 programma.


## Esempio di 30 sequenza con uso della SP\*

Generalita'

- Nell' esempio seguente si fa riferimento ad una sequenza di 30 programma che
  pur essendo avviata da una istruzione SP, ha le singole unita' occupate
  mediante l'istruzione S3P\*

- La sequenza e' costituita da 2 cicli fondamentali riferentisi rispettivamente
  a 2 unita': unita' 1 e 2.

L'unita' 1 e' supposta essere un perforatore di schede, l'unita' 2 una
stampante in linea.

    SCHEMA DI 3?? PROGRAMMA CON USO DELL' ISTRUZIONE S3P *
    PROGRAMMA
    3?? PROGRAMMA
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

- Le zone di memoria interessate dalle istruzioni TOL vengono preparate
  mediante sequenze d'istruzioni di 1?? programma indicate sommariamente con la
  dicitura "Elabora zona SK (scheda)" zona ST (stampa)".

- Ognuna di queste sequenze e' preceduta da un deviatore che viene aperto dal
  3?? programma ad effettuato trasferimento alla memoria unita' in linea di ogni
  scheda elaborata.

- I registri utilizzati Ti, T2, Tg, T4, associati a coppie alle unita' 1 e 2,
  servono per il posizionamento dei deviatori "& "e "?? "del primo programma,
  "y"e =?? : del terzo.

- Il numero delle schede da perforare e da stamparsi e' imprecisato ma
  determinabile mediante opportune istruzioni di programma raccolte sotto la
  descrizione generica "sono terminate le operazioni relative al 3?? programma".

Il programma

La sequenza di 3?? programma e' composta da quattro parti di cui la prima e
l'ultima acicliche.

a) La prima parte a cui rinvia l'istruzione S3P com prende due istruzioni TM
che aprono rispettivamente i deviatori "y= e ??5 * per permettere la attivazione
delle unita' in linea interessate nel corso dell' elaborazione.

b) La seconda parte e' introdotta dal deviatore y: che troviamo aperto ogni
qualvolta dal 1?? program ma si esige la periorazione di una scheda.

c) La terza parte e' introdotta dal deviatore 65 .  che troviamo aperto ogni
qualvolta dal 1?? programma si esige la stampa di una riga.

d) La quarta parte comprende due istruzioni di STOP relative alle due unita' in
linea, condizionate all'alternativa di fine elaborazione posta nel 1??
programma.

Si hanno pertanto le seguenti operazioni:

Istruzione S3P (1?? programma)

rinvia all'istruzione IgM e IgM permettendo l'attivazione delle unita' in
linea.

Istruzione TsM (3?? programma)

apre il deviatore sy. permettendo il ciclo relativo alla unita' 1.

Istruzione. TgM

apre il deviatore "5" permettendo il ciclo relativo alla unita

Istruzione SUO (# riferita ad unita' inesistente).

Questa istruzione come si e' detto ha solo una funzione tecnica: su di essa
termina ogni ciclo di 30 programma; da essa il ciclo riprende a segnalazione di
unita disponibile.

Istruzione SI o SN

funge da deviatore; viene alternativamente trasformata mediante apposite
istruzioni in istruzione SI O SN.

Istruzione SUO

avvia l' unita' 1 e predispone il sincronizzatore al trasferimento.

Istruzione TOL

esegue un primo trasferimento da memoria principale a memoria di transito e
avvia un ciclo meccanico di lavoro.

Il primo programma, come si e' detto, comprende 2
sequenze interessate rispettivamente alla preparazione dei dati da trasferire su schede perforate e
a stampa.

In ognuna di esse, oltre che le istruzioni di elaborazione vera e propria, appaiono un deviatore, un
posizionatore di deviatore, e una istruzione S3P\*
con le seguenti funzioni

deviatore dn
(12
sequenza)

: condiziona l'elaborazione di
una nuova scheda all' avvenuto
trasferimento della scheda precedente, nella memoria dell'unita' in linea.

Puo' essere costituito da una
istruzione SI che rinvia ad
una istruzione qualsiasi di
servizio (es. CT) che la preceda immediatamente.

posizionatore " Y' : apre il deviatore " y " che per (1?? sequenza) mette 1'
entrata in ciclo della sequenza di 3 programma relativa all' unita' 1.

istruzione S3P\* (1a sequenza)

: avvia un ciclo di 30 programma con conseguente esecuzione della sequenza
relativa all'unita 1.

Il deviatore ?? , il posizionatore d e la S3P\*della seconda sequenza hanno
funzioni analoghe a quelle su descritte, ma relativamente all'unita' 2.

Opportune istruzioni di 1?? programma permettono in fine l'avvio del 30
programma sui 2 STOP che ne con dizionano 1' arresto.

Lo STOP di 1?? eseguito immediatamente dopo la SP\* arresta invece il primo
programma.

Istruzione SEL

Istruzione TiM

Istruzione TzM

Istruzioni SI, SUO, TOL,
SEL, ??????, ?????? (relative alla unita' 2)

Istruzione STOP (1?? unita')

Istruzione STOP (2?? unita')

= in caso di errore, salta al sottoprogramma di errore che provvede a
riprodurre le condizioni esistenti prima del ciclo meccanico durante il quale
l'errore si e' verificato, affinche' l'operazione possa ripetersi in modo
corretto, (le caratteristiche dell' istruzione SEL sono esposte nello schema
relativo).

= trasforma l'istruzione deviatore: (SI o SN) precedentemente considerata, in
salto effettivo; chiude cioe' il deviatore "y' che puo' essere riaperto solo da
una istruzione posta nel 1?? programma.

= stessa funzione della TiM, in a relativamente al deviatore d?? posto nel 1??
programma il cui posizionamento condiziona l' elaborazione di una eventuale
scheda da perforare.

= per queste istruzioni valgono le considerazioni fatte per il gruppo
precedentemente descritto ma relativamente all'unita' in linea N?? 2: stampante
in linea.  lette di seguito mediante S3P\* di 1?? programma permettono l'arresto
del 3?? programma.

