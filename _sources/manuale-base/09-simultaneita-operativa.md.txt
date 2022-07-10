```{sectnum}
---
start: 9
---
```

# La simultaneita' operativa dell'ELEA 9003; Logica e utilizzazione del 1° e 2° programma


## Considerazioni generali

Alla memoria principale dell' ELEA 9003 si puo' accedere mediante due canali di
trasferimento delle informazioni, uno interno ed uno esterno. Il canale interno
collega la memoria principale agli organi interni della macchina; il canale
esterno e utilizzato per il collegamento con le unita' a nastro, tramite il
relativo governo, e quando si opera direttamente fra due diverse zone di
memoria.

L'istruzione dell' ELEA 9003 si svolge, come abbiamo
gia' visto, in due fasi distinte : la fase preparatoria, durante la quale il canale interno della macchina e impegnato in continuita per la durata di
nove periodi di cifra, la fase esecutiva, che varia
a seconda della funzione che l'istruzione stessa deve svolgere, e che impegna sempre per un periodo di
cifra il canale interno, prima che si inizi l'esecuzione vera e propria che potra' impegnare uno dei
due canali.

Sotto questo punto di vista le istruzioni dell' ELEA
9003 sono raggruppate nel seguente modo

1. istruzioni che impegnano il canale interno;

2. istruzioni che impegnano il canale esterno e il governo delle unita' a
nastro magnetico;

3. istruzioni che impegnano il canale interno ed il canale esterno;

4. istruzioni che impegnano il canale interno, il canale esterno e il governo
delle unita' a nastro magnetico;

5. istruzioni che impegnano il governo delle unita' a nastro magnetico.

In particolare l'istruzione avvolgi nastro (AV) puo' essere eseguita
simultaneamente con aualsiasi altra istruzione purche' quest'ultima non si
riferisca all' unita' a nastro indicata nell'istruzione di avvolgimento.

In forma tabellare indichiamo le possibili sovrapposizioni tra le varie
categorie di istruzioni precedentemente definite.

    Gruppo di appartenenza dell'istruzione

    Gruppi di appartenenza delle istruzioni che si possono svolgere in
    simultaneita' con la prima

    10
    20
    50
    2°
    1°
    30
    50
    40
    50
    10
    30

Dall' esame di questa tabella risulta che i metodi di organizzazione di un
programma sono due

a) un programma che prevede 'utilizzazione di istruzioni doppie e quindi che
esclude ogni simultaneita' operativa organizzata;

b) un programma che prevede 'utilizzazione delle si sultaneita operative delle
istruzioni dell' ELEA 9003.

Mentre nel caso a) lo svolgimento del programma si ripartisce linearmente sui
due canali della macchina e quindi non vi e' alcuna ricerca di ottimizzazione
dell' impegno degli stessi, in un programma di tipo b) questa ricerca e'
necessaria ma, come vedremo, non puo' essere fatta dal programmatore.

Cio' significherebbe infatti tener conto dello svolgimento di ogni singola
istruzione, predisporre il programma in modo da inserire tra due successive
istruzioni esterne un numero opportuno di istruzioni interne, tale che la loro
durata complessiva fosse uguale alla durata dell'istruzione esterna
contemporaneamente eseguita.

La realizzazione della simultaneita' operativa si basa ed e' valida per le
particolari caratteristiche logiche dell' ELEA 9003 che consentono alla
macchina di operare su piu' sequenze di programma contemporaneamente.

In questa analisi terremo conto delle sequenze definite di 10 e di 20 programma
mentre esamineremo in altra sede la sequenza che e' propria del collegamento
delle unita' in linea dell' ELEA 9003.

Esaminiamo ora le caratteristiche particolari dei due tipi di programmi
precedentemente definiti.


## Programma con istruzioni doppie

