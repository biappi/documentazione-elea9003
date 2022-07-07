OLIVETTI ELEA
9003
MANUALE BASE DI PROGRAMMAZIONE
Il presente manuale e' stret
tamente riservato al persona
le della Olivetti e non puo'
essere ceduto ne' mostrato in
visione ad estranei.

INDICE GENERALE
Cap. 1° - Descrizione generale dell' elaboratore
1.1. Caratteristiche generali
1.2. La struttura modulare
1.3. La codificazione dei caratteri
1.4. I supporti di introduzione ed
estrazione
1.5. Caratteristiche tecnologiche
del sistema
pag.
10
Cap. 2° - Caratteristiche logiche dell'unita' centrale
2.1. Caratteristiche generali
2.2. Il programma
2.3. L'unita' di governo
2.4. Il flusso delle informazioni
2.5. La memoria di lavoro
2. 6. L' accumulatore e i registri T
2.7. L' unita' aritmetica e logica
2.8. I controlli
2.9. Il tavolo di comando
pag.
11
11
13
14
16
17
18
1g
20
Cap. 3° - Caratteristiche logiche del governo delle uni
ta' a nastro magnetico e delle altre unita'
d'introduzione ed estrazione
3.0. Caratteristiche generali
3.1. Governo unita' a nastro
3.2. Le unita' in linea
pag.
23
24
26
Cap. 4° - L' unita' centrale
4.1. Memoria principale
4.2. Accumulatore
4.3. Registri T
4.4. Logica aritmetica
pag.
33
37
46
48
Cap. 5° - Le unita' a nastro magnetico
5.1. Governo delle unita' a nastro
5.2. Nastro magnetico
5.3. Organizzazione delle informa-
zioni su nastro magnetico
pag.
53
54
56
Cap. 6° - Organizzazione della programmazione
6.1. Struttura della programmazione
6.2. La codifica delle informazioni
6.3. La codifica delle istruzioni
6.4. Modifica automatica delle istru
zioni
6.5. Lunghezza degli operandi nelle
istruzioni interne
6.6. Registrazione del programma
pag.
59
60
64
6.9
71
74
Cap. 7° - Istruzioni riguardanti l' unita' centrale
7.1. Istruzioni memoria-accumulatore pag.
7.2. Istruzioni memoria-memoria
7.3. Istruzioni memoria-registri
7.4. Istruzioni costanti-registri
7.5. Istruzioni di moltiplicazione
7.6. Istruzioni per la ricerca
7.7. Istruzioni di operaz. logiche
7.8. Istruzioni del tavolo di comando
7.9. Istruzioni di salto
7.10. Istruzioni di salto su errore
79
93
100
111
121
126
130
136
140
151
Cap. 8° - Utilizzazione dei nastri magnetici
8.1. Caratteristiche generali
8.2. La registrazione e la lettura
del nastro magnetico
8.3. Organizzazione delle informa-
zioni su nastro magnetico
pag. 157
n
159
161
Cap, 9° - La simultaneita' operativa dell' ELEA 9003
logica e utilizzazione del 10 e 20 programma
9.1. Considerazioni generali
9.2. Programma con istruzioni doppie
9.3. Programma con simultaneita' ope
rative organizzate
9.3.1. L'organizzazione dei dati
9.3.2. Rapporti tra le due sequenze
9.4. Metodi d'utilizz. di 20 programma
9.5. Descrizione del primo metodo
9.6. Descrizione del secondo metodo
pag. 181
183
185
185
187
188
189
194
Cap. 10° - La terza sequenza di programma
10.1. Generalita'
10.2. Caratteristiche logiche del 30
programma
10.3. Fasi di svolgimento di 30 progr.
10.4. Funzione e logica delle istruzio
ni S3P, SUO, TOL, STOP
10.5. L'istruzione S3P*
10.6. L'organizzazione di un 3°program
ma che prevede l'uso della S3P*
10.7. Esempio di 3ª sequenza con uso
della sola S3P
10.8. Esempio di 3ª sequenza con uso
della S3P*
pag. 203
204
207
208
210
211
218
" 224
Cap. 11° - Il tavolo di comando
11.1. Generalita'
11.2. Quadro di comando manuale
11.3. Il quadro di controllo
pag. 231
232
237

