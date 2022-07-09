```{sectnum}
---
start: 3
---
```

# Caratteristiche logiche del governo delle unita' a nastro magnetico e delle altre unita' di introduzione e estrazione


## Caratteristiche generali

Il governo dell' unita' a nastro magnetico e' parte costitutiva del sistema
Elea 9003. Abbiamo gia' definito il nastro magnetico come il supporto piu'
congeniale all' elaboratore elettronico; le unita' relative e il loro governo
consentono rispettivamente la sua utilizzazione e il collegamento tra questi e
l'unita' centrale.

Alla parte centrale dell' elaboratore e' necessario accedere dall'esterno sia
per fare affluire i dati e il programma relativo, sia per estrarre i risultati
del conseguente ciclo di elaborazione. Queste due funzioni d'introduzione dei
dati e d'estrazione dei risultati, sono affidate alle unita' a nastro magnetico
che possiamo quindi definire "unita' d'introduzione" e "unita' di estrazione"
del sistema. Esse costituiscono la parte periferica che completa la struttura
dell' elaboratore Elea 9003.

La principale caratteristica di queste unita' e' di poter essere collegate alla
parte centrale del sistema sia direttamente come unita' in linea, sia
indirettamente come unita' fuori linea.

In quest'ultimo caso esse restano staccate fisicamente e logicamente dall'
unita' centrale e hanno lo scopo di trasferire i dati da nastro perforato o da
scheda perforata, a nastro magnetico eseguendo l'opportuna conversione di
linguaggio.

Funzione di questi convertitori e' anche quella di eseguire l'operazione
inversa da quella ora descritta di portare cioe' i dati da nastro magnetico a
scheda o nastro perforato, e a stampa.


## Governo unita' a nastro magnetico (GUN)

Fino a 20 unita' a nastro magnetico possono essere collegate ad un apposito
governo (che costituisce il tramite fra esse e il calcolatore), le cui funzioni
sono molteplici ed importanti. Il governo delle unita' a nastro, interamente
transistorizzato, assicura e controlla il trasferimento delle in formazioni dai
nastri magnetici alla memoria principale, e viceversa. Questo trasferimento
puo' avvenire consecutivamente oppure selettivamente, interessare una o piu'
unita' a nastro.

Le operazioni di lettura e di registrazione su nastro magnetico oltre che
simultaneamente, possono essere eseguite infatti in modo selettivo, nel senso
che e' possibile registrare di seguito sul nastro il contenuto di zone di
memoria non contigue e contemporaneamente suddividere le informazioni in
entrata nelle zone di memoria piu' adatte all'elaborazione.

Il governo delle unita' a nastro puo' anche ordinare e controllare la
trascrizione delle informazioni da una unita' a nastro, in lettura, ad un'altra
unita' in registrazione: e cio' per un numero prefissato di informazioni, o
fino a quando non viene trascritta una informazione determinata.

E' possibile inoltre la ricerca di una particolare informazione registrata su
nastro magnetico.  Detta operazione puo' avvenire contemporaneamente alla
trascrizione del nastro su un altro nastro con evidente vantaggio, quindi,
nelle operazioni di aggiornamento di un archivio, specialmente quando sia basso
il rapporto tra variazione e contenuto .dell'archivio stesso. Oltre a cio', il
governo delle unita' a nastro puo' ordinare il riavvolgimento contemporaneo di
una bobina in un senso o nell'altro per una determinata lunghezza, ecc.

LE CONFIGURAZIONI DEI CARATTERI SU NASTRO MAGNETICO E SU NASTRO PERFORATO
TEMPORIZZ.

La lettura viene controllata per mezzo della verifica di disparita'; la
registrazione invece viene verificata rileggendo attraverso la testina di
lettura cio' che e' stato appena registrato attraverso la testina di
registrazione, ed eseguendo quindi il confronto.

Nel caso di disuguaglianza, le registrazione continua, ma l' elaboratore
denuncia l' errore, che viene corretto subito dopo automaticamente.


## Le unita' in linea

Il collegamento di queste unita' con l'unita' centrale e' stato ottenuto
mediante appositi organi le cui funzioni sono di interpretare gli ordini
trasmessi dal governo centrale, di coordinare e sincronizzare le operazioni che
le singole unita' devono eseguire.