Non considerando la sequenza relativa al terzo pro.
gramma, in questo tipo di organizzazione avremo lo
svolgimento di una sequenza principale di program-
ma : in essa ogni istruzione verra' eseguita in se-
rie dalla macchina e in corrispondenza delle istru-
zioni doppie previste (PUM-MEM, NDN, PIN-NAN) avre-
mo l'impegno contemporaneo dei due canali della mac
china.
Una soluzione di questo tipo puo' per esempio esse-
re adottata nei casi in cui i tempi di elaborazione
siano brevi rispetto ai tempi di introduzione e di
estrazione dei dati e percio' sia piu'
conveniente
sovrapporre questi ultimi.
183
NESSUNA SIMULTANEITA OPERATIVA
BLOCCO
LN
NASTRO IN LETTURA
NASTON IN DERISTOA>
PIN
NAN
BLOCCO 1
SIMULTANEITA IN LETTURA E REGISTRAZIONE NASTRI
staccc
BLOCCO 3
BLOCCO 4
• NASTON IN TEMIOA
SIMULTANEITA® DI ELABORAZIONE E LETTURA O REGISTRAZIONE
1° PROGR.^
29 PROGRA CANALE
CANALE INTEONI
184

## Programma con simultaneita' operative organizzate

Un programma di questo tipo, sempre non considerando la sequenza del terzo
programma, comprendera due Sequenze di istruzioni : una definita di primo
programma ed una di secondo programma.

Le caratteristiche principali di questa organizzazione sono due:

a. la necessita di una particolare organizzazione dei dati;

b. i rapporti tra le due sequenze e la logica della simultaneita' interna.


### L'organizzazione dei dati

Per utilizzare la possibilita' di sovrapposizione del tempo esecutivo dei due
programmi e' necessario assegnare ad ogni flusso di informazioni piu' zone di
memoria; in pratica sono sempre sufficienti due zone.

Si esamini infatti questo caso elementare. Dobbiamo introdurre da nastro
magnetico delle informazioni su una zona di memoria che indichiamo con Zi (zo
na di introduzione), elaborarle depositando i risultati in un' altra zona di
memoria che definiamo Ze (zona di estrazione), e infine estrarle da
quest'ultima zona registrandole su nastro magnetico.

Utilizzando una sola zona per ogni flusso di dati, cioe' in pratica per ogni
operazione esterna (nel caso nostro una IN e una RN ), il programma risulte
rebbe cosi' strutturato

1. LN sulla zona Zi.

2. Elaborazione dei dati contenuti in Zi e deposito dei risultati in Ze.

3. RN dalla zona Ze.

4. Di nuovo, LN nella zona Zi, ecc.

Ovviamente, non e' possibile attuare alcuna simultaneita', tra l'elaborazione e
l'introduzione o la estrazione dei dati, perche' l'elaborazione sulla zona Zi
non puo' aver luogo finche' non e' servita dalla LN e la estrazione dei
risultati da Ze deve attendere che la fase di elaborazione sia terminata.

Se, si ricorre ad una doppia zona di memoria per ogni
operazione esterna, si potra' introdurre le informazioni una volta nella zona Zi e una volta nella
zona Zi, ed estrarle una volta dalla zona Ze e una
volta dalla zona Ze. Il programma risultera' cosi'
strutturato:

1. LN sulla zona Zi

2.  a. elaborazione dei dati contenuti in Zi e deposito dei risultati in Ze

    b. LN sulla zona Zi

3.  a. elaborazione dei dati contenuti in Zi e deposito dei risultati in Ze

    b. RN dalla zona Ze, seguita dalla LN sulla Zi

4.  a. elaborazione dei dati contenuti in Zi e deposito dei risultati in Ze

    b. RN dalla zona Z' e seguita da LN sulla zona Zi, ecc.

Le operazioni a e b risultano eseguite contemporaneamente, cosa che prima non
era possibile.

Abbiamo detto che per avere simultaneita' operativa tra elaborazione ed
introduzione o estrazione e' necessario servirsi di almeno due zone di memoria
in alternanza : in effetti le zone utilizzate alternativamente potrebbero
essere piu' di due con qualche vantaggio di tempo in quanto, in alcuni ca si,
aumentando le zone utilizzabili si eliminano i tempi di attesa di uno dei due
programmi. Ma si occuperebbero molte posizioni di memoria, non sempre
disponibili e si appesantirebbe il programma con ulteriori istruzioni di
servizio.