INDICE DELLE TAVOLE
Schema logico del sistema ELEA 9003
Esempio di flusso delle informazioni nel sistema
ELEA 9003 : I
Esempio di flusso delle informazioni nel sistema
ELEA 9003 : II
Il flusso delle informazioni (Tabella 1)
Le configurazioni dei caratteri su nastro magne-
tico e su nastro perforatc
a circolarita' della memoria
Posizione 0 per ogni gruppo tecnologico di memoria
Norme che regolano lo stato del registro del segne
Norme che regolano la complementazione (esempi)
Registri T
Tabella delle somme dei bit "f, e"
Caratteri operabili secondo la logica aritmetica
(abella
La configurazione in bit dei caratteri
La configurazione in bit dei caratteri su nastro
perforato
La configurazione delle istruzioni
Caratteri rappresentanti le migliaia e centinaia
nei diversi gruppi di memoria (Tabella 3)
Esempi di modifica automatica delle istruzioni
Legenda
Schema riassuntivo istruzioni Mem - Acc
Mem - Mer
Mem
~ Reg
Cost - Reg
di moltiplicazione
di ricerca
operaz. logiche
рад
15
25
34
36
42
44
50
52
61
62
65
68
70
77
92
99
110
120
125
129
135
Schema riassuntivo istruzioni tavolo di comando
di
saltc
di salto su errore
Organizzazione su nastro
• 1° metodo
Organizzazione su nastro
.20 metodo
Rappresentazione grafica di un'operazione NDN
Schema riassuntivo istruzioni di nastro
Le simultaneita' operative
Schema logico di 20 programma : S2P
Diagramma a blocchi di 20 programma : S2P
Schema logico di 2° programma : S2P*
Diagramma a blocchi di 20 programma : S2P*
Schema riassuntivo istruzioni di 20 programma
Schema riassuntivo istruzioni di 30 programma
Schema logico di 30 programma
S3P
Esempio di codifica di 3° programma
:S3P
Schema logico di 3° programma: S3P*
11 quadro di comando manuale
Il quadro di controllo
Pag. 139
150
155
162
163
173
180
184
191
" 192
195
" 196
201
217
219
" 220
225
" 232
" 237
INDICE DELLE FOTOGRAFIE
Elementi ad armadio del sistema ELEA 9003
Piastrina a circuito stampato
La memoria di lavoro in un armadio
Il tavolo di comando
Il fotolettore
Il convertitore da banda a nastro
La memoria di lavoro
Alcune unita' anastro magnetico collegate FR-400
Unita' a nastro magnetico
Dispositivo di lettura e registrazione FR-300
pag.
11
17
21
29
31
33
157
161
PREMESSA
Il presente manuale ha lo scopo di descri-
vere le caratteristiche basilari dell' ela-
boratore Elea 9003, e di fornire gli ele-
menti necessari alla compilazione dei pro-
grammi relativi.
Oggetto quindi dei primi capitoli sono la
struttura logica funzionale del sistema e
la dettagliata descrizione degli elementi
che lo compongono.
Nei restanti capitoli vengono analizzati
gli elementi che interessano la programma-
zione; le istruzioni, le possibilita' of-
ferte dai due canali di flusso, dai suppor
ti magnetici collegati, e dalla utilizza-
zione in linea di apparecchiature partico-
lari di introduzione ed estrazione dei da-
ti.
Non ci si sofferma invece nel presente ma-
nuale sulla descrizione tecnica e funziona
le delle unita' in linea e fuori linea che
restano oggetto di una trattazione specifi
ca.

CAP. 1° : DESCRIZIONE GENERALE DELL' ELABORATORE
1.1. Caratteristiche generali
L' elaboratore elettronico aritmetico Elea 9003 e'
uno strumento automatico di grandi capacita per
il trattamento delle informazioni aziendali e per
la risoluzione di problemi matematici, scientifi-
ci e tecnici; esso consente un ciclo di lavoro in
teramente automatico, essendo l'intervento umano
strettamente limitato alla alimentazione delle in
formazioni e alla raccolta degli elaborati.
Esso e' costituito da un insieme di apparecchiatu
re che consentono di preparare per la loro succes
siva elaborazione una grande quantita di dati,di e
seguire quindi su di essi in maniera automatica e
laborazioni matematiche, logiche o contabili di
qualsiasi tipo, di fornire con rapidita' i risul-
tati nella forma richiesta per 'utilizzazione in
mediata e l' archiviazione.
Non e' solamente un calcolatore elettronico, nel-
la accezione comune del termine, ma comprende an-
che le unita' periferiche, i collegamenti delle
unita' fra loro e con l' elaboratore centrale, ele
apparecchiature fisicamente lontane dal centro di
calcolo, ma profondamente integrate con esso, che
forniscono le informazioni su cui operare.
La parte centrale del sistema e' costituita da due
unita' : il calcolatore numerico universale, od
unita' centrale propriamente detta, e il governo
delle unita' a nastro magnetico.
Il calcolatore numerico e addetto alla elabora-
zione; e pertanto questa unita' che, seguendo le
istruzioni preparate una tantum dall'uomo, ela-
bora tutte le informazioni e controlla contemporanea
mente tutte le altre unita' del complesso. In essa,
ad esempio, un fatto contabile o amministrativo, che
e' stato rilevato all'atto stesso della sua imposta
Zione e successivamente interpretato, e elaborato e
correlato ad altri fatti in maniera del tutto auto-
matica, affinche la situazione dei vari settori di
un' azienda sia costantemente aggiornata, e siano
inoltre disponibili elementi sicuri per le decisio-
ni future.
Il governo delle unita' a nastro magnetico costitui
sce invece la centrale di memorizzazione dell'inte-
ro complesso : il nastro magnetico e' infatti il mez
zo normale per l'entrata, l'uscita e l'archiviazio-
ne dei dati, ed e' il supporto di informazioni piu'
conveniente dal punto di vista della capacita e del
la flessibilita
Il governo delle unita' a nastro magnetico non solo
controlla il funzionamento delle unita a nastro, ma
realizza il coordinamento di queste tra loro e l'uni
ta' centrale di calcolo, ed e in grado anche di ese
guire operazioni su archivi magnetici funzionando in
modo autonomo. Esso risolve infatti problemi di ri-
cerca su nastro e di aggiornamento di archivi senza
interessare l' unita' centrale.
Le altre unita' che compongono il sistema Elea 9003
sono quelle che forniscono le informazioni registra
te sui supporti di volta in volta piu' convenienti
(nastro perforato, scheda perforata, nastro magneti
co, ecc.) e quelle che danno la visualizzazione dei
risultati, mediante la compilazione di prospetti
la perforazione di schede.
ELEMENTI AD ARMADIO DEL SISTEMA ELEA 9003 ._

INITITIT
12.41
INITITIT
0000
Q
1
IT
SCHEMA LOGICO DEL SISTEMA ELEA 9003
1.2. La struttura modulare
La struttura modulare, che caratterizza l'intero si-
stema, permette di adeguare la potenza dell' Elea al
reale bisogno dell'utente, e cio' da completa garan
zia di servirsi sempre di una macchina attuale
i
problemi possono cosi' essere visti non in senso sta
tico, bensi' in senso dinamico. All'inizio, la poten.
zialita della macchina e' determinata in funzione
dei problemi che e' necessario risolvere; in segui-
to, aumentando il volume del lavoro, si possono col-
legare nuove unita', e, se cambia la natura dei pro-
blemi, si puo' ricorrere ad unita di tipo diverso
per rendere l' elaboratore piu' adatto alle nuove esi
genze. Queste prerogative consentono all'utente di e
vitare continue riorganizzazioni del centro di elabo
razione
1. 3. La codificazione dei caratteri
Un insieme di caratteri numerici, alfabetici o spe-
ciali, che ha un significato compiuto e che indivi-
dua una determinata funzione (un codice, un importo,
una descrizione, ecc.), costituisce una informazio
ne.
Per la rappresentazione delle informazioni, nell'in-
terno dell' elaboratore, e' stata scelta la forma al-
fanumerica decimale codificata in binario.
I caratteri alfabetici e le cifre decimali sono quin
di rappresentati per mezzo di configurazioni in bina
rio o "bit, in modo da poter sfruttare, nella
struzione degli elementi circuitali, tutti i vantag-
gi di semplicita' e sicurezza offerti dalla logica a
due valori. Il bit, infatti, non e altro che una va
riabile che puo' assumere solo due valori opposti, che
potrebbero indicarsi con le parole no",
"si".
0001-
re con le cifre "0m, •in; i metodi impiegati per rap
presentare materialmente un bit variano
a
seconda
del tipo di organo interessato.
Il codice binario utilizzato nell' Elea 9003 preve
de, per ogni carattere, sei bit,i quali consentono
di formare 64 configurazioni diverse e cioe'
T.11 T. T. a
le lettere dell' alfabeto, le cifre decimali e nume
rosi altri caratteri tra cui i segni algebrici e di
interpunzione.
Per la rappresentazione delle informazioni nei sup-
porti di entrata e di uscita si usa il linguaggio
che di volta in volta risulta piu' conveniente
i T
funzione del tipo di supporto e della struttura del
le informazioni su cui operare.
1.4. I supporti di introduzione e di estrazione
Le informazioni possono essere introdotte nel calco
latore da nastro magnetico, da schede o da nastro
perforato, o per mezzo di una tastiera manuale di in
terrogazione; esse possono essere estratte su nastro
magnetico, su schede o su nastro perforato, o su mo
duli a stampa ottenuti per mezzo di una telescriven
te o di stampanti parallele.
Il nastro magnetico occupa una posizione preminente
fra i supporti di informazioni utilizzati. Esso in-
fatti consente elevatissime velocita' di introduzio
ne e di estrazione, e la concentrazione di un gran-
de numero di caratteri in un peso e in un volume ri
dotti. Ha inoltre il vantaggio di poter essere uti-
lizzato un numero praticamente illimitato di volte.
Oltre ad essere il mezzo piu' idoneo per l'introdu
zione e l' estrazione delle informazioni e dei risul
tati, presenta anche grandi vantaggi come supporto
per 1' archiviazione. Poche bobine sono infatti suf
ficienti per conservare decine di milioni di dati.
I vantaggi sono rilevanti non solo nei confronti
dei tradizionali ingombranti archivi di documenti
cartacei, ma anche nei confronti degli archivi di
schede periorate.
oltre a cio' la facilita con la quale si puo' ot-
tenere in pochi minuti la duplicazione di un nastro
consente di tenere in doppio tutti i documenti piu'
importanti.
Altro supporto di informazioni utilizzato nel si-
stema Elea 9003, e', come si e' detto, il nastro
perforato.
La configurazione geometrica e le caratteristiche
strutturali del nastro perforato sono state studia
te in modo da rispondere nella maniera migliore al
le esigenze di un mezzo particolarmente adatto al-
la raccolta e alla trasmissione dei dati dalla pe
riferia al centro elettronico
Il nastro perforato si presenta come una striscia
di carta sulla quale i caratteri vengono rappresen
tati mediante una codificazione che sfrutta 6 cana
li di perforazione.
Il nastro a 6 canali presenta il vantaggio della
larghezza ridotta (la banda e' larga 20,5 mm. )
consente le 64 possibilita' di codificazione pre
viste nel sistema.
Si noti pero' che essendo l' Elea 9003 una macchina
"aperta", si possono utilizzare nastri perforati
aventi caratteristiche diverse da quelle descrit-
te
STAMPATI
NASTRO PERFORATC
FOTOLETORE D NASTRO PERFORATC
INTRODUZIONE DATI DA ELABORARE
UNTA CCNTRAC
ELABORAZIONE DELDAT
UNITA A NASTRO MAGNETICC
REGISTRAZIONE SUN
. M. DEI DAT
MAGNETICC
ESEMPIO DI FLUSSO DELLE INFORMAZIONI NEL SISTEMA
8
I FLUSSO DELLE INFORMAZIONI NEL SISTEMA
Anche la scheda perforata, elemento base degli im-
pianti meccanografici tradizionali, puo' essere uti
lizzata per introdurre ed estrarre i dati diretta-
mente dall' Elea 9003.
Il numero dei supporti collegabili e' variabile con
formemente al genere e all' ampiezza dei problemi da
risolvere.
Esistono unita' di entrata e di uscita non diretta-
mente collegate all' elaboratore. Si tratta di uni-
ta' di conversione delle informazioni da un suppor-
to ad un altro.
In questo caso il collegamento con l'unita' centra-
le e assicurato per mezzo di bobine di nastro ma.
gnetico su cui vengono registrate le informazioni in
trodotte dagli altri supporti, o che contengono i ri
sultati da trasferire ad esempio su schede o su na.
stro perforato o su moduli stampati.
All' elaboratore inoltre possono accedere informazig
ni provenienti dai piu' disparati organismi di una
azienda che siano dotati di macchine contabili
per scrivere munite di apparecchiature per la perfo
razione. In questo caso durante la compilazione dei
documenti si possono ottenere gli stessi dati sotto
forma di nastro perforato nel linguaggio accessibi-
le all' elaboratore.
Per la sua particolare struttura l' Elea 9003 puo' in
fine funzionare oltre che con unita' a nastro magne
tico, lettori e perforatori di schede e di nastro
perforato, con altre unita' diverse come ad esempio,
memoria ad accesso causale, lettori di documenti
ecc.
Queste caratteristiche contribuiscono a far si che
1' elaboratore non abbia solo un impiego limitato, ma
sia universale, atto a risolvere problemi di qual-
siasi tipo.
1. 5. Caratteristiche tecnologiche del sistema
La sicurezza operativa dell' Elea 9003 e' favorita
dalla moderna tecnologia costruttiva seguita per
la sua realizzazione.
I componenti attivi usati sono infatti esclusivamen
te transistori, gli organi di immagazzinamento del
le informazioni sono costituiti da nuclei di ferri
te, le funzioni logiche sono realizzate con diodi
al germanio.
I circuiti dell'intero complesso sono di tipo stan
dardizzato, stampati su piastrine inseribili, cosi'
da rendere facile ed economica sia la costruzione
che la manutenzione ordinaria e straordinaria del-
1' elaboratore.
I collegamenti fra le varie unita' sono ottenuti
mediante guide metalliche aeree nelle quali sono con
tenuti i cavi che assicurano il collegamento fra
tutti i circuiti particolari del sistema.
Le caratteristiche tecnologiche su descritte.el'im
piego dei circuiti aerei che evitano la necessita
di lavori di adattamento dei locali, permettono i-
inoltre di ottenere notevoli risparmi sui costi di
esercizio.
10
PIASTRINA A CIRCUITO STAMPATO

CAP. 2° : CARATTERISTICHE LOGICHE DELL' UNITA' CENTRA
LE
2.1. Caratteristiche generali
L' unita' centrale del sistema Elea 9003, intesa come
insieme di organi interni, ha il compito di ricevere
le informazioni dalle unita' di introduzione, di ela
borarle e di predisporle per le unita di estrazione:
in pratica ha la funzione di dirigere il flusso del-
le informazioni secondo le richieste dell'utilizzato
re.
E' quindi l'unita' centrale che riceve gli ordini dal
l'esterno, cioe' a dire il programma, che lo fa ese -
guire impegnando via via tutti gli elementi richiesti
Gli organi che consentono all' unita centrale di ese
guire questi compiti sono :
- 1' unita' di governo
- la memoria di lavoro
- 1' accumulatore
- 1' unita aritmetica e logica
- il tavolo di comando
2.2. Il programma
La successione delle operazioni da eseguirsi dall'ela
boratore e' determinata dal "programma" registrato nel
la memoria di lavoro: questo e' formato da una serie
di parole di otto caratteri, chiamate istruzioni.
Il programma, e' svolto eseguendo successivamente le
istruzioni partendo da quella indicata all'avvio sul
tavolo di comando; speciali registri di indirizzo i-
struzionin contengono l'indirizzo dell'istruzione in
corso e avanzano automaticamente non appena questa
sia stata eseguita.
Questo modo di procedere sequenzialmente puo' essere
variato mediante apposite istruzioni, dette istruzio
ni di salto, che permettono di alterare la normale se
quenza sia sistematicamente, sia in funzione di even
ti rilevati durante l'elaborazione, sia a seguito di
condizioni impostate sul tavolo di comando. L'indi-
rizzo dell'ultima istruzione eseguita, prima di passa
re ad un' altra sequenza puo essere ricordato automa
ticamente e senza perdita di tempo, cosi' da facili-
tare il ritorno alla sequenza iniziale.
Il programma puo' essere registrato in una zona qual
siasi della memoria principale : questa puo' infatti
contenere indifferentemente in ogni sua posizione da
ti da elaborare, risultati e istruzioni di programma.
E' possibile eseguire parallelamente fino a tre se-
quenze di programma. I tre programmi possono essere
iniziati contemporaneamente. ed eseguiti secondo un
sistema di priorita' del tutto automatico; tale prig
rita', naturalmente, entra in giuoco solo quando vie
ne richiesto simultaneamente l'intervento di uno stes
so organo da parte di due programmi.
In questo modo possono essere eseguite contemporanea
mente
una operazione aritmetica o di trasferimento inter
no,
una operazione di stampa per mezzo della stazione
di risposta alle interrogazioni,
una ricerca automatica su nastro magnetico,
• una o piu' operazioni di riavvolgimento di nastri
magnetici,
12
• una o piu operazioni di introduzione od estrazio-
ne, per mezzo di unita' a schede o nastro perfora-
to e di stampatrici parallele collegate
Una tipica utilizzazione dei tre programmi e' la se-
guente
.. il primo contiene la maggior parte delle istruzio
ni riguardanti gli organi dell' unita' centrale,
.. il secondo contiene le istruzioni riguardanti
unita' a nastro e a tamburo magnetico,
. il terzo le istruzioni relative alle unita' a sche
de perforate e alle stampatrici parallele diretta-
mente collegate.
E' interessante notare che il terzo programma fa si
che queste unita' di lettura - stampa - perforazione
impegnino in misura minima il calcolatore.
Qualora esse vengano fatte funzionare insieme ad una
unita' a nastro magnetico, consentono la conversione
nastro perforato - nastro magnetico, schede perfora-
T.e
• nastro magnetico e nastro magnetico - stampa.
In tal modo puo' dirsi che l'intero complesso e'
grado di funzionare come convertitore senza che
svolgimento delle elaborazioni ne venga alterato.
in
10
2.3. L'unita' di governo
Cuore dell' elaboratore e' l' unita di governo;
essa
dirige tutte le operazioni, comanda l' unita' aritme-
tica e logica, la memoria principale, 1' introduzio-
ne e l'estrazione dal sistema.
I compiti assolti dall' unita' di governo per esegui-
re un'onerazione sono:
il prelevamento in memoria
13
delle istruzioni da eseguire, la interpretazione di
queste istruzioni, l'avvio dei vari organi dell'ela-
boratore per svolgere le loro funzioni e il control-
lo di quanto e' stato eseguito. Inoltre il governo e'
in grado di tenere conto delle segnalazioni che i va
ri organi centrali e periferici possono dare per va-
riare il corso delle operazioni
2.4. Il flusso delle informazioni
Il collegamento fra le diverse parti componenti l'u-
nita' centrale e assicurato da due canali di trasfe
rimento, uno dei quali, detto canale interno", serve
fondamentalmente a collegare la memoria principale al
l'unita' aritmetica e logica, all' accumulatore e regi
stri T, al governo del calcolatore e sincronizzatore,
mentre l' altro, detto "canale esterno e' utilizzato
normalmente per il collegamento della memoria con le
unita' di governo dei nastri ed eventualmente dei tam
buri magnetici.
Ognuno dei due canali e' provvisto di organi per la ve
rifica di disparita', e di un indirizzatore che consen
te di ricercare nella memoria principale l'indirizzo
del carattere che deve essere trasferito o registrato.
I due canali possono pertanto lavorare in parallelo,
prelevando o registrando nella memoria principale due
caratteri alfanumerici per ogni periodo di cifra. Que
sta possibilita' viene normalmente utilizzata per ot
tenere la contemporanea esecuzione di operazioni inter
ne di introduzione od estrazione; vi sono pero' istruzig
ni che sfruttano il parallelismo dei due canali per so
vrapporre operazioni di lettura e di registrazione, o
per trasferire direttamente una informazione da una
zona all' altra della memoria.
La funzione dei due canali e' descritta graficamente
nella tabella N. 1 che mette in evidenza anche i col-
legamenti dell' accumulatore e registri T e degli ope
ratori aritmetico e di verifica.
14
GOVERNO
GOVERNO UNITÀ A NASTRO
u.n.12
з 11
IL FLUSSO DELLE INFORMAZON
Tabella N. 1
15
L' accumulatore e i registri T sono collegati alla me
moria principale dal canale interno, e agli operato-
ri aritmetico e di verifica da un proprio canale, dota
to di verifica di disparita'
Gli operatori aritmetico e di verifica sono collegati
alla memoria principale dal canale interno, attraver
so il quale ricevono il secondo operando quando il
primo si trova nell' accumulatore o nei registri T. Il
calcolatore puo' tuttavia effettuare operazioni su ope
randi contenuti entrambi in memoria, che arrivano allg
ra agli operatori aritmetico e logico l'uno attraver
so il canale esterno, l'altro attraverso il canale in
terno. Il risultato viene inviato in memoria dall'o-
peratore aritmetico attraverso il canale interno.
2.5. La memoria di lavoro
Tutte le informazioni in entrata vengono convogliate
alla memoria di lavoro. Da essa sono prelevate le in
formazioni in uscita; in essa sono considerati i ri-
sultati intermedi, il programma, le costanti di imme
diata consultazione,
ecc.
La memoria di lavoro, o memoria principale e quindi
un punto di passaggio per tutte le informazioni.
Ciascuna posizione della memoria principale e indi-
rizzabile: cio' significa che il programmatore ha la
possibilita' di indicare su quale informazione vuole
operare, specificandone semplicemente l' ubicazione
Si possono indicare tanti indirizzi diversi quanti so
no i caratteri contenuti.
E' bene definire un' altra suddivisione della memoria,
utile da un punto di vista funzionale: i gruppi di ca
ratteri che fanno parte di uno stesso insieme opera-
tivo, e che vengono operati per mezzo di un'unica i-
struzione, sono chiamati "parole". Una parola, per e
16
LA MEMORIA DI LAVORO IN UN ARMADIO ._

sempio, e' un numero decimale composto da piu
fre e segno, oppure un nome o una data.
ci-
L'indirizzo iniziale e la lunghezza sono gli elemen
ti per identificare una parola: la lunghezza puo'es
sere espressa mediante un numero di due cifre, oppu
re identificata, senza bisogno di speciali istruzio
ni, da un particolare carattere di fine parola. Que
sto e' scelto dal programmatore e puo' coincidere con
il segno algebrico della parola adiacente: in questo
caso non vengono occupate posizioni di memoria per
delimitare le parole di lunghezza sconosciuta. L'E-
lea 9003 e dunque una macchina a parole di lunghez
za variabile senza limitazioni.
2. 6. L' accumulatore e i registri T
L' accumulatore e' una piccola memoria ausiliare a nu
clei magnetici, la cui funzione principale e quel
la di contenere uno degli operandi e, successivamen
te, il risultato di un'operazione aritmetica.
T.s
sua capacita' e' di 100 caratteri alfanumerici piu
il segno. In modo analogo alla memoria di lavoro, si
puo' indirizzare la parola a partire da una qualsia
si delle posizioni dell' accumulatore. Inoltre, gra
zie alla presenza di uno speciale "bit in aggiunta
a quelli necessari per formare il carattere, puo' es
sere segnalata la fine della parola in esso contenu
ta
Altra memoria ausiliare a nuclei magnetici e' quel-
la dei registri T: essa ha la capacita' di 200 carat
teri alfanumerici indirizzabili di cinque in cinque
posizioni per un totale di 40 registri. La loro fun-
zione principale e' la modifica automatica delle i-
struzioni. Essi pero possono essere utilizzati per
operazioni aritmetiche su operandi la cui lunghezza
non superi 10 caratteri. Esiste uno speciale "bit"
analogo a quello dell' accumulatore, che segnala la
fine della parola contenuta in un registro.
Gli operandi possono essere trasferiti dalla memo
ria principale all' accumulatore e viceversa: dalla
memoria principale ai registri modificatori e vice
versa: ma non direttamente dall' accumulatore ai re
gistri e viceversa; il tempo di trasferimento di-
pende dalla lunghezza della parola.
2.7. L'unita' aritmetica e logica
L'unita› aritmetica e logica effettua i calcoli a-
ritmetici, i confronti e le operazioni logiche: mo-
difica le istruzioni per mezzo dei registri T: puo'
intervenire nei trasferimenti delle informazioni.
Dell' unita' aritmetica e logica fanno parte :
l'operatore aritmetico e logico,
- l'operatore di verifica,
~ il confrontatore.
Le operazioni aritmetiche possono avvenire fra pa-
role dotate o prive di segno: ogni operazione puo'
dunque essere algebrica o fra valori assoluti.
Gli operandi elaborati dall' unita' aritmetica e 10
gica non necessariamente devono trovarsi in due me
morie diverse (memoria princ.-accumulatore ; memo
ria principale - registri) ma possono essere conte
nuti in zone diverse della memoria principale, sen
za interessare l' accumulatore o altri organi,
con
conseguente notevole riduzione di tempo e semplifi
cazione dello svolgimento del programma
I risultati delle operazioni possono ottenersi nella
memoria, nell' accumulatore o nei registri di modifi-
ca.
Questa unita' ci permette di eseguire operazioni se-
condo 1' algebra di Boole, consentendoci:
1) 1 utilizzazione singola dei bit
2) '1' elaborazione di proposizioni logiche
Nelle operazioni di confronto l' unita' aritmetica e lo
gica ricorda se le parole confrontate sono uguali o
diverse e, in questo caso qual' e' la maggiore; il
confronto puo' essere eseguito fra parole numeriche
e alfabetiche e fra parole dotate o prive di segno.
Le caratteristiche di quest' operazione rendono parti
colarmente facile l'ordinamento alfabetico e la sele
zione di codici o nominativi di identificazione.
2.8. I controlli
L' esatta esecuzione di tutte le elaborazioni che 10
Elea 9003 svolge e' garantita da un insieme di con-
trolli automatici che individuando qualsiasi errore
non appena questo si verifichi, ne segnalano l'ubica-
zione nella macchina.
Il controllo dei dati registrati nella memoria prin-
cipale e nelle altre memorie ausiliarie e' garanti-
to dall' esistenza, per ciascun carattere, di un bit
di controllo, la cui funzione e' quella di garantire
che ciascun carattere risulti sempre costituito da
un numero dispari di bit . Pertanto il controllo del
le informazioni nella memoria si ottiene verificando
la disparita' del numero di bit in ciascun carattere.
Lo stesso procedimento di controllo e' applicato in
19
tutti i trasferimenti all'interno dell' elaboratore
Per l'organo di calcolo i controlli sono effettuati
mediante la prova del 3. Analogamente alla prova del
9 essa consiste nel confrontare il resto della divi
sione modulo 3 del risultato dell'operazione, con 11
resto della divisione modulo 3 del moltiplicando, mol
tiplicato per il resto della divisione modulo 3 del
moltiplicatore e aumentato del resto della divisione
modulo 3 dell' addendo.
Esempio
19
11
215
1
0
2
Nelle operazioni aritmetiche una ulteriore forma di
controllo e' data dalla verifica della rappresenta-
zione dei caratteri numerici ed alfabetici; in essi
infatti non compaiono mai le configurazioni c, b, a,
= 101, oppure b, a,
10
2.9. Il tavolo di comando
Il mezzo di comunicazione fra l'operatore e l'elabo.
ratore e' il tavolo di comando, che contiene i coman
di manuali, il quadro e le linee di controllo.
Per mezzo del tavolo di comando si puo' seguire ed e
ventualmente intervenire nello svolgimento di tutte
le operazioni. Esso e' costituito dai tasti e dagli
interruttori mediante i quali e' possibile agire sul
1' elaboratore dall' esterno, e dal quadro di control-
lo che contiene gruppi di indicatori che permettono
di seguire lo stato di avanzamento dell' elaborazio
ne,
individuare e localizzare eventuali anomalie.
20
JUNEWUS IU 00AVL I
• 4
0000