Ogni unita' (stampante parallela, lettore o perfora tore di schede, lettore di
nastro perforato) e' quindi dotata di un proprio governo, mentre il
sincronizzatore e' unico per tutte le unita' e fa parte del sistema centrale.


### Sincronizzatore

Il sincronizzatore e' connesso da un lato all'unita' centrale e dall'altro a
tante unita' in linea quante sono previste nella particolare installazione per
un massimo di 10. Esso contiene anche tutta la logica comune al gruppo di
apparecchiature connesse e necessarie allo smistamento di informazioni fra le
varie unita' Esso dispone di 10 bocchettoni di entrata ed uscita numerati da 1
a 10.  Ad uno qualsiasi di questi bocchettoni puo' essere connessa una
qualsiasi unita' meccanica.

Dal momento in cui essa e connessa ad un certo bocchettone, il numero di ordine
di questo diviene l'indirizzo dell' unita' suddetta e con questo indirizzo il
programmatore da' qualsiasi indicazione che la riguardi.

Data l'assenza di ogni differenziazione per i bocchettoni, e' possibile
collegare ad essi qualunque tipo di unita' entro il limite di 10: come ad
esempio 10 stampanti oppure 10 perforatrici, oppure 10 lettori di schede oppure
10 lettori di banda.

Naturalmente nell'uso normale sono collegate simultaneamente unita' di tipo
diverso.


### Lettore di schede

Il lettore di schede puo' leggere schede a 80 colonne, con qualsiasi tipo di
codice di perforazione, alla velocita' di 500 schede al minuto: e dotato di due
caselle di alimentazione e quattro caselle di ricezione.

La scheda si presenta sotto forma di cartoncino indeformabile, reso
elettricamente isolante con opportuno trattamento, ed avente forma
rettangolare.

Essa puo' essere perforata in diverse posizioni, disposte in 12 linee a 80
colonne. Su ognuna di queste 80 colonne si puo' rappresentare un dato numerico
mediante una perforazione posta in una determinata posizione, a seconda della
cifra che si vuol rappresentare ; e' pure possibile la rappresentazione di un
carattere alfabetico mediante due perforazioni nella stessa colonna, secondo
particolari codificazioni.

La lettura delle schede e' eseguita da una apparecchia tura fornita di due
spazzole a 80 posizioni; la prima spazzola e utilizzata per la lettura vera e
propria.  la seconda per la verifica dell' esatta lettura.

Con una sola istruzione di programma si specifica l'unita interessata, si
ordina la lettura di una scheda; la registrazione delle informazioni nella
memoria di transito e il trasferimento delle informazioni stesse dal la memoria
di transito alla memoria principale, nelle posizioni specificate
dall'istruzione. Tutte queste o perazioni sono rigorosamente controllate.


### Perforatore di schede

Il perforatore di schede puo' perforare schede ad 80 colonne, alla velocita' di
150 schede al minuto: e' dotato di una casella di alimentazione, di due caselle
di ricezione e di una stazione di lettura a valle della stazione di
perforazione.

L' esatta perforazione e' verificata rileggendo le schede, dopo che la
perforazione e' stata eseguita, per mezzo di una stazione di lettura a 80
posizioni


### Stampante in linea

E' collegata all' unita' centrale e serve astampare ad alta velocita' le
informazioni elaborate provenienti dalla memoria principale. Le modalita' di
stampa possono essere determinate sia dall' unita' centrale, sia dal governo
proprio della stampante.

28
IL FOTOLETTORE

L'operazione di stampa non ostacola il processo di elaborazione.

Il blocco di stampa si compone di 102 ruote di stampa capace ciascuna di
stampare 36 caratteri alfanumerici.

La velocita' e' di 300 righe al minuto. La memoria di transito contiene 104
caratteri alfanumerici prelevati dalla memoria principale.

Prima di essere utilizzate per la stampa, tutte le informazioni vengono
controllate e, qualora si rilevi un errore, questo viene posto in evidenza
mediante la stampa di un carattere convenzionale ai margini del foglio.

