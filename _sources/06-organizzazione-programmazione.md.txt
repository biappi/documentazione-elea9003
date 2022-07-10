```{sectnum}
---
start: 6
---
```

# Organizzazione della programmazione


## Struttura della programmazione

Chiamiamo programma una sequenza di disposizioni o comandi che eseguiti uno di
seguito all'altro, portano alla soluzione di un problema secondo la logica
particolare dell' elaboratore.

L'impostazione di un programma puo' essere ovviamente diversa secondo le
caratteristiche dell'elaboratore a cui il programma stesso va indirizzato; e'
indispensabile quindi conoscerne i particolari requisiti, studiarne a fondo le
possibili utilizzazioni, per riuscire a costruire un programma che sfrutti al
massimo le capacita' della macchina.

Oltre che il numero e la struttura dei comandi che il sistema Elea 9003 e' in
grado di interpretare ed eseguire, si rende necessario conoscere di esso le
peculiari caratteristiche : la simultaneita' operativa o plurisequenzialita di
programma, e lo sfruttamento massimo del nastro magnetico come principale
supporto delle informazioni.

E' sulla traccia di queste nozioni, che il programmatore deve risolvere i
problemi che gli vengono sottoposti.

La stesura della soluzione prescelta deve pertanto essere espressa mediante un
linguaggio comprensibile alla macchina : e' percio richiesta al programmatore
la conoscenza dei simboli con cui i comandi devono essere formulati e le regole
a cui essi sono soggetti.

L'esprimersi nel modo sopradetto significa esprimersi in linguaggio macchina.

E' tuttavia opportuno notare che esiste il modo di evitare al programmatore la
fatica che questo mezzo di comunicazione comporta.

E' stato cioe' creato un linguaggio, chiamato linguaggio simbolico, molto piu
vicino a quello da noi abitualmente usato, e che quindi non richiede lo sforzo
mentale continuo di adattamento alla macchina.

E' evidente pero' che il lavoro di cui viene alleggerito l' uomo non puo' che
essere trasferito all'elaboratore che viene dotato in questo caso di un
particolare dispositivo che gli permette la traduzione di questo nuovo
linguaggio nei simboli ad esso intelligibili.

Nei capitoli che seguono si trovano illustrate le istruzioni, i comandi cioe'
che si possono impartire alla macchina, se ne elencano le caratteristiche, ed
infine si espongono le norme relative all'utilizzazione dei nastri e dei
programmi plurisequenziali.


## La codificazione delle informazioni

Le informazioni - dati, risultati e istruzioni di programma - sono
rappresentate per mezzo di caratteri alfanumerici e speciali, la cui
codificazione varia secondo il supporto utilizzato per la loro registrazione.

Per i seguenti supporti : la memoria principale e i registri del calcolatore, i
nastri ed i tamburi magnetici ed infine la banda perforata, ogni carattere e'
rappresentato da un insieme di sette variabili binarie denominate bit: sei bit
servono per la rappresentazione del carattere vero e proprio, settimo, che
viene denominato bit di disparita, serve

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

per il controllo dell' esatta registrazione delle informazioni. Piu'
precisamente il settimo bit e' 0 o 1 in modo che il numero dei bit 1 che
compaiono in ogni carattere sia dispari. Su banda perforata non compare il
settimo bit.

Tali bit sono materializzati:

- da posizioni di perforazione sulla banda perforata:

- da nuclei magnetizzabili nella memoria principale e nei registri del
  calcolatore;

- da aree di magnetizzazione nei nastri e tamburi magnetici.

I sei bit del codice permettono ovviamente di rappresentare 64 caratteri fra
cifre decimali, lettere, punteggiatura, principali simboli matematici, e altri
caratteri speciali, che solitamente vengono utilizzati per l'organizzazione
delle informazioni.

Per codice del calcolatore: si intende il codice usato per le memorie a nuclei
magnetici e per i nastri e tamburi magnetici; per "codice di perforazione: il
codice utilizzato nella perforazione della banda. Le lettere a, b, c, d, e, f,
nel codice del calcolatore, ed i numeri 1, 2, 3, 4, 5, 6 nel codice di
perforazione, indicano la posizione dei diversi bit nell'ambito del carattere
rappresentato.