Al tavolo di comando e' annessa una stazione di
risposta alle interrogazioni che ha il compito di
prelevare il contenuto delle posizioni desiderate
della memoria principale, dandone la trascrizione
a stampa; e, qualora lo si desideri, contemporanea-
mente alla stampa, in modo del tutto automatico e
senza perdita di tempo, e' possibile ottenere la
perforazione su nastro di carta degli stessi carat
teri
Questa caratteristica risulta particolarmente como
da per la messa a punto dei programmi. La stampa
e' completamente indipendente dall' unita' centrale;
quest'ultima infatti si limita a fornire i caratte
ri da stampare e rimane impegnata solamente per il
tempo necessario ai trasferimenti che avvengono al
la normale velocita' di macchina.
21

CAP. 3°: CARATTERISTICHE LOGICHE DEL GOVERNO DELLE
UNITA' A NASTRO MAGNETICO E DELLE ALTRE
UNITA' DI INTRODUZIONE E DI ESTRAZIONE
3.0. Caratteristiche generali
Il governo dell' unita' a nastro magnetico e' parte co
stitutiva del sistema Elea 9003. Abbiamo gia' defini
to il nastro magnetico come il supporto piu' congenia.
le all' elaboratore elettronico; le unita' relative e
il loro governo consentono rispettivamente la sua uti
lizzazione e il collegamento tra questi e l'unita'
centrale.
Alla parte centrale dell' elaboratore e' necessario ac
cedere dall'esterno sia per fare affluire i dati e il
programma relativo, sia per estrarre i risultati del
conseguente ciclo di elaborazione. Queste due funzio
ni d'introduzione dei dati e d'estrazione dei risul-
tati, sono affidate alle unita' a nastro magnetico
che possiamo quindi definire "unita' d'introduzione"
e "unita' di estrazione" del sistema. Esse costitui-
scono la parte periferica che completa la struttura
dell' elaboratore Elea 9003.
La principale caratteristica di queste unita' e' di
poter essere collegate alla parte centrale del si-
stema sia direttamente come unita' in linea, sia in-
direttamente come unita' fuori linea.
In quest'ultimo caso esse restano staccate fisicamen
te e logicamente dall' unita' centrale e hanno lo sco
po di trasferire i dati da nastro perforato o da sche
da perforata, a nastro magnetico eseguendo l'opportu
na conversione di linguaggio.
Funzione di questi convertitori e' anche quella di e
seguire l'operazione inversa da quella ora descritta
23
di portare cioe' i dati da nastro magnetico a sche
da o nastro perforato, e a stampa.
3. 1. Governo unita' a nastro magnetico (GUN)
Fino a 20 unita' a nastro magnetico possono esse
re collegate ad un apposito governo (che costitui
sce il tramite fra esse e il calcolatore), le cui
funzioni sono molteplici ed importanti. Il governo
delle unita' a nastro, interamente transistorizza-
to, assicura e controlla il trasferimento delle in
formazioni dai nastri magnetici alla memoria prin-
cipale, e viceversa. Questo trasferimento puo' av-
venire consecutivamente oppure selettivamente,
interessare una o piu' unita' a nastro.
Le operazioni di lettura e di registrazione su na
stro magnetico oltre che simultaneamente, possono
essere eseguite infatti in modo selettivo, nel sen
so che e' possibile registrare di seguito su
Ila-
stro il contenuto di zone di memoria non contigue
e contemporaneamente suddividere le informazioni in
entrata nelle zone di memoria piu' adatte all'ela-
borazione.
Il governo delle unita' a nastro puo' anche ordina
re e controllare la trascrizione delle informazio-
ni da una unita' a nastro, in lettura, ad un'altra
unita' in registrazione: e cio' per un numero pre-
fissato di informazioni, o fino a quando non viene
trascritta una informazione determinata.
E' possibile inoltre la ricerca di una particolare
informazione registrata su nastro magnetico.
Detta operazione puo' avvenire contemporaneamente
alla trascrizione del nastro su un altro nastro
LE CONFIGURAZIONI DEI CARATTERI SU NASTRO MAGNETICO E SU NASTRO PERFORATO
TEMPORIZZ.
con evidente vantaggio, quindi, nelle operazioni di
aggiornamento di un archivio, specialmente quando
sia basso il rapporto tra variazione e contenuto
.dell'archivio stesso. Oltre a cio', il governo del-
le unita' a nastro puo' ordinare il riavvolgimento
contemporaneo di una bobina in un senso o nell'al-
tro per una determinata lunghezza, ecc.
La lettura viene controllata per mezzo della verifi
ca di disparita'; la registrazione invece viene ve-
rificata rileggendo attraverso la testina di lettu-
ra cio' che e' stato appena registrato attraverso la
testina di registrazione, ed eseguendo quindi il con
fronto.
Nel caso di disuguaglianza, le registrazione conti
nua, ma l' elaboratore denuncia l' errore, che viene
corretto subito dopo automaticamente.
3.2. Le unita' in linea
Il collegamento di queste unita' con l'unita' centra
le e' stato ottenuto mediante appositi organi le cui
funzioni sono di interpretare gli ordini trasmessi
dal governo centrale, di coordinare e sincronizzare
le operazioni che le singole unita' devono eseguire.
Ogni unita' (stampante parallela, lettore o perfora
tore di schede, lettore di nastro perforato) e' quin
di dotata di un proprio governo, mentre il sincro -
nizzatore e' unico per tutte le unita' e fa parte
del sistema centrale.
Sincronizzatore
Il sincronizzatore e' connesso da un lato all'unita'
centrale e dall'altro a tante unita' in linea quan-
26
te sono previste nella particolare installazione per
un massimo di 10. Esso contiene anche tutta la logi-
ca comune al gruppo di apparecchiature connesse e ne
cessarie allo smistamento di informazioni fra le va-
rie unita'
Esso dispone di 10 bocchettoni di entrata ed uscita
numerati da 1 a 10.
Ad uno qualsiasi di questi bocchettoni puo'
essere
connessa una qualsiasi unita' meccanica.
Dal momento in cui essa e connessa ad un certo boc-
chettone, il numero di ordine di questo diviene l'in
dirizzo dell' unita' suddetta e con questo indirizzo
il programmatore da' qualsiasi indicazione che la ri
guardi.
Data l'assenza di ogni differenziazione per i bocchet
toni, e' possibile collegare ad essi qualunque tipo
di unita' entro il limite di 10: come ad esempio 10
stampanti oppure 10 perforatrici, oppure 10 lettori di
schede oppure 10 lettori di banda.
Naturalmente nell'uso normale sono collegate simulta
neamente unita' di tipo diverso.
Lettore di schede
Il lettore di schede puo' leggere schede a 80 colon-
ne, con qualsiasi tipo di codice di perforazione, al-
la velocita' di 500 schede al minuto: e dotato di
due caselle di alimentazione e quattro caselle di ri
cezione.
La scheda si presenta sotto forma di cartoncino inde
formabile, reso elettricamente isolante con opportu-
no trattamento, ed avente forma rettangolare.
Essa puo' essere perforata in diverse posizioni, dispo
ste in 12 linee a 80 colonne. Su ognuna di queste 80
colonne si puo' rappresentare un dato numerico median
te una perforazione posta in una determinata posizio-
ne, a seconda della cifra che si vuol rappresentare ;
e' pure possibile la rappresentazione di un carattere
alfabetico mediante due perforazioni nella stessa co-
lonna, secondo particolari codificazioni.
La lettura delle schede e' eseguita da una apparecchia
tura fornita di due spazzole a 80 posizioni; la prima
spazzola e utilizzata per la lettura vera e propria.
la seconda per la verifica dell' esatta lettura.
Cot
una sola istruzione di programma si specifica l'unita
interessata, si ordina la lettura di una scheda; la re
gistrazione delle informazioni nella memoria di tran-
sito e il trasferimento delle informazioni stesse dal
la memoria di transito alla memoria principale, nelle
posizioni specificate dall'istruzione. Tutte queste o
perazioni sono rigorosamente controllate.
Perforatore di schede
Il perforatore di schede puo' perforare schede ad 80
colonne, alla velocita' di 150 schede al minuto: e' do
tato di una casella di alimentazione, di due caselle
di ricezione e di una stazione di lettura a valle del
la stazione di perforazione.
L' esatta perforazione e' verificata rileggendo le sche
de, dopo che la perforazione e' stata eseguita, per
mezzo di una stazione di lettura a 80 posizioni
Stampante in linea
E' collegata all' unita' centrale e serve astampare ad
alta velocita' le informazioni elaborate provenienti
dalla memoria principale. Le modalita' di stampa pos-
sono essere determinate sia dall' unita' centrale, sia
28
IL FOTOLETTORE

