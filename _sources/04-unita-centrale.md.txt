```{sectnum}
---
start: 4
---
```

# L'unita' centrale


## Memoria principale

La memoria principale e' costituita da nuclei di ferrite a ciclo di isteresi
rettangolare. I nuclei sono montati su piani, ognuno dei quali ne contiene
10.000.  Sette piani sovrapposti contengono 70000 bit necessari a rappresentare
10.000 informazioni alfanumeriche; il loro insieme forma un elemento
tecnologico di memoria.

Due elementi tecnologici di memoria, per un totale di 20.000 informazioni
alfanumeriche, costituiscono in vece la minima unita funzionale di memoria: un
calcolatore puo' disporre di un numero di unita' di memoria variabile da 1 a 8,
corrispondenti ad un numero di informazioni alfanumeriche compreso fra 20.000 e
160.000.

I sette bit costituenti ogni carattere vengono operati in parallelo: il tempo
necessario al loro trasferimento da una zona ad un' altra della memoria, o dal
la memoria agli altri organi della unita centrale e' di 10 microsecondi; tale
intervallo di tempo e' detto "periodo di cifra".

In un periodo di cifra si possono estrarre o introdurre dalla memoria due
caratteri, ed operare su di essi.

La memoria e' circolare e indirizzabile posizione per posizione mediante
indirizzi di quattro cifre la cui aritmetica e per contare modulo 40.000.

Cio' significa che in una macchina con memoria di 20.000 posizioni qualora si
oltrepassasse l'indirizzo 19.999 (I999), in tutti gli organi programmabili
(memoria, registri T, comparatori ecc.) apparirebbero numeri relativi alle
posizioni di una memoria avente la capacita' di 40.000 posizioni: cioe' €000
(20.000), J000 (21.000): K000 (22.000), ecc. Essendo pero' la memoria di 20.000
posizioni e' evidente che per la circolarita' della memoria l'indirizzo E000
corrisponde alla posizione 0000 e che l'indirizzo J000 corrisponde alla
posizione 1000 ecc., come illustrato dalla figura seguente:

    0001
    0000
    19000
    30003
    2000~
    IM
    40004
    5000
    6000
    18 000
    6 17 000
    X
    - 16000
    W
    E 15000
    7000
    8000
    9000
    D14000
    C 13000
    12.000
    10000
    11000
    34

Per quanto riguarda le memoria con piu' di 40.000 posizioni vi e l'
impossibilita di percorrere mediante operazione aritmetica (e modifica
automatica) l'intero insieme degli indirizzi.  Accade cioe' che oltrepassando
l'indirizzo 39.999 ('999) 1'indirizzatore sceglie non 1' indirizzo 40.000
(0000) ma l'indirizzo 0000.

Non esiste cioe' la possibilita di attraversare con operazioni aritmetiche i
multipli di 40.000.  Questo non avviene invece per aggiornamenti effettuati
nell' ambito di un gruppo di memoria di 40.000 caratteri.

Da cui:

    ( 39.999) ' 999 + 1 = 0000 (
    0)
    (79.999) 'I99 + 1 = 0000 ( 40. 000)
    (119.999) 'R99
    + 1 = 0E00 ( 80.000)
    (159.999) 199 + 1 = 0.00 (120.000)
    0) 0000
    ( 40.000) 0000
    ( 80.000) 0800
    (120.000) 0.00
    999 ( 39.999)
    199 ( 79.999)
    'R99 (119.999)
    . 99 (159.999)
    ( 39.999) ' 999
    ( 79.999)
    • I99
    (119.999) R99
    (159.999) 11 99
    998 ( 39.998)
    198 ( 79. 998)
    R98 (119.998)
    1' 98 (159.998)
    (
    0) 0000
    ÷ 1 = 0001 (
    1)
    ( 40.000) 0000 ÷ 1 = 0001 ( 40.001)
    ( 80.000) 0800
    + 1 = 0€01 ( 80.001)
    (120.000) 0.00 ÷ 1 = 0.01 (120.001)
    POSIZIONE O PER OGNI GRUPPO TECNOLOGICO DI MEMORIA
    0000÷39999
    0000
    40000÷79999
    120000÷159999
    40000
    120000
    0ф00
    0.00
    8000
    0E00
    80000÷119999
    CIRCOLARITA NELL/AMBITO DI UN ELEMENTO TECNOLOGICO DI MEMORIA
    ORDINE DI SUCCESSIONE DEGLI ELEMENTI TECNOLOGICI DI MEMORI