I singoli caratteri possono essere raggruppati con diversi criteri in modo da
formare parole, elementi, blocchi, sequenze, ecc. La parola e' formata da uno o
piu' caratteri e identifica una unita' di informazione : una quantita'
numerica, un nome, una da ta, есс.

Durante l'elaborazione una parola puo' essere identificata mediante il suo
indirizzo iniziale di memoria e la sua lunghezza oppure per mezzo del suo
carattere estremo scelto a piacere tra i 64 possibili.

un elemento e composto da una o piu parole e rappresenta, ad esempio, un fatto
contabile o amministrativo, come un movimento bancario o di magazzino, ecc.

Un blocco e' composto da uno o piu' elementi. Una sequenza e' composta da uno o
piu blocchi.


## La codificazione delle istruzioni

Una istruzione di programma e' codificata per mezzo
di otto caratteri alfanumerici. Questi hanno normalmente la seguente funzione : il primo - nell'ordine
in cui sono esaminati dall'unita' di governo - indica la funzione F, che definisce di quale tipo di istruzione si tratta; il secondo indica il registro
T modificatore, il cui contenuto modifica l'indirizzo; i quattro seguenti contengono un indirizzo I;
gli ultimi due specificano la lunghezza L dell'informazione da trattare.

Vi sono pero' molte importanti eccezioni a questa regola: ad esempio, per tutte le istruzioni di salto
l'ultimo carattere specifica il tipo di salto; le istruzioni interessanti memorie e registri hanno la
configurazione

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

Qualunque sia il significato degli otto caratteri di una istruzione, la sua
esecuzione si svolge in due fasi: una fase preparatoria ed una fase esecutiva.

Alcune istruzioni non comportano fase esecutiva.

La fase preparatoria ha una durata di nove periodidi cifra, che si indicano con
i simboli da p0 a p8; i periodi da p1 a p8 sono utilizzati per la lettura e
l'analisi dei caratteri dell'istruzione, e per la predisposizione degli organi
interessati all'istruzione stessa.

In molti casi alcune posizioni dell'istruzione non hanno significato, e non
sono neppure esaminate dall'unita' di governo, in queste posizioni si scrivera,
per convenzione. la lettera x.  Esse possono contenere un carattere qualsiasi,
e possono quindi essere utilizzate per la registrazione di costanti o altre
informazioni.

Si e' visto che la posizione p2 dell'istruzione indica il registro T che deve
intervenire a modificare l'istruzione stessa, Se non si desidera che questa
venga modificata e' necessario indicare un registro T inesistente : cio' si
ottiene registrando in p2 il carattere # (diesis), oppure il carattere (da ...
a). E' questo un fatto generale: se in una istruzione una determinata posizione
indica normalmente uno fra diversi organi della macchina, e non si vuole
richiamare nessun organo di quel tipo, in essa si deve registrare un #
(diesis).

Le posizioni da p3 a p6 sono normalmente riservate all'indirizzo, e
precisamente

- p3 indica le unita' dell'indirizzo

- p4 indica le decine dell'indirizzo

- p5 indica le centinaia dell'indirizzo

- p6 indica le migliaia dell'indirizzo.
 
Le unita' e decine sono sempre espresse mediante caratteri numerici; le
centinaia e le migliaia invece possono essere espresse con caratteri sia
numerici che alfabetici o speciali: cio' permette di indicare con solo 4
caratteri tutti gli indirizzi della memoria principale. La tabella N. 3 in
appendice riporta la corrispondenza fra i caratteri registrati in p5 e p6 e le
migliaia e centinaia.

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
    DECINE UNITA MIGLIAIA
    UNITA CENTINAI 8 9
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


## Modifica automatica delle istruzioni

Per ogni istruzione e' indicato se essa e' modificabile automaticamente, nel qual caso il registro T modificatore e' specificato nella posizione p2.

