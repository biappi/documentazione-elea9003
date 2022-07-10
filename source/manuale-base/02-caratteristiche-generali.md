```{sectnum}
---
start: 2
---
```
# Caratteristiche logiche dell'unita' centrale


## Caratteristiche generali

L'unita' centrale del sistema Elea 9003, intesa come insieme di organi interni,
ha il compito di ricevere le informazioni dalle unita' di introduzione, di
elaborarle e di predisporle per le unita di estrazione: in pratica ha la
funzione di dirigere il flusso delle informazioni secondo le richieste
dell'utilizzatore.

E' quindi l'unita' centrale che riceve gli ordini dal l'esterno, cioe' a dire
il programma, che lo fa eseguire impegnando via via tutti gli elementi
richiesti

Gli organi che consentono all' unita centrale di ese guire questi compiti sono:

 - l' unita' di governo
 - la memoria di lavoro
 - l' accumulatore
 - l' unita aritmetica e logica
 - il tavolo di comando


## Il programma

La successione delle operazioni da eseguirsi dall'ela boratore e' determinata
dal "programma" registrato nel la memoria di lavoro: questo e' formato da una
serie di parole di otto caratteri, chiamate istruzioni.

Il programma, e' svolto eseguendo successivamente le istruzioni partendo da
quella indicata all'avvio sul tavolo di comando; speciali registri di indirizzo
i- struzionin contengono l'indirizzo dell'istruzione in corso e avanzano
automaticamente non appena questa sia stata eseguita.

Questo modo di procedere sequenzialmente puo' essere variato mediante apposite
istruzioni, dette istruzioni di salto, che permettono di alterare la normale se
quenza sia sistematicamente, sia in funzione di even ti rilevati durante
l'elaborazione, sia a seguito di condizioni impostate sul tavolo di comando.
L'indirizzo dell'ultima istruzione eseguita, prima di passa re ad un' altra
sequenza puo essere ricordato automaticamente e senza perdita di tempo, cosi'
da facilitare il ritorno alla sequenza iniziale.

Il programma puo' essere registrato in una zona qual siasi della memoria
principale : questa puo' infatti contenere indifferentemente in ogni sua
posizione da ti da elaborare, risultati e istruzioni di programma.

E' possibile eseguire parallelamente fino a tre se- quenze di programma. I tre
programmi possono essere iniziati contemporaneamente. ed eseguiti secondo un
sistema di priorita' del tutto automatico; tale prig rita', naturalmente, entra
in giuoco solo quando vie ne richiesto simultaneamente l'intervento di uno stes
so organo da parte di due programmi.

In questo modo possono essere eseguite contemporaneamente:

 - una operazione aritmetica o di trasferimento interno,
 - una operazione di stampa per mezzo della stazione di risposta alle
   interrogazioni,
 - una ricerca automatica su nastro magnetico,
 - una o piu' operazioni di riavvolgimento di nastri magnetici,
 - una o piu operazioni di introduzione od estrazione, per mezzo di unita' a
   schede o nastro perforato e di stampatrici parallele collegate

Una tipica utilizzazione dei tre programmi e' la seguente

 - il primo contiene la maggior parte delle istruzioni riguardanti gli organi
   dell' unita' centrale,
 - il secondo contiene le istruzioni riguardanti unita' a nastro e a tamburo
   magnetico,
 - il terzo le istruzioni relative alle unita' a schede perforate e alle
   stampatrici parallele direttamente collegate.

E' interessante notare che il terzo programma fa si che queste unita' di
lettura - stampa - perforazione impegnino in misura minima il calcolatore.

Qualora esse vengano fatte funzionare insieme ad una unita' a nastro magnetico,
consentono la conversione nastro perforato - nastro magnetico, schede
perforate - nastro magnetico e nastro magnetico - stampa.

In tal modo puo' dirsi che l'intero complesso e' grado di funzionare come
convertitore senza che lo svolgimento delle elaborazioni ne venga alterato.


## L'unita' di governo

Cuore dell' elaboratore e' l' unita di governo; essa dirige tutte le
operazioni, comanda l' unita' aritmetica e logica, la memoria principale, l'
introduzione e l'estrazione dal sistema.  I compiti assolti dall' unita' di
governo per eseguire un'operazione sono: il prelevamento in memoria delle
istruzioni da eseguire, la interpretazione di queste istruzioni, l'avvio dei
vari organi dell'elaboratore per svolgere le loro funzioni e il controllo di
quanto e' stato eseguito. Inoltre il governo e' in grado di tenere conto delle
segnalazioni che i vari organi centrali e periferici possono dare per variare
il corso delle operazioni.


## Il flusso delle informazioni