## Accumulatore

L' accumulatore e' una speciale memoria a 100 posizioni; ad ogni posizione e'
associato un indirizzo.  Gli indirizzi vanno da 00 a 99; l'indirizzo successivo
al 99 e l'indirizzo 00, cioe' 1' accumulatore e' circolare. L'indirizzo
iniziale di una parola contenuta in accumulatore e' dato dal contenuto di uno
speciale registro detto DA.

DA - Mediante l'istruzione DA si puo' fissare l'inizio dell' accumulatore in
una qualsiasi delle sue 100 posizioni. Cio' significa che il primo carattere di
una parola che venga prelevata o inviata all' accumulatore proverra' o andra'
all'indirizzo fissato mediante la istruzione DA. I caratteri successivi hanno
riferimento agli indirizzi identificati da numero d' ordine maggiore.

Esempio:

    Accumulatore do
    po un trasterimento con DA = 91
    del numero di cifre: 12345
    .. Si noti l'influenza della circolarita' della memoria
    MILE
    000000
    6 • • . . . .. •• 7.654,32,1
    13 4 5

BIT GA

Bit gA - Il registro DA indica dunque l' indirizzo di una parola contenuta in
accumulatore; la fine dell'informazione e' segnata invece da uno speciale bit
detto gA. Cio' permette di utilizzare l' accumulatore per contenere piu'
parole; ad ognuna di esse corrispondera' un bit gA che ne segnala la fine,
mentre il contenuto del registro DA rappresenta l'inizio della parola sulla
quale si vuole operare.  I diversi bit gA sono materializzati da un ottavo
piano di nuclei ferromagnetici, che si aggiunge ai sette utilizzati per la
registrazione dei caratteri alfanumerici e per la verifica di disparita'.

Il bit gA ha i seguenti effetti:

  - nelle operazioni aritmetiche le cifre che lo seguono sono considerate degli
    zeri;
  - nelle operazioni di trasferimento da accumulatore a memoria il bit gA non
    viene considerato.

La posizione del bit gA e' determinata dalle seguenti regole generali

 - l'istruzione AoM (trasferimento da accumulatore a memoria con azzeramento
   delle posizioni di accumu latore trasferite) pone un gA in corrispondenza di
   ogni posizione che viene azzerata.

   Esempio

        9 9
        Accumulatore do-
        po una AoM di 8
        posizion1 suppo
        nendo A 00
        HF 5 S
        5700000000
        BIT GA

 - L'istruzione di trasferimento da memoria ad accumulatore (MA) pone un bit gA
   in corrispondenza del l'ultimo carattere trasferito e lascia inalterati i
   bit gA posti precedentemente purche' non si riferiscano ai caratteri
   trasferiti.

   Esempio

        38
        00000000

        Accumulatore do-
        Do un AoM (esem-
        pio precedente) e
        un trasterimento
        con DA = 02,
        del
        numero 1420.
        117 6 1 919111 9 91 1/1010141
        HF 5 S
        5700142000

Nelle istruzioni aritmetiche il bit gA viene di
sposto secondo le seguenti regole

 - se l' operando chiamato dalla memoria ha una lunghezza minore o uguale al
   numero di posizioni comprese fra DA e gA, questo non viene spostato;
 - in caso contrario il gA viene posto in corrispondenza della cifra piu'
   significativa dell' operando chiamato da memoria;
 - nel caso di superamento di capacita' dovuto a riporto, il gA viene posto in
   corrispondenza della cifra piu' significativa e cioe' eventualmente una
   posizione piu' a sinistra di quella che risulterebbe diversamente