dal governo proprio della stampante .
L'operazione di stampa non ostacola il processo di e
laborazione.
Il blocco di stampa si compone di 102 ruote di stam-
pa capace ciascuna di stampare 36 caratteri alfanume
rici.
La velocita' e' di 300 righe al minuto. La memoria di
transito contiene 104 caratteri alfanumerici preleva
ti dalla memoria principale.
Prima di essere utilizzate per la stampa, tutte le
informazioni vengono controllate e, qualora si rile-
vi un errore, questo viene posto in evidenza median-
te la stampa di un carattere convenzionale ai margi-
ni del foglio.
Tutte le unita' in linea possono essere dotate di
pannelli di connessione.
Fotolettore
Questo organo permette di registrare direttamente nel
la memoria principale del calcolatore le informazio-
ni contenute su banda perforata, alla velocita' di
800 caratteri al secondo. Ad esso si ricorre normal-
mente per introdurre programmi da mettere a punto, ma
puo' essere utilizzato vantaggiosamente per l'intro-
duzione di piccole quantita' di informazioni.
La forma rettangolare dei fori di perforazione (1,65x
2,05 mm) consente il raggiungimento delle piu' alte
velocita' agli apparecchi di fotolettura.
Infatti a parita' di dimensione assiale (il lato per
29
la sezione rettangolare, il diametro per la sezione
tonda) tra fori di forma diversa, il fascio lumino-
so gode nel nostro caso di una maggiore sezione di
indagine fotoelettrica.
Il convertitore da banda o schede perforate anastrc
magnetico
Questa unita' non e' collegata al calcolatore; essa
trascrive su nastro magnetico le informazioni conte
nute su schede o banda perforata, allo scopo di in-
trodurle nel calcolatore per mezzo delle unita'
nastro magnetico, a velocita' maggiore di quella con
sentita dai lettori di schede e dal fotolettore in
linea.
Consta di due fotolettori, capaci ciascuno di legge
re 800 caratteri al secondo, e di un lettore di sche
de che legge 700 schede al minuto; il lettore di
schede e' munito di piu' caselle di ricezione,
per
agevolare l'asportazione delle schede gia' lette.
Le informazioni sono riportate su nastro magnetico
per mezzo di una unita' anastro collegata; esse ven
gono automaticamente riorganizzate, se necessario, e
trascritte a blocchi di lunghezza prefissabile fino
ad un massimo di 1200 caratteri.
Pure automaticamente vengono registrati sul nastro
magnetico, nelle posizioni opportune, i caratteri di
servizio necessari alla sua utilizzazione in fase di
elaborazione; si possono inserire sino a 10 costan-
ti diverse, e togliere o aggiungere il segno a una
parola numerica
Il controllo della lettura del carattere in uscita
da banda o scheda perforata viene eseguito rileggen
do lo stesso carattere per mezzo di due testine fo-
30
IL CONVERTITORE DA BANDA PERFORATA A NASTRO MAGNETICO

toelettriche o di due spazzole di lettura, ed ese-
guendo quindi un confronto.
Il controllo della registrazione su nastro magneti
co viene effettuato mediante il bit di disparita'
La stampante fuori linea
Questa unita' non e' collegata al calcolatore; es-
sa stampa, ad una velocita' variabile da 600 a 1000
righe/minuto, con 120 caratteri/riga, il contenuto
dei nastri magnetici ottenuto sia come risultato di
elaborazioni effettuate dal calcolatore sia per la
conversione da schede o da nastro perforato. Rice-
ve i dati da una unita' a nastro magnetico e prov-
vede alla loro organizzazione per la stampa median
te un pannello mobile di connessione e un lettore
fotoelettrico di un anello di nastro perforato.
Le informazioni da stampare sono organizzate su na
stro magnetico nel modo consueto e vengono lette e
trasferite, un blocco alla volta, nella memoria di
transito che ha la capacita' di 2048 caratteri al-
fanumerici.
Da qui vengono prelevate all'istante voluto e in-
viate alla stampa tramite un pannello mobile di con
nessione, che determina sia il tempo sia la desti-
nazione d'uscita
L'eccezionale flessibilita' del convertitore da na
stro magnetico a stampa permette di eliminare, du-
rante l' elaborazione nel calcolatore, il tempo ne-
cessario alla organizzazione dei dati per la stam-
pa e di ottenere, dallo stesso nastro, stampati di
versi sia orizzontalmente che verticalmente.
1.a
lettura del nastro, la registrazione nella memoria
di transito, la trans-codificazione, l' avanzamento
31
della carta sono sistematicamente ed automaticamente
controllati sicche' si rende superflua la presenza di
un operatore che sorvegli la stampa.
I caratteri stampabili sono: 10 numerici, 26 alfanu-
merici, e 20 fra i principali simboli matematici,com
merciali e di interpunzione. Sono ottenibili fino a
6 copie simultaneamente.
LA MEMORIA DI LAVORO