Il collegamento fra le diverse parti componenti l'unita' centrale e assicurato
da due canali di trasferimento, uno dei quali, detto canale interno", serve
fondamentalmente a collegare la memoria principale all'unita' aritmetica e
logica, all' accumulatore e registri T, al governo del calcolatore e
sincronizzatore, mentre l' altro, detto "canale esterno e' utilizzato
normalmente per il collegamento della memoria con le unita' di governo dei
nastri ed eventualmente dei tamburi magnetici.

Ognuno dei due canali e' provvisto di organi per la verifica di disparita', e
di un indirizzatore che consente di ricercare nella memoria principale
l'indirizzo del carattere che deve essere trasferito o registrato.

I due canali possono pertanto lavorare in parallelo, prelevando o registrando
nella memoria principale due caratteri alfanumerici per ogni periodo di cifra.
Questa possibilita' viene normalmente utilizzata per ottenere la contemporanea
esecuzione di operazioni interne di introduzione od estrazione; vi sono pero'
istruzioni che sfruttano il parallelismo dei due canali per sovrapporre
operazioni di lettura e di registrazione, o per trasferire direttamente una
informazione da una zona all' altra della memoria.

La funzione dei due canali e' descritta graficamente nella tabella N. 1 che
mette in evidenza anche i collegamenti dell' accumulatore e registri T e degli
operatori aritmetico e di verifica.

14 GOVERNO GOVERNO UNITÀ A NASTRO u.n.12 з 11 IL FLUSSO DELLE INFORMAZON
Tabella N. 1 15

L' accumulatore e i registri T sono collegati alla memoria principale dal
canale interno, e agli operatori aritmetico e di verifica da un proprio canale,
dota to di verifica di disparita'.

Gli operatori aritmetico e di verifica sono collegati alla memoria principale
dal canale interno, attraverso il quale ricevono il secondo operando quando il
primo si trova nell' accumulatore o nei registri T. Il calcolatore puo'
tuttavia effettuare operazioni su operandi contenuti entrambi in memoria, che
arrivano allora agli operatori aritmetico e logico l'uno attraver so il canale
esterno, l'altro attraverso il canale in terno. Il risultato viene inviato in
memoria dall'operatore aritmetico attraverso il canale interno.


## La memoria di lavoro

Tutte le informazioni in entrata vengono convogliate alla memoria di lavoro. Da
essa sono prelevate le in formazioni in uscita; in essa sono considerati i
risultati intermedi, il programma, le costanti di immediata consultazione, ecc.

La memoria di lavoro, o memoria principale e quindi un punto di passaggio per
tutte le informazioni.

Ciascuna posizione della memoria principale e indirizzabile: cio' significa che
il programmatore ha la possibilita' di indicare su quale informazione vuole
operare, specificandone semplicemente l' ubicazione Si possono indicare tanti
indirizzi diversi quanti so no i caratteri contenuti.

E' bene definire un' altra suddivisione della memoria, utile da un punto di
vista funzionale: i gruppi di caratteri che fanno parte di uno stesso insieme
operativo, e che vengono operati per mezzo di un'unica istruzione, sono
chiamati "parole". Una parola, per esempio, e' un numero decimale composto da
piu cifre e segno, oppure un nome o una data.

16 LA MEMORIA DI LAVORO IN UN ARMADIO ._

L'indirizzo iniziale e la lunghezza sono gli elementi per identificare una
parola: la lunghezza puo'essere espressa mediante un numero di due cifre,
oppure identificata, senza bisogno di speciali istruzioni, da un particolare
carattere di fine parola. Questo e' scelto dal programmatore e puo' coincidere
con il segno algebrico della parola adiacente: in questo caso non vengono
occupate posizioni di memoria per delimitare le parole di lunghezza
sconosciuta. L'Elea 9003 e dunque una macchina a parole di lunghezza variabile
senza limitazioni.


## L' accumulatore e i registri T

L' accumulatore e' una piccola memoria ausiliare a nuclei magnetici, la cui
funzione principale e quella di contenere uno degli operandi e,
successivamente, il risultato di un'operazione aritmetica.

T.s

sua capacita' e' di 100 caratteri alfanumerici piu il segno. In modo analogo
alla memoria di lavoro, si puo' indirizzare la parola a partire da una
qualsiasi delle posizioni dell' accumulatore. Inoltre, grazie alla presenza di
uno speciale "bit in aggiunta a quelli necessari per formare il carattere, puo'
essere segnalata la fine della parola in esso contenuta.

Altra memoria ausiliare a nuclei magnetici e' quella dei registri T: essa ha la
capacita' di 200 caratteri alfanumerici indirizzabili di cinque in cinque
posizioni per un totale di 40 registri. La loro funzione principale e' la
modifica automatica delle i- struzioni. Essi pero possono essere utilizzati per
operazioni aritmetiche su operandi la cui lunghezza non superi 10 caratteri.
Esiste uno speciale "bit" analogo a quello dell' accumulatore, che segnala la
fine della parola contenuta in un registro.