L'esempio che segue mostra la posizione del bit gA attraverso una successione
di istruzioni

    •• 9 9 8 9 9 9 95
    Condizioni iniziali
    14 45 96 2101
    dopo una AoM lunga 7
    dopo il trasferimento in acc.
    numero 810345 (lung.
    1408103451
    dopo il trasferimento del numerc
    6234 (lung.
    14 0 81 6234
    dopo 1' addizione del numero 2
    (lung. 1)
    14 0816236
    dopo l'addizione del numero 1000
    (lung
    140817236
    dopo l'addizione del numero 9000
    (lung. 4)
    140816236
    40

Per quanto riguarda le operazioni algebriche il valore assoluto di un numero
puo' essere registrato in accumulatore sia nella sua vera grandezza che nel suo
complemento alla potenza di 10 immediatamente superiore : un apposito organo a
flip-flop segnala con la sua posizione quale delle due rappresentazio ni e' in
quel momento utilizzata.  La memorizzazione del segno e' invece affidata ad uno
speciale registro, chiamato "registro del segno: che segnala se la parola
contenuta in accumulatore e' dotata di segno, e in caso affermativo, se il
segno e' "piu" o "meno"

Questo registro e il flip-flop segnalatore dei complementi possono essere
considerati come organo unico che puo' indicare una eventualita' fra sei
possibili: le due eventualita' -in vera grandezza e in "complemento": si
compongono infatti con le tre eventualita' "non segnato", "segno piu", e "segno
meno".

    VERA GRANDEZZA
    COMPLEMENTO
    NON
    SEGNAT
    SEGNO
    SEGNO
    NON
    SEGNATO
    SEGNO
    SEGNO

Altri tre registri concorrono all'esecuzione delle operazioni algebriche (le
operazioni aritmetiche possono essere considerate operazioni algebriche tra
operandi di segno +: in questo caso pero' i risultati non sono ovviamente
segnati).

    NORME CHE RECOLANO LO STATO DEL REGTSTRO DE SE GNO
    VERA GRANDEZZA
    COM LEMENTO
    NON SEGNATO
    SEGNATO
    NON SEGNATO
    SEGNATO
    a) dopo un trasferi-
    mento mediante AOM
    a) qualora da una o
    perazione tra ad
    dendi non segnat
    si ottenga il ri.
    sultato in compl
    mento
    b) dopo un trasferi.
    mento mediante MA
    di parola non se-
    mn ata
    a) dopo un trasferi
    mento mediante MA
    di parola segnata
    a) gualora da una o-
    perazione tra ad.
    dendi di cui alme
    no uno sia segna-
    to. si ottenga il
    risultato in com-
    alemento
    c) dopo una operazio
    operandi
    non geonati. e ri
    sultato in
    Pano
    grandezza
    b) dono una operazio
    ne tra anerandi.
    di cui uno almeno
    sia segnato

Essi servono a ricavare rispettivamente:
 1. il segno dell' operazione da eseguirsi (somma, sottrazione);
 2. il segno dell' operando contenuto in memoria;
 3. il segno del moltiplicatore.