CAP.
4°: L° UNITA CENTRALE
4. 1. Memoria principale
La memoria principale e' costituita da nuclei di fer
rite a ciclo di isteresi rettangolare. I nuclei sono
montati su piani, ognuno dei quali ne contiene 10.000.
Sette piani sovrapposti contengono 70000 bit neces-
sari a rappresentare 10.000 informazioni alfanumeri.
che; il loro insieme forma un elemento tecnologico
di memoria.
Due elementi tecnologici di memoria, per un totale di
20.000 informazioni alfanumeriche, costituiscono in
vece la minima unita funzionale di memoria: un cal
colatore puo' disporre di un numero di unita' di me-
moria variabile da 1 a 8, corrispondenti ad un nume-
ro di informazioni alfanumeriche compreso fra 20.000
e 160.000.
I sette bit costituenti ogni carattere vengono opera
ti in parallelo: il tempo necessario al loro trasfe
rimento da una zona ad un' altra della memoria, o dal
la memoria agli altri organi della unita centrale e'
di 10 microsecondi; tale intervallo di tempo e' det
to "periodo di cifra
In un periodo di cifra si possono estrarre o intro-
durre dalla memoria due caratteri, ed operare su di
essi.
La memoria e' circolare e indirizzabile posizione per
posizione mediante indirizzi di quattro cifre la cui
aritmetica e per contare modulo 40.000.
Cio' significa che in una macchina con memoria di
20.000 posizioni qualora si oltrepassasse l'indiriz.
zo 19.999 (I999), in tutti gli organi programmabili
(memoria, registri T, comparatori ecc.) apparirebbe-
ro numeri relativi alle posizioni di una memoria a-
vente la capacita' di 40.000 posizioni: cioe' €000
(20.000), J000 (21.000): K000 (22.000), ecc. Essen-
do pero' la memoria di 20.000 posizioni e' evidente
che per la circolarita' della memoria l'indirizzo
E000 corrisponde alla posizione 0000 e che l' indi-
rizzo J000 corrisponde alla posizione 1000 ecc., co
me illustrato dalla figura seguente:
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
Per quanto riguarda le memoria con piu' di 40.000
posizioni vi e l' impossibilita di percorrere me-
diante operazione aritmetica (e modifica automati-
ca) l'intero insieme degli indirizzi.
Accade cioe' che oltrepassando l'indirizzo 39.999
('999) 1'indirizzatore sceglie non 1' indirizzo
40.000 (0000) ma l'indirizzo 0000.
Non esiste cioe' la possibilita
attraversare
con operazioni aritmetiche i multipli di 40.000.
Questo non avviene invece per aggiornamenti effet-
tuati nell' ambito di un gruppo di memoria di 40.000
caratteri.
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
4.2. Accumulatore
L' accumulatore e' una speciale memoria a 100 posi-
zioni; ad ogni posizione e' associato un indirizzo.
Gli indirizzi vanno da 00 a 99; l'indirizzo succes-
sivo al 99 e l'indirizzo 00, cioe' 1' accumulatore
e' circolare. L'indirizzo iniziale di una parola con
tenuta in accumulatore e' dato dal contenuto di uno
speciale registro detto DA.
DA - Mediante l'istruzione DA si puo' fissare l'ini
zio dell' accumulatore in una qualsiasi delle sue 100
posizioni. Cio' significa che il primo carattere di
una parola che venga prelevata o inviata all' accumu
latore proverra' o andra' all'indirizzo fissato me-
diante la istruzione DA. I caratteri successivi han
no riferimento agli indirizzi identificati da nume
ro d' ordine maggiore.
Esempio:
Accumulatore do
po un trasteri.
mento con DA = 91
del numero di
cifre: 12345
.. Si noti l'influen
za della circola
rita' della
MILE
moria.
000000
6 • • . . . .. •• 7.654,32,1
13 4 5
BIT GA
Bit gA - Il registro DA indica dunque l' indirizzo di
una parola contenuta in accumulatore; la fine del-
l'informazione e' segnata invece da uno speciale bit
detto gA. Cio' permette di utilizzare l' accumulato-
re per contenere piu' parole; ad ognuna di esse cor
rispondera' un bit gA che ne segnala la fine, men-
tre il contenuto del registro DA rappresenta l'ini-
zio della parola sulla quale si vuole operare.
I diversi bit gA sono materializzati da un ottavo
piano di nuclei ferromagnetici, che si aggiunge ai
sette utilizzati per la registrazione dei caratteri
alfanumerici e per la verifica di disparita'.
Il bit gA ha i seguenti effetti :
- nelle operazioni aritmetiche le cifre che lo
guono sono considerate degli zeri;
- nelle operazioni di trasferimento da accumulatore
a memoria il bit gA non viene considerato.
La posizione del bit gA e' determinata dalle seguen
ti regole generali
l'istruzione AoM (trasferimento da accumulatore a
memoria con azzeramento delle posizioni di accumu
latore trasferite) pone un gA in corrispondenza di
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
- L'istruzione di trasferimento da memoria ad accu-
mulatore (MA) pone un bit gA in corrispondenza del
l'ultimo carattere trasferito e lascia inalterati
i bit gA posti precedentemente purche' non si ri-
feriscano ai caratteri trasferiti.
38
Esempio
00000000
- Accumulatore do-
Do un AoM (esem-
pio precedente) e
un trasterimento
con DA = 02,
del
numero 1420.
117 6 1 919111 9 91 1/1010141
HF 5 S
5700142000
- Nelle istruzioni aritmetiche il bit gA viene di
sposto secondo le seguenti regole
. se l' operando chiamato dalla memoria ha una lun
ghezza minore o uguale al numero di posizioni
comprese fra DA e gA, questo non viene sposta
to;
. in caso contrario il gA viene posto in corri-
spondenza della cifra piu' significativa del-
l' operando chiamato da memoria;
. nel caso di superamento di capacita' dovuto a ri
porto, il gA viene posto in corrispondenza del -
la cifra piu' significativa e cioe' eventualmen
te una posizione piu' a sinistra di quella che
risulterebbe diversamente
39
L'esempio che segue mostra la posizione del bit gA
attraverso una successione di istruzioni
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
Per quanto riguarda le operazioni algebriche il va-
lore assoluto di un numero puo' essere registrato in
accumulatore sia nella sua vera grandezza che nel
suo complemento alla potenza di 10 immediatamente
superiore : un apposito organo a flip-flop segnala
con la sua posizione quale delle due rappresentazio
ni e' in quel momento utilizzata.
La memorizzazione del segno e' invece affidata ad
uno speciale registro, chiamato "registro del segno:
che segnala se la parola contenuta in accumulatore
e' dotata di segno, e in caso affermativo, se il se
gno e spiu' : o "meno*
Questo registro e il flip-flop segnalatore dei com-
plementi possono essere considerati come organo uni
co che puo' indicare una eventualita' fra sei possi
bili : le due eventualita' -in vera grandezza e in
"complemento: si compongono infatti con le tre even
tualita' "non segnato, "segno piu' » e "segno meno .
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
Altri tre registri concorrono all'esecuzione delle
operazioni algebriche (le operazioni aritmetiche pos
sono essere considerate operazioni algebriche
t.ra
operandi di segno + : in questo caso pero' i risul-
tati non sono ovviamente segnati).
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
Essi servono a ricavare rispettivamente :
(1) il segno dell' operazione da eseguirsi (somma, sot
trazione);
(2) il segno dell' operando contenuto in memoria;
3) il segno del moltiplicatore.
Si hanno quindi complessivamente 4 registri e conse
guentemente 4 indicazioni di segno per ogni opera-
zione. (Il segno del moltiplicatore non e' conside-
rato nelle operazioni di somma e sottrazione e il se
gno della moltiplicazione non compare nel registro
del segno dell'operazione; in sua vece si hanno i se
gni + o - ad indicare se il prodotto ottenuto va som
mato o sottratto al contenuto dell' accumulatore).
In base al numero complessivo dei segni "-. che pos
sono comparire nei quattro registri, durante una ope
razione, si hanno le seguenti norme che regolano la
complementazione dei dati operandi e dei risultati:
10) Se il numero dei segni .. e dispari: si ha la
complementazione dell' operando contenuto in me-
moria con inversione di segno prima che su que-
sti si effettui l'operazione richiesta.
21
20) Se in seguito alla complementazione del dato in
memoria e alla sua inversione di segno si ottie
ne un risultato con "riporto", il riporto viene
annullato e il risultato compare in vera gran-
dezza". Vedi esempio 1.
30) Se in seguito alla complementazione del dato di
memoria e della sua inversione di segno si ot-
tiene un risultato senza riporto il risultato
compare in "complemento. Vedi esempio 2.
Esembio
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
4°) Se in seguito alla complementazione del dato di
memoria e della sua inversione di segno si ot-
tiene un risultato nullo = 0, il risultato e' in
dicato in "vera grandezza". Vedi esempio 3.
50) Se il numero dei segni
-" e' "pari", 1' operan-
do di memoria viene operato tale e quale se si
tratta di una somma, o col segno inverso se
tratta di una sottrazione. Vedi esempio 4.
si
Per quanto riguarda il trasferimento di un operando
o di un risultato dall' accumulatore a memoria si han-
no le seguenti possibilita'
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
4. 3. Registri T
L'insieme dei registri T e' costituito da una memo-
ria a nuclei magnetici della capacita' di 200 carat
teri alfanumerici, indirizzabili di 5 in 5 posizio-
ni. Ad ogni possibile indirizzo corrisponde un regi
stro T; vi sono dunque 40 di tali registri.
Ogni registro ha la lunghezza massima di 10 posizio
ni; e' chiaro quindi che, ad esempio, il registro 2
ed il registro B si sovrappongono parzialmente.
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
Quando il registro T e' utilizzato per modificare
un'istruzione, o, come si dice, quando opera come mo
dificatore, al massimo i primi 5 caratteri del suo
contenuto vengono utilizzati; conseguentemente, tut
ti i 40 registri possono operare come modificatori
senza che risulti alcun inconveniente dallaloro par
Ziale sovrapposizione
4 6
Immaginando per convenienza di esposizione le posi-
zioni di memoria numerate da 000 a 199, la parola re
gistrata a partire dall' indirizzo zero, normalmente
uno dei fattori della moltiplicazione, puo' avere una
lunghezza qualsiasi fino ad un massimo di 100 carat
teri, piu' un segno che viene trasferito in un appo
sito registro; le parole registrate a partire dagli
altri indirizzi possono avere un massimo di 10
ratteri.
Bit gr - Non esiste per i registri T 1' analogo del-
la DA: le informazioni contenute in ogni registro
hanno sempre inizio dall'indirizzo corrispondente a
quel registro. Esiste invece l' analogo del bit gA
detto gT; anche per i registri T il hit gT e' mate-
rializzato da un ottavo piano di nuclei magnetici.
Esiste ambiparita' anche per quanto riguarda il re-
gistro del segno; solo che questo resta accessibile
esclusivamente mediante l'istruzione "y".
Per quanto riguarda l'utilizzazione ed il posiziona
mento del bit gT valgono le stesse considerazioni
fatte a proposito del bit gA ovviamente sostituendo
le istruzioni per •1' accumulatore con le corrispon-
denti per i registri T.
Nelle singole istruzioni verra' specificato quando
il risultato puo' avere lunghezza più lunga del
piu' lungo degli operandi ed in quali casi si ha in
dicazione di overflow.
Un registro T viene identificato nell'istruzione da
un carattere; la tabella precedente indica l'indiriz-
zo iniziale di ogni registro Tin corrispondenza del
carattere che lo identifica.
47
4. 4. Logica aritmetica dell' Elea 9003
Operazioni aritmetiche che possono interessare lame
moria, 1' accumulatore e i registri T ( + MM :
+ MT; - MT; + MA;
- MA; + TM ; + AM ).
Le operazioni su caratteri speciali non possono es
sere effettuate. Nel caso si abbiano operazioni su
tali caratteri si ha indicazione di errore nell'uni
ta' aritmetica e logica.
Possono invece essere effettuate operazioni su ca-
ratteri alfabetici e ovviamente su caratteri numeri
ci.
La macchina sa distinguere questi caratteri dagli al
tri, in quanto in essi non appaiono le configurazio
ni c, b, a = 101, oppure b, a = 10
Operando su numeri :
a) la parte numerica (*) viene operata normalmente
(modulo 10)
b) un eventuale riporto non influisce sulla configu
razione della parte alfabetica (*).
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
1° la parte numerica viene operata allo stesso mo
do dei caratteri numerici, tenendo conto del va-
lore numerico dato alla lettera in questione (ve
di tabella 2);
20 i risultati delle operazioni sono espressi me-
diante uno o due caratteri a seconda che si ab.
bia avuto o no riporto dalla somma dei due ca-
ratteri;
3° la parte alfabetica viene operata distintamente
dalla parte numerica, secondo modulo aritmetico
4 (da cul 3 + 1 = 0):
4° la complementazione nella parte alfabetica av-
viene anch' essa secondo modulo aritmetico 4.
Si ha pertanto :
Esempio 10
f
0 1 (1)
+ D 0 1 (1)
= Q 1 1 (2)
d c b a
0 1 0 0 (4)
0 1 0 0 (4)
1 1 1 1 (8)
Esempio 20
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
I caratteri alfabetici ripetono nei bit "d
c, b, a" le configurazioni dei caratteri
numerici a cui sono associati (vedi tabel-
la 2) e si distinguono pertanto solo per la
configurazione dei bit "f, e".
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
CAP.
5°: LE UNITA° A NASTRO MAGNETICO
5.1. Governo delle unita' a nastro
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
5.2. Nastro magnetico
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
5.3. Organizzazione delle informazioni su nastro ma
gnetico
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

CAP.
6°: ORGANIZZAZIONE DELLA PROGRAMMAZIONE
6.1. Struttura della programmazione
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
6. 2. La codificazione delle informazioni
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
6.3. La codificazione delle istruzioni
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
S. 4. Modifica automatica delle istruzioni
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
- 6.5. Lunghezza degli operandi nelle istruzioni in-
terne.
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
6.6. Registrazione del programma
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

CAP. 7° : ISTRUZIONI RIGUARDANTI L° UNITA CENTRALE
7.1. Istruzioni memoria-accumulatore
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
7.2. Istruzioni memoria-memoria
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
7.3. Istruzioni memoria-registri
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
7.4. - Istruzioni costanti-registri
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
7.5. Istruzioni per la moltiplicazione
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
7.6. Istruzioni per la ricerca in memoria
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
7.7. Le istruzioni per le operazioni logiche
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
7.8. Istruzioni relative al tavolo di comando
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
7.9. Istruzioni di salto
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
7.10. Istruzioni di salto su errore
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