Gli operandi possono essere trasferiti dalla memo ria principale all'
accumulatore e viceversa: dalla memoria principale ai registri modificatori e
vice versa: ma non direttamente dall' accumulatore ai registri e viceversa; il
tempo di trasferimento dipende dalla lunghezza della parola.


## L'unita' aritmetica e logica

L'unita› aritmetica e logica effettua i calcoli aritmetici, i confronti e le
operazioni logiche: mo difica le istruzioni per mezzo dei registri T: puo'
intervenire nei trasferimenti delle informazioni.

Dell' unita' aritmetica e logica fanno parte:
 - l'operatore aritmetico e logico,
 - l'operatore di verifica,
 - il confrontatore.

Le operazioni aritmetiche possono avvenire fra parole dotate o prive di segno:
ogni operazione puo' dunque essere algebrica o fra valori assoluti.  Gli
operandi elaborati dall' unita' aritmetica e 10 gica non necessariamente devono
trovarsi in due memorie diverse (memoria princ.-accumulatore ; memoria
principale - registri) ma possono essere contenuti in zone diverse della
memoria principale, senza interessare l' accumulatore o altri organi, con
conseguente notevole riduzione di tempo e semplificazione dello svolgimento del
programma.

I risultati delle operazioni possono ottenersi nella memoria, nell'
accumulatore o nei registri di modifica.

Questa unita' ci permette di eseguire operazioni secondo 1' algebra di Boole,
consentendoci:

 1. l'utilizzazione singola dei bit 2. l'elaborazione di proposizioni logiche

Nelle operazioni di confronto l' unita' aritmetica e lo gica ricorda se le
parole confrontate sono uguali o diverse e, in questo caso qual' e' la
maggiore; il confronto puo' essere eseguito fra parole numeriche e alfabetiche
e fra parole dotate o prive di segno.

Le caratteristiche di quest' operazione rendono parti colarmente facile
l'ordinamento alfabetico e la selezione di codici o nominativi di
identificazione.


## I controlli

L' esatta esecuzione di tutte le elaborazioni che l'Elea 9003 svolge e'
garantita da un insieme di controlli automatici che individuando qualsiasi
errore non appena questo si verifichi, ne segnalano l'ubicazione nella
macchina.  Il controllo dei dati registrati nella memoria principale e nelle
altre memorie ausiliarie e' garantito dall' esistenza, per ciascun carattere,
di un bit di controllo, la cui funzione e' quella di garantire che ciascun
carattere risulti sempre costituito da un numero dispari di bit . Pertanto il
controllo del le informazioni nella memoria si ottiene verificando la
disparita' del numero di bit in ciascun carattere.

Lo stesso procedimento di controllo e' applicato in tutti i trasferimenti
all'interno dell' elaboratore.

Per l'organo di calcolo i controlli sono effettuati mediante la prova del 3.
Analogamente alla prova del 9 essa consiste nel confrontare il resto della
divisione modulo 3 del risultato dell'operazione, con il resto della divisione
modulo 3 del moltiplicando, moltiplicato per il resto della divisione modulo 3
del moltiplicatore e aumentato del resto della divisione modulo 3 dell'
addendo.

Esempio 19 11 215 1 0 2

Nelle operazioni aritmetiche una ulteriore forma di controllo e' data dalla
verifica della rappresentazione dei caratteri numerici ed alfabetici; in essi
infatti non compaiono mai le configurazioni c, b, a, = 101, oppure b, a, 10


## Il tavolo di comando

Il mezzo di comunicazione fra l'operatore e l'elaboratore e' il tavolo di
comando, che contiene i comandi manuali, il quadro e le linee di controllo.
Per mezzo del tavolo di comando si puo' seguire ed eventualmente intervenire
nello svolgimento di tutte le operazioni. Esso e' costituito dai tasti e dagli
interruttori mediante i quali e' possibile agire sul l' elaboratore dall'
esterno, e dal quadro di controllo che contiene gruppi di indicatori che
permettono di seguire lo stato di avanzamento dell' elaborazione, individuare e
localizzare eventuali anomalie.

20 JUNEWUS IU 00AVL I • 4 0000

Al tavolo di comando e' annessa una stazione di risposta alle interrogazioni
che ha il compito di prelevare il contenuto delle posizioni desiderate della
memoria principale, dandone la trascrizione a stampa; e, qualora lo si
desideri, contemporaneamente alla stampa, in modo del tutto automatico e senza
perdita di tempo, e' possibile ottenere la perforazione su nastro di carta
degli stessi caratteri.

Questa caratteristica risulta particolarmente comoda per la messa a punto dei
programmi. La stampa e' completamente indipendente dall' unita' centrale;
quest'ultima infatti si limita a fornire i caratte ri da stampare e rimane
impegnata solamente per il tempo necessario ai trasferimenti che avvengono al
la normale velocita' di macchina.

21