L'alternanza di zona per le operazioni esterne deve essere preparata dopo che e
stata eseguita l'operazione sulla zona interessata: ad esempio, dopo che si e'
dato inizio all'istruzione IN sulla zona Zi, si predispone il relativo registro
di modifica perche' la volta successiva la stessa LN sia eseguita sulla zona '
i. In modo analogo si predispone 1° alternanza per l'istruzione RN; in entrambi
i casi si attua un meccanismo di flip-flop.  Generalmente le istruzioni di
elaborazione interna saranno modificate da uno o piu° registri per poter
operare dalle zone Zi a Ze e da Zi a Ze.


### Rapporti tra le due sequenze di programma

L' esame delle due sequenze di programma e la contem poranea esecuzione vengono
eseguiti dalla macchina secondo le seguenti regole logiche interne

a) Se nel 1° programma sono in corso istruzioni che riguardano il canale
interno e nel 20 istruzioni che riguardano il canale esterno o viceversa due
programmi agiscono simultaneamente.

b) Se nel 10 programma sono in corso istruzioni interne, e si verificasse che
il 20 debba eseguire anch' esso un' istruzione interna, quest' ultimo prende la
precedenza bloccando il 1° programma..

c) Se uno dei due programmi dovesse eseguire un' istruzione doppia (es. MEM, +
MM, ecc.), che impegni entrambi i canali, questo programma prende comunque la
precedenza.

Come regola generale il secondo programma ha sempre la precedenza sul primo; in
ogni caso pero' la precedenza viene presa dopo che sia stata eseguita la fase
esecutiva dell'istruzione in corso.

Da quanto detto, per avere la massima sovrapposizione e' bene che sul 10
programma non vi siano mai istruzioni esterne, e che non si usino mai in nessun
programma istruzioni doppie.

Inoltre e' bene nel 20 programma limitare allo stretto indispensabile l'uso di
istruzioni interne.

E' consigliabile inoltre evitare l'uso degli stessi registri nei due programmi,
mentre l' accumulatore dovra' essere usato su un solo programma.

In ogni modo se si volesse fare ugualmente uso dell' accumulatore e degli
stessi registri e' necessario scaricarli prima e ricaricarli dopo averli usati.


## Metodi di utilizzazione del 20 programma

Ogni metodo di utilizzazione del 10 e del 2°programma deve soddisfare alle due
seguenti condizioni che costituiscono dei vincoli per il programmatore.

a) L'elaborazione sulla zona 2 puo' essere eseguita solamente quando
l'operazione esterna che serve quella zona ha avuto termine.

L' alternanza delle operazioni esterne deve quindi essere predisposta sul 20
programma e quella delle operazioni interne sul 1°.

b) Appena eseguita l' elaborazione interna e' necessario richiedere una
operazione esterna sulla stessa zona di memoria, per evitare eventuali tempi di
arresa.

E' pertanto necessario programmare delle segnalazioni da parte del 20 programma
al 10 programma ad ogni operazione esterna eseguita, e delle richieste di nuove
operazioni esterne da parte del 10 al 20.

Esistono due metodi di utilizzazione delle simultaneita' operative,
realizzabili mediante le due struzioni di salto speciale S2P e S2P\*


## Descrizione del primo metodo

Al secondo programma si accede mediante l'istruzione S2P (salta al secondo
programma) posta sul primo programma.

La lettura di questa istruzione provoca l'interruzione della sequenza in corso:
infatti la macchina invia l'indirizzo di salto contenuto nella S2P nel registro
indirizzi istruzioni del 20 programma e inizia l'esame delle istruzioni poste
in questa seconda sequenza.

Da questo momento la macchina si comporta rispettando le regole di precedenza
gia' descritte. Effettuato il salto cioe', i due programmi procedono
parallelamente e il loro avanzamento contemporaneo dipende solamente dalle
singole istruzioni poste sui due programmi. L'organizzazione del programma di
lavoro deve prevedere l'esecuzione di una operazione interna di elaborazione e
di una operazione esterna di introduzione e di estrazione alla volta.