CAP
8° : UTILIZZAZIONE DEI NASTRI MAGNETICI
8.1. Caratteristiche generali
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
8.2. La registrazione e la lettura del nastro
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
8. 3. Organizzazione delle informazioni
magnetico
su nastro
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
e) Non e' possibile porre ns o ni inesistenti (carattere
# )
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
CAP. 9° : LA SIMULTANEITA' OPERATIVA DELL' ELEA 9003;
LOGICA E UTILIZZAZIONE DEL 1° E 2° PROGRAMMA
9.1. Considerazioni generali
Alla memoria principale dell' ELEA 9003 si puo' acce
dere mediante due canali di trasferimento delle in-
formazioni, uno interno ed uno esterno. Il canale in
terno collega la memoria principale agli organi in-
terni della macchina; il canale esterno e utilizza
to per il collegamento con le unita' a nastro, tra-
mite il relativo governo, e quando si opera diretta
mente fra due diverse zone di memoria.
L'istruzione dell' ELEA 9003 si svolge, come abbiamo
gia' visto, in due fasi distinte : la fase prepara-
toria, durante la quale il canale interno della mag
china e impegnato in continuita per la durata di
nove periodi di cifra, la fase esecutiva, che varia
a seconda della funzione che l'istruzione stessa de
ve svolgere, e che impegna sempre per un periodo di
cifra il canale interno, prima che si inizi l'esecu
zione vera e propria che potra' impegnare uno del
due canali.
Sotto questo punto di vista le istruzioni dell' ELEA
9003 sono raggruppate nel seguente modo
1°) istruzioni che impegnano il canale interno;
20) istruzioni che impegnano il canale esterno e il
governo delle unita' a nastro magnetico;
30) istruzioni che impegnano il canale interno ed il
canale esterno;
40) istruzioni che impegnano il canale interno, ilca
nale esterno e il governo delle unita' a nastro
magnetico;
#
181
50) istruzioni che impegnano il governo delle uni-
ta' a nastro magnetico.
In particolare l'istruzione avvolgi nastro (AV) puo'
essere eseguita simultaneamente con aualsiasi altra
istruzione purche' quest'ultima non si riferisca al
l' unita' a nastro indicata nell'istruzione di avvol
gimento.
In forma tabellare indichiamo le possibili sovrappo
sizioni tra le varie categorie di istruzioni prece-
dentemente definite.
Gruppo di appartenenza
dell'istruzione
Gruppi di appartenenza delle istru
Zioni che si possono svolgere in
simil tanerta' con la prim
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
Dall' esame di questa tabella risulta cheimetodi di
organizzazione di un programma sono due
a) un programma che prevede 'utilizzazione di istru
zioni doppie e quindi che esclude ogni simulta-
neita' operativa organizzata;
b) un programma che prevede 'utilizzazione delle si
sultaneita operative delle istruzioni dell' ELEA
9003.
Mentre nel caso a) lo svolgimento del programma si
ripartisce linearmente sui due canali della macchi-
na e quindi non vi e' alcuna ricerca di ottimizza-
zione dell' impegno degli stessi, in un programma di
tipo b) questa ricerca e' necessaria ma, come vedre
mo, non puo' essere fatta dal programmatore.
182
cio' significherebbe infatti tener conto dello svol
gimento di ogni singola istruzione, predisporre il
programma in modo da inserire tra due successive i-
struzioni esterne un numero opportuno di istruzioni
interne, tale che la loro durata complessiva fosse
uguale alla durata dell'istruzione esterna contempo
raneamente eseguita.
La realizzazione della simultaneita' operativasi ba
sa ed e' valida per le particolari caratteristiche
logiche dell' ELEA 9003 che consentono alla macchina
di operare su piu' sequenze di programma contempora
neamente.
In questa analisi terremo conto delle sequenze defi
nite di 10 e di 20 programma mentre esamineremo in
altra sede la sequenza che e' propria del collega-
mento delle unita' in linea dell' ELEA 9003.
Esaminiamo ora le caratteristiche particolari dei
due tipi di programmi precedentemente definiti.
9.2. Programma con istruzioni doppie
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
9.3. Programma con simultaneita' operative organiz
zate
Un programma di questo tipo, sempre non consideran-
do la sequenza del terzo programma, comprendera due
Sequenze di istruzioni : una definita di primo pro.
gramma ed una di secondo programma.
Le caratteristiche principali di questa organizza-
zione sono due : a) la necessita di una particola-
re organizzazione dei dati; b) i rapporti tra le due
sequenze e la logica della simultaneita' interna.
9.3.1. L'organizzazione dei dati
Per utilizzare la possibilita' di sovrapposizione
del tempo esecutivo dei due programmi e' necessario
assegnare ad ogni flusso di informazioni piu' zone
di memoria; in pratica sono sempre sufficienti due
zone.
Si esamini infatti questo caso elementare. Dobbia
mo introdurre da nastro magnetico delle informazia•
ni su una zona di memoria che indichiamo con Zi (zo
na di introduzione), elaborarle depositando i risul
tati in un' altra zona di memoria che definiamo Ze
(zona di estrazione), e infine estrarle da quest'ul
tima zona registrandole su nastro magnetico
Utilizzando una sola zona per ogni flusso di dati,
cioe' in pratica per ogni operazione esterna ( nel
caso nostro una IN e una RN ), il programma risulte
rebbe cosi' strutturato
1) LN sulla zona Zi.
2) Elaborazione dei dati contenuti in Zi e deposi-
to dei risultati in Ze.
185
3) RN dalla zona Ze.
4) Di nuovo, LN nella zona Zi, ecc.
Ovviamente, non e' possibile attuare alcuna simul.
taneita', tra l'elaborazione e l'introduzione o la
estrazione dei dati, perche' l'elaborazione sulla
zona Zi non puo' aver luogo finche' non e'
servita dalla LN e la estrazione dei risultati da
Ze deve attendere che la fase di elaborazione sia
terminata.
Se, si ricorre ad una doppia zona di memoria per ogni
operazione esterna, si potra' introdurre le infor-
mazioni una volta nella zona Zi e una volta nella
zona Z'i, ed estrarle una volta dalla zona Ze e una
volta dalla zona Z' e. Il programma risultera' cosi'
strutturato:
1) LN sulla zona Zi
2) a) elaborazione dei dati contenuti in Zi e de-
posito dei risultati in Ze
b) LN sulla zona Z' i
3) a) elaborazione dei dati contenuti in Z'i e de
posito dei risultati in Z'e
b) RN dalla zona Ze, seguita dalla LN sulla Zi
4) a) elaborazione dei dati contenuti in Zi e de-
posito dei risultati in Ze
b) RN dalla zona Z' e seguita da LN sulla zona
Z' i, ecc.
Le operazioni a e b risultano eseguite contempora-
neamente, cosa che prima non era possibile.
Abbiamo detto che per avere simultaneita' operati-
va tra elaborazione ed introduzione o estrazione e'
necessario servirsi di almeno due zone di memoria
in alternanza : in effetti le zone utilizzate al-
ternativamente potrebbero essere piu' di due con
186
qualche vantaggio di tempo in quanto, in alcuni ca-
si, aumentando le zone utilizzabili si eliminano i
tempi di attesa di uno dei due programmi. Ma si oc-
cuperebbero molte posizioni di memoria, non sempre
disponibili e si appesantirebbe il programma con ul
teriori istruzioni di servizio
L' alternanza di zona per le operazioni esterne deve
essere preparata dopo che e stata eseguita l'opera
zione sulla zona interessata : ad esempio, dopo che
si e' dato inizio all'istruzione IN sulla zona Zi,
si predispone il relativo registro di modifica per
che' la volta successiva la stessa LN sia eseguita
sulla zona ' i. In modo analogo si predispone 1° al-
ternanza per l'istruzione RN; in entrambi i casi si
attua un meccanismo di flip-flop
Generalmente le istruzioni di elaborazione interna
saranno modificate da uno o piu° registri per poter
operare dalle zone Zi a Ze e da Zi a Ze.
9.3.2. Rapporti tra le due sequenze di programma
L' esame delle due sequenze di programma e la contem
poranea esecuzione vengono eseguiti dalla macchina
secondo le seguenti regole logiche interne
a) Se nel 1° programma sono in corso istruzioni che
riguardano il canale interno e nel 20 istruzioni
che riguardano il canale esterno o viceversa
due programmi agiscono simultaneamente.
b) Se nel 10 programma sono in corso istruzioni in-
terne, e si verificasse che il 20 debba eseguire
anch' esso un' istruzione interna, quest' ultimo
prende la precedenza bloccando il 1° programma..
c) Se uno dei due programmi dovesse eseguire un' i-
struzione doppia (es. MEM, + MM, ecc.), che impe
gni entrambi i canali, questo programma prende co
munque la precedenza
187
Come regola generale il secondo programma ha sempre
la precedenza sul primo; in ogni caso pero' la pre-
cedenza viene presa dopo che sia stata eseguita la
fase esecutiva dell'istruzione in corso.
Da quanto detto, per avere la massima sovrapposizio
ne e' bene che sul 10 programma non vi siano mai i-
struzioni esterne, e che non si usino mai in nessur
programma istruzioni doppie.
Inoltre e' bene nel 20 programma limitare allo stret
to indispensabile l'uso di istruzioni interne.
E' consigliabile inoltre evitare l'uso degli stessi
registri nei due programmi, mentre 1' accumulatore
dovra' essere usato su un solo programma.
In ogni modo se si volesse fare ugualmente uso del-
1' accumulatore e degli stessi registri e' necessa-
rio scaricarli prima e ricaricarli dopo averli usa-
ti.
9.4. Metodi di utilizzazione del 20 programma
Ogni metodo di utilizzazione del 10 e del 2°program
ma deve soddisfare alle due seguenti condizioni che
costituiscono dei vincoli per il programmatore.
a) L'elaborazione sulla zona 2 puo' essere eseguita
solamente quando l'operazione esterna che serve quel
la zona ha avuto termine.
L' alternanza delle operazioni esterne deve quindi
essere predisposta sul 20 programma e quella delle
operazioni interne sul 1°.
b) Appena eseguita l' elaborazione interna e' neces-
sario richiedere una operazione esterna sulla stes-
188
sa zona di memoria, per evitare eventuali tempi di
arresa.
E' pertanto necessario programmare delle segnala-
zioni da parte del 20 programma al 10 programma ad
ogni operazione esterna eseguita, e delle richieste
di nuove operazioni esterne da parte del 10 al 20.
Esistono due metodi di utilizzazione delle simulta
neita' operative, realizzabili mediante le due
1--
struzioni di salto speciale S2P e S2P*
9.5. Descrizione del primo metodo
Al secondo programma si accede mediante l'istruzio
ne S2P (salta al secondo programma) posta sul pri-
mo programma.
La lettura di questa istruzione provoca l'interru-
zione della sequenza in corso: infatti la macchi-
na invia l'indirizzo di salto contenuto nella S2P
nel registro indirizzi istruzioni del 20 programma
e inizia l'esame delle istruzioni poste in questa
seconda sequenza.
Da questo momento la macchina si comporta rispet-
tando le regole di precedenza gia' descritte. Ef-
fettuato il salto cioe', i due programmi procedono
parallelamente e il loro avanzamento contemporaneo
dipende solamente dalle singole istruzioni poste
sui due programmi. L'organizzazione del programma
di lavoro deve prevedere l'esecuzione di una opera
zione interna di elaborazione e di una operazione
esterna di introduzione e di estrazione alla vol-
ta.
189
Dato l'impegno dell' alternanza delle zone per le sin
gole operazioni si deduce che se la operazione in-
terna e' eseguita sulla zona Zi, contemporaneamente
l'operazione esterna e' eseguita sulla zona Zi.
E' chiaro allora che e' possibile avviare l'opera-
zione interna sulla zona ' i solo quando e' termina
ta la relativa operazione esterna.
In dettaglio, si avra' allora questo svolgimento :
dopo un inizio di programma che provvede ad intro-
durre i primi dati nelle zone ed a richiedere l'in-
troduzione dei dati successivi nelle zone alterne ad
essi destinate, viene avviato il secondo programma
che esegue le operazioni esterne richieste. Nel frat
tempo il 1° programma provvede ad eseguire le neces
sarie elaborazioni e, posizionando opportuni devia-
tori, ad annotare le operazioni esterne che piu'tar
di dovra' richiedere al 20 programma.
Al termine delle elaborazioni, il 1° programma pas-
sa ad una istruzione di salto $2P che conduce ad uno
STOP. Ora, l'istruzione S2P ha la proprieta' di non
venire eseguita fino a che e' in corso il 2°program
ma : cio' obbliga il 1° programma ad attendere il
termine delle operazioni esterne in corso, o, se que
ste sono gia' terminate, gli permette di passare ol
tre dopo un' attesa di soli 25 periodi di cifra (15
per la istruzione $2P, 10 per lo STOP).
Solamente dopo aver eseguita l'istruzione S2P il 10
programma provvede a richiedere al 20 le operazioni
esterne precedentemente annotate.
Soddisfatte tali richieste il 1° programma avvia nuo
vamente il 20 con una istruzione $2P e riprende
elaborazione.
Tale organizzazione da la sicurezza che le due con
dizioni richieste siano soddisfatte: infatti, appe
190
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
na terminata l' elaborazione sulla zona 2, il 1° pro
gramma ha provveduto, ad esempio in un ciclo n, ari
chiedere l'operazione esterna che serve quella
7.0 -
Il d.
Durante il ciclo n + 1, viene effettuata sia l' ela-
borazione sulla zona alterna, che l'operazione
e-
sterna sulla zona 7 : all'inizio del ciclo n + 2,in
cui si dovranno elaborare le informazioni su questa
ultima zona, sono terminate tutte le operazioni e-
sterne richieste durante il ciclo n, e quindi certa
mente e' terminata anche l'operazione sulla zona Z.
caratteristica di questo metodo e quindi di assicu
rare una protezione globale contro il pericolo di
iniziare l' elaborazione su una zona non ancora ser-
vita, imponendo al 1° programma di attendere anche
quando le operazioni esterne non ancora effettuate
non riguardano l'elaborazione che dovrebbe inizia
re.
Per tale motivo, tale metodo non si adatterebbe, per
esempio, al caso in cui fossero previste piu' di due
zone di alternanza per ogni operazione esterna.
In conclusione questo metodo implica che il program
ma attenda la fine del 20 programma in corso prima
di riprendere il ciclo delle operazioni interne, e
il successivo rilancio del 20 programma mediante una
S2P posta sul 10
Lo schema logico e il diagramma a blocchi della fi-
gura 1 definiscono in tutti gli aspetti l•applica-
zione di questo primo metodo. Con J verra indicato
il generico blocco da introdurre in memoria; con n
il numero dei blocchi da elaborare e con B. X.d.
M. 7 i deviatori utilizzati.
193
9.6. Descrizione del secondo metodo
Questo metodo si basa non su una condizione rigida
di rapporti tra il 10 ed il 20 programma, come avve
niva nel primo metodo, ma su scambi di informazioni
programmati tra le due sequenze.
Gli scambi da realizzare tra i due programmi sono :
a) Il 1° programma "segnala", col massimo anticipo,
le proprie future necessita', perche' le zone in
teressate siano rifornite di dati one siano sgom
berate. Chiameremo tali comunicazioni
"segnala-
Zioni'
b) Il 10 programma "richiede" l'esecuzione di una da
ta operazione esterna su una zona; se la "richie
sta" non puo' essere subito soddisfatta, il 10
programma attende.
Dato che il 20 programma, quando ha ricevuto la
"segnalazione fara' il possibile per prepararsi
a soddisfare la "richiesta che seguira', senza
bisogno di solleciti, sara' opportuno effettuare
la richiesta all'ultimo momento.
Fisicamente, sul programma, non e' necessario che
ci sia una corrispondenza 1-1 tra segnalazionin
e "richieste", perche', mentre le segnalazioni
servono ad avvisare il 20 programma della neces-
sita' di una operazione esterna, le richieste ser
vono ad assicurare il 10 programma che l'opera-
zione esterna su una determinata zona e' stata e
seguita.
Sarebbe necessario introdurre un ulteriore deviato-
re che consentisse di accedere alla istruzione solo
quando il 20 programma ha raggiunto lo STOP e di sca
valcarla in via normale, quando il 20 programma
A!
in corso.
Si puo' concludere affermando che il 20 metodo, a
differenza del 10, assicura in tutti i casi la mas-
194
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
sima sovrapponibilita' logicamente e tecnicamente
possibile
Basti pensare ad un programma con due sole operazio
ni esterne, una LN e una RN; in cui per ogni blocco
letto vi siano piu' blocchi da registrare, per esen
pio tre in media.
Il 2° metodo ci permette di accedere alle elabora
zioni dei blocchi successivi anche quando non e ter
minata la serie delle registrazioni su nastro dopo
l'elaborazione di ogni blocco, con vantaggio tanto
piu' notevole quanto piu' varia puo essere la dura
ta dell'elaborazione dei singoli blocchi.
Lo schema logico ed il diagramma a blocchi della fi
gura 2 definiscono l' applicazione di questo secon-
do metodo.
In particolare nella fig. 2 abbiamo indicato con :
J
=
blocco generico introdotto in memoria
n
numero dei blocchi da elaborare
=
numero delle zone di memoria disponibili
i
=
indice della zona di memoria in cui vengono in
trodotti i dati da elaborare
1' =
indice della zona di memoria in elaborazione
=
indice della zona di memoria contenente dati
elaborati
e' = indice della zona di memoria da cui vengono
stratti i dati elaborati
numero delle zone di memoria gia' impegnate
numero delle zone di memoria con dati pronti
per essere estratti.
Evidentemente le zone di memoria coincidono e sono
state indicate con i diversi quattro indici (i, i'
197
e, e') secondo la fase di programma in cui si trova
nO.
Si intende inoltre che le zone di memoria sono di-
sposte circolarmente, cioe' all'ultima zona, i = m,
seguira ancora la prima zona, i = m + 1 = 1
Le richieste di cui precedentemente abbiamo detto, so
no configurate con la domanda ( i ‹ i' ?) cioe'quan
do ci si chiede se la zona che dobbiamo elaborare
sia gia' stata fornita di dati
Le segnalazioni sono invece configurate con il con-
tatore "h" che segnala al 2° programma se vi sono
delle zone con dati elaborati da estrarre ed in se-
guito da rifornire con nuovi dati.
In conclusione, questo metodo implica che il 20 pro
gramma puo' essere avviato una sola volta e che il
1° programma attende, prima di elaborare, che siano
stati introdotti ed estratti i dati nelle dalle zo
ne interessate.
E' pero' possibile che ad un certo punto, il 20 pro
gramma arrivi allo STOP mentre il 1° sta ancora ese
guendo operazioni interne.
In questo caso, terminata l'operazione interna, il
1° programma riavviera' il 20 con l'istruzione $2P*
La caratteristica operativa dell' $2P*, consente di
inserirla nel ciclo principale del 1° programma. Il
governo dell'unita' centrale la leggera' nel
cors(
di ogni ciclo; se la sequenza di 20 programma sara
in corso, non blocchera' lo svolgimento del 10, ma
ne ritardera' di soli 15 periodi di cifra l' esecu-
zione.
In caso contrario, se nel corso del lavoro il 20 pro
gramma avra' raggiunto lo STOP, il salto $2P* ver-
198
ra' eseguito e dara' corso ad una nuova sequenza del
2° programma.
Si puo' notare che il ricorso alla S2P per il secon
do metodo di utilizzazione richiederebbe un disposi
tivo di sicurezza atto a neutralizzare la sua fun-
zione bloccante della sequenza di 1° programma in
cui e' inserita.
199
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
:
carattere di eventualita'
: registro che ricorda l'indirizzo della posizione p8
dell'istruzione
: indirizzo dell'istruzione posta nella sequenza di 20
programma alla quale si deve saltarc
:il registro Im puo' modificare sia l'indirizzo IIII
che il nome del registro Is
: salta se si e' verificata l'eventualita a.
a) L'istruzione posta nel 1° programma comanda l'inizio di una sequenza di 2 pro
gramma.
b) Se e' gia' in corso una sequenza di 2° programma la S2P viene riciclata fino
termine dell'esecuzione del 20 programma; eseguito lo STOP di 2° programma
S2P riavvia il programma stesso
interno
d
Is
IIII
Im
0
Salta al 20 Programma *
S2P*
(010010)
Is
III I
Im 0
15
: carattere di eventualita'
: registro che ricorda l'indirizzo della posizione p8
dell'istruzione
: indirizzo dell'istruzione posta nella sequenza di 20
programma alla guale si deve saltare
: il registro Im puo' modificare sia l'indirizzo IIII
che il nome del registro Is
: salta se si e' verificata l'eventualita' f
a) L'istruzione posta nel 1° programma comanda l'inizio di una sequenza di 2° pro
si amila,
b) Se e' gia' in corso una sequenza di 20 programma la presente istruzione non bloc
ca il programma su cul e posta
200
SUREMA RIASSUNTIYO
Istruzioni di salto al 2 programma
Istruzion1
52P
S2P*
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

