# CAP. 3°: CARATTERISTICHE LOGICHE DEL GOVERNO DELLE UNITA' A NASTRO MAGNETICO E DELLE ALTRE UNITA' DI INTRODUZIONE E DI ESTRAZIONE

## 3.0. Caratteristiche generali

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

## 3.1. Governo unita' a nastro magnetico (GUN)

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

## 3.2. Le unita' in linea

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