Tutte le unita' in linea possono essere dotate di pannelli di connessione.


### Fotolettore

Questo organo permette di registrare direttamente nella memoria principale del
calcolatore le informazioni contenute su banda perforata, alla velocita' di 800
caratteri al secondo. Ad esso si ricorre normalmente per introdurre programmi
da mettere a punto, ma puo' essere utilizzato vantaggiosamente per
l'introduzione di piccole quantita' di informazioni.

La forma rettangolare dei fori di perforazione (1,65x 2,05 mm) consente il
raggiungimento delle piu' alte velocita' agli apparecchi di fotolettura.

Infatti a parita' di dimensione assiale (il lato per la sezione rettangolare,
il diametro per la sezione tonda) tra fori di forma diversa, il fascio luminoso
gode nel nostro caso di una maggiore sezione di indagine fotoelettrica.


### Il convertitore da banda o schede perforate a nastro magnetico

Questa unita' non e' collegata al calcolatore; essa trascrive su nastro
magnetico le informazioni contenute su schede o banda perforata, allo scopo di
introdurle nel calcolatore per mezzo delle unita' nastro magnetico, a velocita'
maggiore di quella consentita dai lettori di schede e dal fotolettore in linea.

Consta di due fotolettori, capaci ciascuno di leggere 800 caratteri al secondo,
e di un lettore di schede che legge 700 schede al minuto; il lettore di schede
e' munito di piu' caselle di ricezione, per agevolare l'asportazione delle
schede gia' lette.

Le informazioni sono riportate su nastro magnetico per mezzo di una unita'
anastro collegata; esse vengono automaticamente riorganizzate, se necessario, e
trascritte a blocchi di lunghezza prefissabile fino ad un massimo di 1200
caratteri.

Pure automaticamente vengono registrati sul nastro magnetico, nelle posizioni
opportune, i caratteri di servizio necessari alla sua utilizzazione in fase di
elaborazione; si possono inserire sino a 10 costanti diverse, e togliere o
aggiungere il segno a una parola numerica.

Il controllo della lettura del carattere in uscita da banda o scheda perforata
viene eseguito rileggendo lo stesso carattere per mezzo di due testine
fotoelettriche o di due spazzole di lettura, ed eseguendo quindi un confronto.

30
IL CONVERTITORE DA BANDA PERFORATA A NASTRO MAGNETICO

Il controllo della registrazione su nastro magnetico viene effettuato mediante
il bit di disparita'.


### La stampante fuori linea

Questa unita' non e' collegata al calcolatore; essa stampa, ad una velocita'
variabile da 600 a 1000 righe/minuto, con 120 caratteri/riga, il contenuto dei
nastri magnetici ottenuto sia come risultato di elaborazioni effettuate dal
calcolatore sia per la conversione da schede o da nastro perforato. Riceve i
dati da una unita' a nastro magnetico e provvede alla loro organizzazione per
la stampa mediante un pannello mobile di connessione e un lettore fotoelettrico
di un anello di nastro perforato.  Le informazioni da stampare sono organizzate
su nastro magnetico nel modo consueto e vengono lette e trasferite, un blocco
alla volta, nella memoria di transito che ha la capacita' di 2048 caratteri
alfanumerici.

Da qui vengono prelevate all'istante voluto e inviate alla stampa tramite un
pannello mobile di connessione, che determina sia il tempo sia la destinazione
d'uscita.

L'eccezionale flessibilita' del convertitore da nastro magnetico a stampa
permette di eliminare, durante l' elaborazione nel calcolatore, il tempo
necessario alla organizzazione dei dati per la stampa e di ottenere, dallo
stesso nastro, stampati diversi sia orizzontalmente che verticalmente.

La lettura del nastro, la registrazione nella memoria di transito, la
trans-codificazione, l' avanzamento della carta sono sistematicamente ed
automaticamente controllati sicche' si rende superflua la presenza di un
operatore che sorvegli la stampa.

I caratteri stampabili sono: 10 numerici, 26 alfanumerici, e 20 fra i
principali simboli matematici, commerciali e di interpunzione. Sono ottenibili
fino a 6 copie simultaneamente.

LA MEMORIA DI LAVORO