CAP. 10° : LA TERZA SEQUENZA DI PROGRAMMA
10.1. Generalita'
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
10.2. Caratteristiche logiche del 30 programma
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
10.3. Fasi di svolgimento del 30 programma
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
10.4. Funzione e logica delle istruzioni s3P,
TOL, STOP
suO,
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
10.5. L'istruzione SP*
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
10.6. L'organizzazione di un 3° programma che preve
de l'uso della istruzione S3P* dovra' pertan-
to essere legata alle seguenti norme.
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
10.7. Esempio di 30 sequenza con uso della sola SP
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
10.8. Esempio di 30 sequenza con uso della SP*
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

CAP. 11° : IL TAVOLO DI COMANDO
11.1. Generalita'
Il tavolo di comando e' l'organo che costituisce un tra-
mite di comunicazione fra l'operatore ed il sistema per
l'elaborazione dei dati. Con esso si puo' seguire lo svol
gersi di tutte le operazioni, ed eventualmente interveni
re in tale svolgimento.
Il quadro di comando e di controllo contiene i tasti di
comando con i quali si puo' agire sulla calcolatrice dal
l'esterno, e batterie di indicatori che indicano lo sta-
to di avanzamento delle elaborazioni oppure localizzano
ed individuano eventuali errori
La funzione specifica dei tasti di comandi e degli indi-
catori luminosi sara' piu' ampliamente trattata nelle pa
gine seguenti.
Al tavolo di comando e' connessa una Telescrivente, che
ha l'ufficio di prelevare il contenuto delle posizioni di
Memoria che si desidera indagare dandone la trascrizione
a stampa su di un foglio di carta.
Si ha cosi' la possibilita' di ottenere per iscritto qual
che risultato intermedio particolarmente interessante
significativo, senza attendere la fine della elaborazio-
ne e la stampa finale nella stampante.
La telescrivente e' in grado di stampare caratteri alfa-
numerici e speciali alla velocita' di 360 caratteri/min.
con 72 caratteri al max per riga. La telescrivente torna
automaticamente a capo all'inizio di ogni istruzione che
segue una stampa oppure quando sia necessario stampare
piu' di 72 caratteri mediante una sola istruzione.
Un perforatore di banda collegato alla telescrivente con
sente di ottenere contemporaneamente alla scrittura
231
perforazione di banda di carta. La telescrivente e' forni
ta anche di una tastiera, che si utilizza ogni qualvolta
si desideri portare dei caratteri in Memoria, impostando-
li direttamente sulla tastiera stessa.
Al tavolo di comando e' pure connesso un lettore di nastro
perforato per mezzo del quale e' possibile introdurre da-
ti direttamente in Memoria. Il lettore e' particolarmente
utile per l'introduzione di programmi da mettere a punto,
eliminando la fase di conversione su nastro magnetico.
Terminata la fase di correzione il programma in via norma
le viene definitivamente registrato su nastro magnetico,
da dove sara successivamente prelevato nera esecuzionE
vera e propria del lavoro.
11.2. Quadro di comando manuale
Il quadro di comando manuale e' composto di una serie
tasti che per comodita' raggruppiamo in 6 zone.
di
-5
W. FOT, STOP. FOT
LASSASSI
6
5. SEPISO
4
F2F3F4
20
MAN. AUTO. SING. CO
(3,
(P8
(P7
(P6) (P5) (PA
BL)
(SGL
2
(VIA
232
Zona 1 : Pulsanti P1 ÷ P8, tastiera e pulsante BL.
(P2
E laboratore, alesseuchparaesstruzion) Impostate di rettamente s61 dia
dro di comando.
Per questo esiste una tastiera di 64 tasti corrispondenti
ratteri usati dalla calcolatrice e otto tasti cosi' segnati
a1
64
ChE
,P1, P2, P3, P4, P5, P6, P7, P8.
Per impostare un'istruzione sul quadro di comando e' sufficiente pre
mere il tasto P8 e quindi premere sulla tastiera gli otto caratteri
relativi all'istruzione stessa.
Il primo carattere impostato viene registrato in ottava posizione
(P8), il secondo in P7 e cosi'
via.
Qualsiasi battuta in tastiera dopo l'ottava (P1) non ha alcun effet-
Se si vuole correggere un'istruzione gia' impostata e' sufficiente pre
mere il tasto P corrispondente alla posizione da modificare e bacce
re in tastiera
1 caratteri sostitutivi.
Il pulsante BL esclude la tastiera. Con l'abbassamento di questo ta-
stC
Si annulla l'efietto di ogni battuta su tastiera.
233
Zona 2 : Tasti VIA, SG, SGL.
(SGL
• Serve ad annullare tutte le condizioni automaticht
relative alla terza sequenza di programma che com.
paiono sul quadro di controllo nella zona 4
(56
• Serve ad annullare tutte le condizioni automatiche
di macchina che appaiono sul quadro
nelle zone 10, 11, 12, 13
controllo
(VIA)
•Premendo il tasto VIA il calcolatore inizialeope.
razioni con le modalita' dipendenti dal posiziona-
mento del tasti della zona 3.
Zona 3 : Tasti MAN, AUTO, SING, CONT, PP.
• Col tasto PP abbassato, premendo il
tasto VIA, si esegue una istruzio•
ne procedendo di cifra per period
di cifra
MAN.AUTO. SING. CONT. P.P.
,Col tasto CONT abbassato, premen-
do il tasto VIA si esegue la pri-
ma istruzione e quindi automatic:
mente tutte le altre fino alla 1]
ne del programma.
• Col tasto SING abbassato, premen-
do il pulsante VIA si esegue .
istruzione alla volta e la calco.
Tatrice si ferma al termine di o.
gn1 istruzione.
• Col tasto AU10 abbassato, premen•
do il tasto VIA si eseguono le 1
struzioni del programma passo pas
so, una per volta, oppure tutto il
programma a seconda che siano ri
spettivamente abbassati 1|
PP, SING, CONT.
tasti
• Col tasto MAN abbassato, premendc
il pulsante VIA si esegue l'istru
zione impostata su quadro di
co.
mando che viene eseguita period
di ciira per periodo di cifra
interamente a seconda che siano ab
bassati i tasti PP o SING
234
Zona 4 : Tasti 1, 2, 3, 4, E1, E2, E3, E4.
E1E2 E3 E4
I selettori "Condizioni esterne" El, E2, E3, E4, se abbassati abili
tano il salto rispettivamente per le istruzioni, sia da console cht
di programma registrato in memoria, SEI, SE2, SE3, SE4.
Per passare dalla posizione "Salta" a quella "Non salta" e' suffi-
ciente premere a fondo i singoli tasti.
I selettori 1, 2, 3, 4 se abbassati permettono il verificarsi delle
condizioni esterne per il tamburo.
Zona 5 : Tasti TAMB, TS, FOT, Lett. Fot, Riav.Fot, StopFot
TAMR TE FOT IETTI FOT QIAY FOLISTOPR
Riporta il fotolettore allo statc
"attivato non avviato'
Abilita il fotolettore al riavvol
gimento del nascro.
Abilita la lettura da fotolettore.
Attiva il fotolettore.
Abilita la telescrivente.
Abilita il tamburo.
235
Zona 6 : Tasti ASE, AE, ASN, AS, PS, SEP, ISOL.
ASE. A.E. ASN. A.S. PS.
SEPISOL
-Permette l'esecuzione dell'istru-
zione MS contemporaneamente alla
elaborazione in corso.
-Arresta l'elaborazione alla fine
del periodo di cifra in cui si e'
verificato un errore.
Arresta l'elaborazione al
termi-
ne dell'istruzione riconosciuta u
guale' a quella impostata da qua
dro di comando.
-Arresta l'elaborazione al termine
di un'istruzione di salto.
-Arresta l'elaborazione al termine
di un'istruzione di salto non ve•
rificato
Arresta l'elaborazione dopo la ri-
levazione di un errore.
-Arresta l'elaborazione al termine
di un'istruzione di salto su erro
re.
I tasti non considerati hanno una funzione variabile a seconda del
le particolari caratteristiche dell'impianto.
236
11.3. Il quadro di controllo
11 quadro di controllo si compone di 13 batterie di indica-
torl luminosi poste superiormente al quadro di comando ma-
nuale.
Ad ogni batteria corrisponde una delle zone sottoindicate
006000606
0@@11500
-a.
ib
12
166666
2
237
Zona 1 : Riquadro di alimentazione
= CORPO CENTR.
~ GENERALE
• ~ UN. NASTRO
~ TAMBURO
~ MOT. IN LINEA
~ ALIM. 48
Interruttore corrente alternata privilegia-
ta del corpo centrale
Interruttore corrente alternata alimentato-
rl.
Interruttore
corrente continua del corpo cen
trale.
Interruttore corrente centro elettronico.
Interruttore corrente del governo unita' na
ASTELO
Interruttore corrente del tamburo.
Interruttore corrente alternata delle unita'
in linea
Interruttore corrente delle unita' in linea.
Zona
In questa zona possono apparire dispositivi diversi
condo le necessita' particolari dell'utente.
se.
238
Zona 3 : Indicatori "Istruzione manuale; permettono il
controllo delle istruzioni impostate manualmente
-Gli indicatori accesi ripor-
tano nel codice di calcolato
i caratteri dell'istruzic
ne impostata.
-L' indicatore acceso segnala
la posizione da P8 a P1 suc
cessiva a quella raggiunta du
rante l'impostazione della i
struzione manuale.
.Zona 4 : Indicatori relativi alla terza sequenza di pro
Indicatori delle unita' atti-
yate.
-Indicatori delle unita'
date.
Indicatori delle unita' in cui
si e' veriiicato un
errore
•Indicatori non utilizzati.
239
(U=
(10
(UD
-Indicatore di unita' fittizia attivata.
•Indicatore di primo ciclo di terzo programma, in ese
cuzione.
-Indicatore di primo ciclo di terzo programma esegui
to.
-Indicatore di unita' disponibile.
Indicatore di unita attivata ed occupata.
-Indicatore non utilizzato.
Zona 5 : Indicatori relativi al tamburo magnetico.
LUNGHEZZ
• Lunghezza dell'informazione in co-
dice calcolatore.
• Numero della pista in codice cal-
colatore.
- Indirizzo, in codice calcolatore
a partire dal quale avviene il tra
sterimento
a camburo.
Indicatore di errore.
Indicatore di elaborazione su tambur
Indicatore di lettura da tamburo.
Indicatore di registrazione su tamburo.
Indicatore di informazione
> 100 caratteri
240
Zona 6 : Indicatori relativi alle unita' a nastro magnetico.
• Indicatore delle unita' in lettu-
Indicatore delle unita' in
strazione.
Indicatore delle unita
volgimento.
•Indicatore delle unita' non
zionanti.
regi
fun-
Numero de1 blocchi operati. in
dice calcolatore.
co
è 5
in corso
in corso
IN in corsc
DUB in corso
a
9000
Ricerca in corso
NAN in corso
NI in corso
KN in corso
IN; in corso
b
possibile un opera
zione di nastro.
L'unita' a nastro inte
ressata e' occupata.
(Ad uso della manuten
zione.
Errore di temporizzazic
ne in lettura.
Errore di disparita 11
Lettura
Errore di disparita' du
rance ricerca su nastro.
, Letturadel carattere di
inizio blocco.
(Ad uso delLa manuten-
zione).
Errore di temporizzazio
ne in registrazione.
Errore di disparita'
registrazione.
Errore in registrazione
Indicatori non utiliz-
zati.
241
Zona 7 : Indicatori relativi alla telescrivente e foto-
lettore.
(та
Telescrivente disponibile per la ricezione di un ca
rattere
E' in corso un'istruzione di telescrivente (CM, MS).
-La telescrivente e' abilitata all'introduzione o al
la scrittura di caratteri.
- Ritorno di carrello a fine operazione.
•E' in corso un ciclo attivo di telescrivente.
Carattere, in codice perforatore, operato da
scrivente o fotolettore.
rep.
Zona 8 : Indicatori della configurazione in codice cal-
colatore dell'istruzione in corso.
_Nome e posizione di memoria T del
registro.
Carattere di funzione.
Wu Ym
P6 ÷ P3
- Stato dell'indirizzatore della memoria
per i dati operati mediante il canale e
sterno.
- Stato dell'indirizzatore della
memorii
per i dati operati mediante il
canale
interno.
- Rappresentano i caratteri in p7 e p8 del
'istruzione
242
Zona 9 : Indicatori dei caratteri in corso di elaborazione
UE AT UA Rm
- Ci fra operanda del moltiplicatore.
Carattere in uscita da unita aritmetica €
logica.
-Carattere in uscita da accumulatore o regi
stri T.
-Carattere in uscita da memoria attraverso il
canale esterno.
-Carattere in uscita da memoria attraverso il
canale interno
-Carattere in entrata nella memoria dispari
-Carattere in entrata nella memoria pari.
Zona 10 : Indicatori delle condizioni della memoria, dell'ac
cumulatore e dei registri T.
Gli indirizzi delle infor
mazioni operate medi ante
istruzioni doppie di memo
ria sono entrambi pari
di spari
Indica l'abilitazione
la conta del registro
(Ad uso della manutenz.
L'indirizzatore del cana.
le interno contiene un 1r
dirizzo parl.
L'indirizzatore del cana-
e esterno contiene un in
dirizzo bari.
S1 opera sulla memoria
Overflow in memoria.
Gli indirizzatori
sOn
entrambi pari o dispari
(Non utilizzato).
L'indirizzatore del ca.
nale interno contiene ui
indirizzo dispari.
T.' indirizzatore del ca.
nale esterno contiene ir
indirizzo dispari.
Si opera sulla
memorla
dispari
243
.Non utilizzato
(Non utilizzato).
Generazione di un bit gAo
gT.
Memoria principale non con
plementata
Carattere in uscita da me
moria complementato
10
Carattere in uscita da
moria complementato
Operando in accumulatore
negativo.
Segno
nel registro del
segno.
Operando in accumulat
Ore
in complemento.
Risultato di una operazio
ne, # 0.
(Non interessante).
Si opera sul registri 1
Operando in accumulato-
re DOSitivo.
, Operando in accumulato-
re negativo.
•Uscita da complementato
re di accumulatore di un
carattere = 0.
• Carattere in uscita d'a
accumulatore complemen•
tato a 9.
E' sommato 1 al caratte
re uscente da accumulat
Si opera su accumulato•
re.
Trasferimento di un sp.
gno da memoria mediante
canale interno
-Moltiplicatore
segnato
-Moltiplicatore ≥ 5
-Contenuto di accumulatc
re. = 0
(Non interessante).
Overflow in un registro
Zona 11 : Indicatori di temporizzazioni
- Indicatori del numero di periodi di
cifre eseguiti.
Indicatori della fase in esecuzione
(2p)(
(P.) (.)
G
-Stop del primo programma.
• (Non interessante).
(Non interessanti).
-E' in esecuzione una sequenza di 3pro
Bramm:
-E' in esecuzione una sequenza di 2°pro
244
Zona 12 : Indicatori di fini ed errori
Fine dell'esecuzione di un
istruzione.
Si opera sull'ultimo carat
tere dell'operando di accu
mulatore o registri T
La tine di una operazione
aritmetica viene ricardata
di un periodo di ciira.
~ terminata la ricerca di
un carattere.
I caratteri precedentemen-
te confrontati sono risul.
tati diversi.
1 dati confrontati risulta
no di segno opposto.
(C*
(Cs
Indica la fine di ogni pro
/ dotto elementare.
Si opera sull'ultimo carat
/tere dell' operando di memo
ria
-Si opera sull'ultimo carat
tere del moltiplicatore.
-E' operata una parola cor
fine speciale
La memoria e' risultata mi
nore, nell'ultimo confror
to.
(Non utilizzato).
Errore di disparita' in en
trata memoria attraverso ca
nale interno.
Errore di disparita' in u-
scita memoria attraverso ca
nale interno.
Errore in uscita da unita'
aritmetica e logica
Errore di frequenza nel tam
buro.
Errore in unita in inea.
(Non utilizzato).
ERROR
Errore di disparita' in en-
trata memoria attraverso il
canale esterno.
Errore di disparita' in u-
scita da accumulatore o re
gistri T
-Errore segnalato dal gover
no unita' a nastro.
-Errore in entrata da foto-
ettore.
(Non utilizzato).
• (Non utilizzato).
Zona 13 : Indicatori relativi a condizioni varie
(Non utilizzato).
'istruzione in esecuzione
diversa da quella impo-
stata da guadro di comandc
Si e' veriticata a conda
zione di un'istruzione
salto.
m bloccato il primo pro
gramma.
E' bloccato il terzo pro-
slamina.
E' terminata l'istruzione
bloccante del secondo pro
&- dillilla.
Non interessante)
•L unita' a nastro interes-
'sata e' occupata.
Indicatore di passaggio tra
un periodo di cifra e l'al
tro.
-E' bloccato il secondo pro
gramma
• Non interessante
E' terminata l' istruzione
bloccante del terzo progran
ma.
245