Dato l'impegno dell' alternanza delle zone per le singole operazioni si deduce
che se la operazione interna e' eseguita sulla zona Zi, contemporaneamente
l'operazione esterna e' eseguita sulla zona Zi.

E' chiaro allora che e' possibile avviare l'operazione interna sulla zona ' i
solo quando e' terminata la relativa operazione esterna.

In dettaglio, si avra' allora questo svolgimento: dopo un inizio di programma
che provvede ad introdurre i primi dati nelle zone ed a richiedere
l'introduzione dei dati successivi nelle zone alterne ad essi destinate, viene
avviato il secondo programma che esegue le operazioni esterne richieste.

Nel frattempo il 1° programma provvede ad eseguire le necessarie elaborazioni
e, posizionando opportuni deviatori, ad annotare le operazioni esterne che
piu'tardi dovra' richiedere al 20 programma. 

Al termine delle elaborazioni, il 1° programma passa ad una istruzione di salto
$2P che conduce ad uno STOP. Ora, l'istruzione S2P ha la proprieta' di non
venire eseguita fino a che e' in corso il 2°programma: cio' obbliga il 1°
programma ad attendere il termine delle operazioni esterne in corso, o, se
queste sono gia' terminate, gli permette di passare oltre dopo un' attesa di
soli 25 periodi di cifra (15 per la istruzione $2P, 10 per lo STOP).

Solamente dopo aver eseguita l'istruzione S2P il 10
programma provvede a richiedere al 20 le operazioni
esterne precedentemente annotate.

Soddisfatte tali richieste il 1° programma avvia nuovamente il 20 con una istruzione $2P e riprende
elaborazione.

    1° PROGRAMMA
    Fseque 1'operaz
    Prepara alternon
    S 2 P
    Operazione
    Finita zona dell'operazio
    Alterna zona
    renaroarchesc
    di un oberazione
    esterna su quella zol,
    $ 2 P
    Completa le richieste
    di oserarioni estern
    STOP
    2° PROGRAMMA
    (c'è do eseguire una dolo
    operazione es
    Eseque operaziont
    Alterna zona
    (Cisono da aseouire operazion
    esterne d'altro tipo
    LEseaue oberonon
    Alterna zona
    STOP
    1° METODO
    191
    1° PROGRAMMA
    STOP
    laboraz.
    Zi-»Ze
    Elaboraz.
    Zi-»Z'e
    • Y
    192
    2° PROGRAMMA
    Malan
    12stas
    @
    FIGURA 1


    7.0 -
    Il d.

Durante il ciclo n + 1, viene effettuata sia l' elaborazione sulla zona
alterna, che l'operazione e-

Tale organizzazione da la sicurezza che le due condizioni richieste siano
soddisfatte: infatti, appena terminata l' elaborazione sulla zona 2, il 1°
programma ha provveduto, ad esempio in un ciclo n, a richiedere l'operazione
esterna che serve quella sterna sulla zona 7 : all'inizio del ciclo n + 2, in
cui si dovranno elaborare le informazioni su questa ultima zona, sono terminate
tutte le operazioni esterne richieste durante il ciclo n, e quindi certa mente
e' terminata anche l'operazione sulla zona Z.

caratteristica di questo metodo e quindi di assicurare una protezione globale
contro il pericolo di iniziare l' elaborazione su una zona non ancora servita,
imponendo al 1° programma di attendere anche quando le operazioni esterne non
ancora effettuate non riguardano l'elaborazione che dovrebbe iniziare.

Per tale motivo, tale metodo non si adatterebbe, per esempio, al caso in cui
fossero previste piu' di due zone di alternanza per ogni operazione esterna.
In conclusione questo metodo implica che il programma attenda la fine del 20
programma in corso prima di riprendere il ciclo delle operazioni interne, e il
successivo rilancio del 20 programma mediante una S2P posta sul 10.

Lo schema logico e il diagramma a blocchi della figura 1 definiscono in tutti
gli aspetti l'applicazione di questo primo metodo. Con J verra indicato il
generico blocco da introdurre in memoria; con n il numero dei blocchi da
elaborare e con B. X.d. M. 7 i deviatori utilizzati.


## Descrizione del secondo metodo

Questo metodo si basa non su una condizione rigida di rapporti tra il 10 ed il
20 programma, come avve niva nel primo metodo, ma su scambi di informazioni
programmati tra le due sequenze.

Gli scambi da realizzare tra i due programmi sono:

a) Il 1° programma "segnala", col massimo anticipo, le proprie future
necessita', perche' le zone in teressate siano rifornite di dati one siano
sgomberate. Chiameremo tali comunicazioni "segnalazioni"

b) Il 10 programma "richiede" l'esecuzione di una data operazione esterna su
una zona; se la "richiesta" non puo' essere subito soddisfatta, il 10 programma
attende.