Si hanno quindi complessivamente 4 registri e conseguentemente 4 indicazioni di
segno per ogni operazione. (Il segno del moltiplicatore non e' considerato
nelle operazioni di somma e sottrazione e il segno della moltiplicazione non
compare nel registro del segno dell'operazione; in sua vece si hanno i segni +
o - ad indicare se il prodotto ottenuto va sommato o sottratto al contenuto
dell' accumulatore).  In base al numero complessivo dei segni "-". che possono
comparire nei quattro registri, durante una operazione, si hanno le seguenti
norme che regolano la complementazione dei dati operandi e dei risultati:

1. Se il numero dei segni .. e dispari: si ha la complementazione dell'
operando contenuto in memoria con inversione di segno prima che su questi si
effettui l'operazione richiesta.

2. Se in seguito alla complementazione del dato in memoria e alla sua
inversione di segno si ottiene un risultato con "riporto", il riporto viene
annullato e il risultato compare in vera grandezza". Vedi esempio 1.

3. Se in seguito alla complementazione del dato di memoria e della sua
inversione di segno si ottiene un risultato senza riporto il risultato compare
in "complemento. Vedi esempio 2.

    ```
    Esempio
    1 = Dispari
    COMPLEMENTAZIONE
    Esemaio2
    NIllASOO SEENI NEGATIVI
    Dispari
    COMPLEMENTAZIONE
    Esempio 3
    NUMERO SEGNI NEGATIVI
    1 = Dispari
    COMPLEMENTAZIONE
    Esempio 4
    лимскоосопі першу
    2 = Pari
    COMPLEMENTAZIONE
    NO
    SEGNO OPERAZIONE
    MOLTIPLICATORE
    10 -
    90 +
    RISULTATO
    20 (N.S)
    (110 +
    VERA GRANDEZZA
    MOLTIPLICATORE
    nOSBANDO VENDIA
    20 (N.S)
    10 (N.S)
    80
    QISULTATO = Q0 INS)
    COMPLEMENTO
    OPERANDO MEMORIA
    20 (N.S)
    80
    RISULTATO
    SEEN10959677ONE
    MOLTIPLICATORE
    20 (N.S)
    (1)00 (N.S)
    VERA GRANDEZZA
    OPERANDO MEMUKIP
    10-
    DISUITATO
    APERANDO ACCUMUL.
    SEENO 095067 ONE
    20 +
    MITEPCER
    30 +
    VERA GRANDEZZA
    ```

4. Se in seguito alla complementazione del dato di memoria e della sua
   inversione di segno si ottiene un risultato nullo = 0, il risultato e' in
   dicato in "vera grandezza". Vedi esempio 3.

5. Se il numero dei segni "-" e' "pari", 1' operando di memoria viene operato
   tale e quale se si tratta di una somma, o col segno inverso se tratta di una  
   sottrazione. Vedi esempio 4.

    si

   Per quanto riguarda il trasferimento di un operando
   o di un risultato dall' accumulatore a memoria si hanno le seguenti possibilita'

    DATO IN ACCUMULATORE
    4
    NATO DOPO IL TRASFERIMENTI
    segnato
    99
    vera grandezzo
    complemento
    vera grandezza
    complemento
    vera grandezza
    complemento
    non segnato
    vera grandezzo
    complemento
    vera grandezzo
    45


## Registri T

L'insieme dei registri T e' co stituito da una memoria a nuclei magnetici della
capacita' di 200 caratteri alfanumerici, indirizzabili di 5 in 5 posizioni. Ad
ogni possibile indirizzo corrisponde un registro T; vi sono dunque 40 di tali
registri.

Ogni registro ha la lunghezza massima di 10 posizioni; e' chiaro quindi che, ad
esempio, il registro 2 ed il registro B si sovrappongono parzialmente.

    NOME
    E
    в
    70
    8
    7
    5
    3
    2
    R
    o
    N

Quando il registro T e' utilizzato per modificare un'istruzione, o, come si
dice, quando opera come modificatore, al massimo i primi 5 caratteri del suo
contenuto vengono utilizzati; conseguentemente, tutti i 40 registri possono
operare come modificatori senza che risulti alcun inconveniente dalla loro
parziale sovrapposizione.

4 6

Immaginando per convenienza di esposizione le posizioni di memoria numerate da
000 a 199, la parola registrata a partire dall' indirizzo zero, normalmente uno
dei fattori della moltiplicazione, puo' avere una lunghezza qualsiasi fino ad
un massimo di 100 caratteri, piu' un segno che viene trasferito in un apposito
registro; le parole registrate a partire dagli altri indirizzi possono avere un
massimo di 10 caratteri.

Bit gr - Non esiste per i registri T 1' analogo della DA: le informazioni
contenute in ogni registro hanno sempre inizio dall'indirizzo corrispondente a
quel registro. Esiste invece l' analogo del bit gA detto gT; anche per i
registri T il hit gT e' materializzato da un ottavo piano di nuclei magnetici.
Esiste ambiparita' anche per quanto riguarda il registro del segno; solo che
questo resta accessibile esclusivamente mediante l'istruzione "y".

Per quanto riguarda l'utilizzazione ed il posizionamento del bit gT valgono le
stesse considerazioni fatte a proposito del bit gA ovviamente sostituendo le
istruzioni per l' accumulatore con le corrispondenti per i registri T.

Nelle singole istruzioni verra' specificato quando il risultato puo' avere
lunghezza più lunga del piu' lungo degli operandi ed in quali casi si ha
indicazione di overflow.

Un registro T viene identificato nell'istruzione da un carattere; la tabella
precedente indica l'indirizzo iniziale di ogni registro Tin corrispondenza del
carattere che lo identifica.


## Logica aritmetica dell' Elea 9003

Operazioni aritmetiche che possono interessare la memoria, 1' accumulatore e i
registri T (+MM; +MT; -MT; +MA; -MA; +TM ; +AM).

Le operazioni su caratteri speciali non possono essere effettuate. Nel caso si
abbiano operazioni su tali caratteri si ha indicazione di errore nell'unita'
aritmetica e logica.

Possono invece essere effettuate operazioni su caratteri alfabetici e
ovviamente su caratteri numerici.

La macchina sa distinguere questi caratteri dagli altri, in quanto in essi non
appaiono le configurazioni c, b, a = 101, oppure b, a = 10

Operando su numeri:
a) la parte numerica (*) viene operata normalmente (modulo 10)
b) un eventuale riporto non influisce sulla configurazione della parte alfabetica (*).