L'operazione di modifica avviene nel modo seguente: i caratteri che si trovano
in posizione p3 p4 p5 p6 p7 dell'istruzione vengono sommati ai caratteri
contenuti nel T modificatore, dall'inizio di questo fino al bit gT per un
massimo di cinque posizioni. Le posizioni p3, p4 e p5 dell'istruzione, cosi'
come le corrispondenti posizioni 1ª, 2a e 3a del T modificatore, possono
contenere solo cifre decimali; su queste posizioni la somma viene effettuata
secondo le regole della aritmetica in base 10 e gli eventuali riporti passano
dalla 1a alla 2a posizione, dalla za alla 3ª, dalla 3a alla 42, La posizione p6
dell'istruzione e la 4ª posizione del T modificatore possono invece contenere i
caratteri alfabetici o speciali utilizzati per rappresentare le migliaia
dell'indirizzo fino a 39.000 (da 40.000 a 79.000 , da 80. 000 a 119.000, da
120.000 a 159.000 a seconda della capacita' della memoria principale). La
addizione di questi due caratteri da come risultato il carattere che
rappresenta la somma delle migliaia indicate nei due addendi (tenendo conto
dell' eventuale riporto dalla 3ª posizione di somma); oppure se viene superato
il trentanovesimo migliaio, il carattere che rappresenta la stessa somma
diminuito di quaranta. Non vi e' mai passaggio di riporto alla 52 posizione di
somma, ma di tale riporto si tiene conto sulla 4ª posizione stessa.

In altre parole, la somma sulla 4à posizione si effettua secondo una aritmetica
in base quaranta con soppressione del riporto; le cifre di tale aritmetica sono
elencate nella tabella N. 3

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
    SEGNC
    U.A.L

E' chiaro che tali regole permettono la modifica automatica degli indirizzi
entro 40.000 posizioni di memoria circolare.

L'indicazione delle centinaia nei gruppi di memoria oltre le 40.000 posizioni
si ha mediante caratteri alfabetici o speciali.  Dal carattere usato per le
centinaia l' elaboratore riconosce il gruppo di appartenenza di un indirizzo.

Finalmente la 5ª posizione del T modificatore viene sommata, secondo le regole
dell' aritmetica in base 10, alla posizione p7 dell'istruzione; tali posizioni
possono quindi contenere solo cifre decimali. L'eventuale riporto viene sommato
al carattere contenuto nella posizione p8 dell'istruzione.

La modifica automatica non esige alcun tempo supplementare di fase
preparatoria: viene poi eseguita l'istruzione modificata (nella quale
ovviamente 1' indicazione del T modificatore non ha alcun interesse).

Il contenuto del T modificatore non viene alterato dalla modifica automatica
dell'istruzione.


## Lunghezza degli operandi nelle istruzioni interne.

Le istruzioni interne sottoindicate possono specificare la lunghezza dell'
operando, o indicando con due caratteri numerici posti in p7 e p8 (LL) il
numero dei caratteri costituenti l' operando, oppure indicando il carattere
registrato in memoria dopo l'ultimo carattere dell' operando stesso.

Cio' puo' essere fatto in due modi diversi:

a) il carattere che segue l'ultimo carattere dell' operando e' ben determinato
e conosciuto dal programmatore. Esso deve essere allora registrato nella
posizione p8 mentre nella posizione p7 si deve porre

    - Q: se si vuole che, terminata l'operazione l' indirizzo del carattere
      chiave sia trasferito nel registro T9;

    - P: se non interessa che l'indirizzo del carattere chiave sia trasferito
      nelle prime 4 posizioni del registro T9.

b) l'ultimo carattere dell'operando e' seguito da un carattere alfabetico o
speciale. La posizione p8 e' allora non interessante, e nella posizione p7 si
deve porre

    - Z : se si vuole che, terminata l'operazione l'indirizzo del carattere
      chiave sia trasferi to in T9;

    - Y: se non interessa che l'indirizzo del ca- rattere chiave sia trasferito
      nelle prime 4 pg sizioni del registro T9.

In entrambi i casi l'operazione prosegue fino a che viene letto un carattere
non numerico.

Il carattere chiave letto in memoria e' sempre rigenerato nella posizione di
memoria in cui si trova.