Dato che il 20 programma, quando ha ricevuto la "segnalazione fara' il
possibile per prepararsi a soddisfare la "richiesta che seguira', senza bisogno
di solleciti, sara' opportuno effettuare la richiesta all'ultimo momento.

Fisicamente, sul programma, non e' necessario che ci sia una corrispondenza 1-1
tra segnalazion in e "richieste", perche', mentre le segnalazioni servono ad
avvisare il 20 programma della necessita' di una operazione esterna, le
richieste servono ad assicurare il 10 programma che l'operazione esterna su una
determinata zona e' stata eseguita.

Sarebbe necessario introdurre un ulteriore deviatore che consentisse di
accedere alla istruzione solo 194 quando il 20 programma ha raggiunto lo STOP e
di scavalcarla in via normale, quando il 20 programma A!  in corso.

    1° PROGRAMMA
    Esegue loperazion
    esterna
    Prenara allernoinizc
    ci sono operozioni interne
    È stata servita la zona Z?
    Richiede opera.
    Iberazione interna
    E Terminara la zona l
    Segnala la necessità
    di una operazione
    esterno
    Alterna zona Z
    Vi sono operazioni esternt
    segnala che è storo
    servila la zonc
    Alferna zono
    conrrolla avole
    operaz
    Vi sono operazioni esterne
    share 208 42 838au
    2° METODO
    195
    1° PROGRAMMA
    STOP
    Elaboraz
    Mi
    Г..
    196
    20 PROGRAMMA
    STOP
    Ulyo
    FIGURA 2

Si puo' concludere affermando che il 20 metodo, a differenza del 10, assicura
in tutti i casi la massima sovrapponibilita' logicamente e tecnicamente
possibile.

Basti pensare ad un programma con due sole operazioni esterne, una LN e una RN;
in cui per ogni blocco letto vi siano piu' blocchi da registrare, per esempio
tre in media.

Il 2° metodo ci permette di accedere alle elaborazioni dei blocchi successivi
anche quando non e terminata la serie delle registrazioni su nastro dopo
l'elaborazione di ogni blocco, con vantaggio tanto piu' notevole quanto piu'
varia puo essere la durata dell'elaborazione dei singoli blocchi.

Lo schema logico ed il diagramma a blocchi della figura 2 definiscono l'
applicazione di questo secondo metodo.

In particolare nella fig. 2 abbiamo indicato con:

J = blocco generico introdotto in memoria
n numero dei blocchi da elaborare =
numero delle zone di memoria disponibili i =
indice della zona di memoria in cui vengono introdotti i dati da elaborare

1' = indice della zona di memoria in elaborazione =
indice della zona di memoria contenente dati elaborati

e' = indice della zona di memoria da cui vengono stratti i dati elaborati

numero delle zone di memoria gia' impegnate

numero delle zone di memoria con dati pronti per essere estratti.

Evidentemente le zone di memoria coincidono e sono state indicate con i diversi
quattro indici (i, i' e, e') secondo la fase di programma in cui si trovano.

Si intende inoltre che le zone di memoria sono disposte circolarmente, cioe'
all'ultima zona, i = m, seguira ancora la prima zona, i = m + 1 = 1.