Si ha pertanto

    f e
    dc b a
    4 (00 0100)
    +5 (00 1000)
    =
    9 (00 1100)
    9
    + 4
    13
    fe dcba
    (00 1100)
    (000100)
    (00 0001) (00 0111)

Operando su caratteri alfabetici e alfanumerici:

1. la parte numerica viene operata allo stesso modo dei caratteri numerici,
tenendo conto del valore numerico dato alla lettera in questione (vedi tabella
2);

2. i risultati delle operazioni sono espressi mediante uno o due caratteri a
seconda che si abbia avuto o no riporto dalla somma dei due caratteri;

3. la parte alfabetica viene operata distintamente dalla parte numerica,
secondo modulo aritmetico 4 (da cul 3 + 1 = 0);

4. la complementazione nella parte alfabetica avviene anch' essa secondo modulo
aritmetico 4. Si ha pertanto :

Esempio 1:

    f
    0 1 (1)
    + D 0 1 (1)
    = Q 1 1 (2)
    d c b a
    0 1 0 0 (4)
    0 1 0 0 (4)
    1 1 1 1 (8)

Esempio 2:

    fe
    D 0 1 (1)
    + 1 0 1 (1)
    = L 1 1 (2)
    1 0 0 (0)
    d c b a
    0 10 0 (4)
    1 1 0 0 (9)
    01 1 1 (3)
    o 0 0 1 (1 di riporto)
    0
    01
    1 1
    10
    00011110
    o 0
    0 1
    1 1
    10
    0 1
    11
    1000
    1 1
    1 0
    0 0
    0 1
    1 0
    00
    01 11

    Tabella delle somme dei bit "f, er.

    * Nota : I caratteri numerici hanno i bit."f, e"
    00.

I caratteri alfabetici ripetono nei bit "d c, b, a" le configurazioni dei
caratteri numerici a cui sono associati (vedi tabella 2) e si distinguono
pertanto solo per la configurazione dei bit "f, e".

Esempio:

    carattere
    D
    fe
    0 0
    0 1
    1 1
    1 0
    d c b a
    0 1 0 0
    0 1 0 0
    0•1'0 0
    0 1 0 0
    identica
    configurazione
    51
    dcba
    CARATTER
    E
    M
    6
    0
    P
    y
    R
    CARATTERI NON OPI
    Tabella N. 2