Agli effetti del calcolo il carattere chiave e' considerato uno zero di
memoria, o piu' in generale un numero non significativo, Esso indica sempre la
fine della parola in memoria.

Se il carattere chiave ricercato si trova all'indirizzo IIII, specificato
nell'istruzione interessata. la macchina si arresta su tale posizione ed ir 19
viene registrato detto indirizzo.

Cio' non avviene se il carattere chiave e' un segno "piu' " o "meno".

Le istruzioni che operano secondo le modalita' a) e b) precedentemente indicate
sono

MA, AM, AOM, +MA, +AM, -MA, CMA, MEM, +MM, -MM, CMM, Y, +X, -X, TOL.

Le istruzioni che operano soltanto nel modo b) sono:

MT, TM, ToM, +MT, -MT, CMT, XLD, XLN, +LD.

Eventuali eccezioni a queste regole sono riportate nella descrizione delle
singole istruzioni.

Esempio:

Nel caso che si voglia trasferire in accumulatore
mediante un'istruzione MA la parola 519+ registrata in memoria come in figura :

    carauterl
    Posizioni di memoria

la parte lunghezza e indirizzo dell'istruzione puo' essere espressa


## Registrazione del programma

Perche' possano essere esaminate ed eseguite dalla unita' centrale, le
istruzioni di programma devono essere registrate nella memoria principale.

Il modo normale di leggere una informazione in memoria principale e' di
leggerla - carattere per carattere - per indirizzi decrescenti; l'indirizzo
dell'informazione in memoria e' pertanto l' indirizzo del suo estremo carattere
di destra.  Conseguentemente, le istruzioni in memoria principale sono
registrate come e' indicato dalla figura; il carattere F, che sara' esaminato
per primo dall' unita' di governo, occupa la posizione di memoria ad indirizzo
piu' elevato; il carattere Tla posizione di indirizzo immediatamente minore, e
cosi' di seguito.

Se dopo l'istruzione n deve essere eseguita l'istruzione n+1, questa dovra'
essere registrata in memoria alla destra della precedente.

    FIL
    ISTRITIONE n

Il programma puo' essere registrato in una zona qualsiasi della memoria; questa
puo' infatti contenere indifferentemente dati da elaborare, risultati o
istruzioni di programma, in ogni sua posizione. Supponiamo di registrare il
programma nelle prime posizioni di memoria, a partire dall'indirizzo 0001: il
carattere F della prima istruzione avra' quindi l'indirizzo 0008, il carattere
F della seconda istruzione l'indirizzo 0016, e cosi' via.

Da quanto si e' detto precedentemente, risulta chiaro che, perche' l'organo di
governo esegua una istruzione deve rivolgersi all'indirizzo del carattere F di
quella istruzione (dunque nel caso anzidetto, successivamente agli indirizzi
0008, 0016, ecc.).

Tale indirizzo si dice brevemente indirizzo dell'istruzione.

Ad ogni istruzione e' stato dato anche un codice simbolico piu' facile da
ricordarsi mnemonicamente quindi piu' comodo nella prima stesura di un
programma. Cosi' ad esempio l'istruzione per confrontare fra di loro due zone
di memoria che ha come codice di funzione il carattere •/. viene indicata con
il codice simbolico CMM.

Il programma normalmente viene svolto eseguendo successivamente le istruzioni
una dopo l'altra nell'ordine in cui sono registrate in memoria a partire da
quella indicata all' avvio sul quadro di controllo; speciali organi di governo
contengono 1' indirizzo dell'istruzione. Si possono svolgere pero
contemporaneamente tre diversi programmi sequenziali come sara' meglio
specificato in seguito.

Questo modo di procedere sequenzialmente puo' essere variato mediante apposite
istruzioni (istruzioni di "salto:) che permettono di eseguire sequenze diverse
sia sistematicamente sia in funzione di eventi rilevati durante l'elaborazione,
sia a seguito di condizioni impostate direttamente sul quadro di controllo. Vi
sono 90 diversi tipi di istruzione di cui 38 di salto. Le istruzioni di salto:
specificano tra l' altro l'indirizzo della prossima istruzione da eseguire.

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