Le richieste di cui precedentemente abbiamo detto, sono configurate con la
domanda ( i ‹ i' ?) cioe'quando ci si chiede se la zona che dobbiamo elaborare
sia gia' stata fornita di dati.

Le segnalazioni sono invece configurate con il contatore "h" che segnala al 2°
programma se vi sono delle zone con dati elaborati da estrarre ed in seguito da
rifornire con nuovi dati.

In conclusione, questo metodo implica che il 20 programma puo' essere avviato
una sola volta e che il 1° programma attende, prima di elaborare, che siano
stati introdotti ed estratti i dati nelle dalle zone interessate.

E' pero' possibile che ad un certo punto, il 20 programma arrivi allo STOP
mentre il 1° sta ancora eseguendo operazioni interne.

In questo caso, terminata l'operazione interna, il 1° programma riavviera' il
20 con l'istruzione $2P\* La caratteristica operativa dell' $2P\*, consente di
inserirla nel ciclo principale del 1° programma. Il governo dell'unita'
centrale la leggera' nel corso di ogni ciclo; se la sequenza di 20 programma
sara in corso, non blocchera' lo svolgimento del 10, ma ne ritardera' di soli
15 periodi di cifra l' esecuzione.

In caso contrario, se nel corso del lavoro il 20 pro gramma avra' raggiunto lo
STOP, il salto $2P\* verra eseguito e dara' corso ad una nuova sequenza del 2°
programma.

Si puo' notare che il ricorso alla S2P per il secondo metodo di utilizzazione
richiederebbe un dispositivo di sicurezza atto a neutralizzare la sua funzione
bloccante della sequenza di 1° programma in cui e' inserita.

    interno
    Salta al 20 Programma
    (101110)
    a Is
    IIII
    Im 0
    S2P
    10 0 15
    a
    Is
    I II I
    Im
    0

: carattere di eventualita'

: registro che ricorda l'indirizzo della posizione p8 dell'istruzione

: indirizzo dell'istruzione posta nella sequenza di 20 programma alla quale si
deve saltare

: il registro Im puo' modificare sia l'indirizzo IIII che il nome del registro
Is

: salta se si e' verificata l'eventualita a.

a) L'istruzione posta nel 1° programma comanda l'inizio di una sequenza di 2
pro gramma.

b) Se e' gia' in corso una sequenza di 2° programma la S2P viene riciclata fino
termine dell'esecuzione del 20 programma; eseguito lo STOP di 2° programma S2P
riavvia il programma stesso

    interno
    d
    Is
    IIII
    Im
    0
    Salta al 20 Programma *
    S2P\*
    (010010)
    Is
    III I
    Im 0
    15

: carattere di eventualita'

: registro che ricorda l'indirizzo della posizione p8 dell'istruzione

: indirizzo dell'istruzione posta nella sequenza di 20 programma alla guale si deve saltare

: il registro Im puo' modificare sia l'indirizzo IIII che il nome del registro Is

: salta se si e' verificata l'eventualita' f

a) L'istruzione posta nel 1° programma comanda l'inizio di una sequenza di 2°
pro si amila,

b) Se e' gia' in corso una sequenza di 20 programma la presente istruzione non
blocca il programma su cul e posta

    200
    SUREMA RIASSUNTIYO
    Istruzioni di salto al 2 programma
    Istruzion1
    52P
    S2P\*
    Particolarita' sulle istruzioni di 2° programma
    colloC
    IMPEGNAT
    ciro
    IN PERIODI DI CIFRA
    CONFIGURAZIONE
    Entrambe le istruzioni : 1°) permettono l'avvio di una sequenza
    di 2° programma;
    2) possono essere poste solo nel 1°pro
    S2P
    interno
    10 0 15
    ais...
    S2P
    'De e gla in corso una sequenza di 2 programma l'i
    struzione viene riciclata fino a che il 20
    non sia cernanaco.
    Eseguito lo STOP di 2° programma la S2P puo' quindi
    riavviarlo.
    52P*
    15
    o Is 1.
    S2P*
    :Se e' gia' in corso una sequenza di 2° programma
    presente istruzione non blocca il programma su cui
    posta.
    Im
    Tm
    •

