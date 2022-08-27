```{sectnum}
---
start: 12
---
```

# Le fasi

Come è noto [^1] in ogni operazione di macchina si distiguono sempre due fasi:
una fase preparatoria e una fase esecutiva.

Nella fase preparatoria vengono estratti dalla macchina i caratteri
dell'istruzione che si deve eseguire e si immettono tali caratteri negli
appositi registri di governo.

Nella fase esecutiva si compie l'operazione vera e propria, e si ottengono i
risultati.

La distinzione fra le fasi è affidata a flip-flop, ognuno dei quali determina
una certa fase.


## Fase ALPHA

E' la fase preparatoria normale in cui si legge l'istruzione che la macchina
dovrà eseguire. La fase ALPHA dura 9 p.d.c. (p0 a p8). La lettura dei caratteri
dell'istruzione avviene in p1 ÷ p8. Soltanto nelle operazioni DELTA_I la fase
dura 3 p-pulsi (p0 + p2): sono operazioni in cui si deve trasferire in un
registro I, una costante contenuta nell'istruzione stessa, oppure si deve
confrontare questa costante con il contenuto di un certo registro T.

I segnali ALPHA e !ALPHA sono ottenuti dal flip-flop ALPHA. Esso viene disposto
in ALPHA al primo M9 dopo la chiusura del tasto VIA in console e alla fine
della fase esecutiva BETA_w se in console è chiuso il tasto "Continuo" cioè è
stabilito che dopo l'esecuzione di una istruzione si passi immediatamente alla
successiva.

Il FF o viene riposto in !ALPHA del segnale di sgancio dato dalla console; in
ALPHA, p8; nelle DELTA_I, in ALPHA, p2; ecc.


## Fase ALPHA ritardata (ALPHA_r)

La fase ALPHA_R comincia 4 µsec dopo l'inizio della fase ALPHA (questa comincia
all'M9, ALPHA_r all'M4) e termina 4 µsec dopo la fine di ALPHA.

I segnali ALPHA_r sono dati dal FF ALPHA_r. Questo viene disposto da ALPHA
all'M3, e riposto da !ALPHA ancora all'M3.


## Fase ALPHA_2

La fase ALPHA_2 è la fase preparatoria delle istruzioni del secondo programma.
I segnali ALPHA_2 e !ALPHA_2 sono dati dal FF ALPHA_2. Questo e riposto con un
segnale di sgancio da console o all'M7 di BETA_w, p0. Viene invece disposto da
tutte le condizioni che dispongono la fase quando la macchina elabora due
programmi contemporaneamente e sono verificate le condizioni che rendono
possibile la lettura di una istruzione del 2° programma.


## Fase BETA_w

E' la principale fase esecutiva dal programma interno.  I segnali BETA_w e
!BETA_w sono dati dal flip-flop BETA_w.

Questo flip-flop viene disposto, all'M9, da tutte le condizioni che ripongono
il FF ALPHA, a meno che non si abbia una istruzione di moltiplicazione.

In questo caso (BETA_w viene disposto all'M9, p2 della fase RHO (v. 12.7.).

Il FF BETA_w viene riposto dal segnale di sgancio da console all'M9 se è
presente il segnale di fine operazione; nelle moltiplicazioni all'9 se c'è
segnale di fine prodotto parziale.


## Fase BETA ritardata (BETA_r)

BETA_r si trova, rispetto a BETA_w nella stessa relazione in cui si trova
ALPHA_r rispetto ad ALPHA. Vale perciò quanto si è detto a proposito di
ALPHA_r.


## Fase BETA_y

E' la principale fase esecutiva delle istruzioni che impegnano il canale
esterno.

Come al solito, i segnali BETA_y e !BETA_y sono dati dal flip-flop BETA_y.
Questo flip-flop viene disposto per esempio all'M7 se sono presenti ALPHA_2,
BETA_w, !Ne (che indica che il canale esterno è libero e può quindi essere
impegnato per l'esecuzione dell'istruzione) e DELTA_BETA_y (che è presente per
esempio nelle istruzioni di preparazione uscita memoria o di preparazione
ingressi nastri, o di trasferimenti da memoria a memoria ecc.).

Il FF BETA_y viene riposto dal segnale di sgancio da console; all'M10 nelle
operazioni da memoria a memoria se c'è segnale di fine operazione; nelle
operazioni da tamburo e da nastro quando compare il segnale di fine operazione,
rispettivamente dal GUT, e dal GUN.


## Fase RHO

E' una fase caratteristica della moltiplicazione: in essa si opera soltanto il
trasferimento da registri T a Rm di una cifra del moltiplicatore; ad essa segue
perció immediatamente una fase BETA_w di esecuzione (v. moltiplicazione).

La fase RHO è stabilita dal flip-flop RHO.

Tale FF viene disposto all'M9 di ALPHA, p8 nella moltiplicazione; al primo M9
dopo la comparsa del segnale di fine prodotto parziale. Viene riposto all'M9 di
RHO, p2, o dal segnale di sgancio da console.


## Fase TAU

Lo scambio dei caratteri fra U.C. e telescrivente avviene nella fase t, che
dura 4 p.d.c. (pO + p3).

La telescrivente può operare isolatamente e allora per tutto il tempo richiesto
dalla stampa rimane inattiva (v. 8.7.2.) oppure può operare contemporaneamente
allo svolgimento di un programma di macchina. Occorre ricordare che la
telescrivente impegna il canale interno.

I segnali TAU e !TAU sono forniti dal FF TAU.  Quando la telescrivente opera
isolatamente lo scambio dei caratteri (fase TAU) si ha non appena sono presenti
i segnali indicanti che la telescrivente è impegnata ed è pronta a ricevere i
caratteri.

Quando la telescrivente opera contemporaneamente allo avolgimento di un
programma di macchina, la fase TAU può iniziare quando si ha un segnale di fine
operazione (riguardante l'altro programma) e sono presenti i segnali indicanti
che la telescrivente è stata impegnata e e' pronta a ricevere i caratteri.


## Fase MU

E' la fase caratteristica della NDN.

Con questa istruzione si registra dalla memoria alla unita a nastro Ns e
simultaneamente si legge dalla unità Nl, verso la memoria. Ciascun carattere
letto su nastro va ad occupare la posizione di memoria da cui si è prelevato il
corrispondente carattere da registrare.

Le informazioni vengono lette e registrate a gruppi di caratteri compresi tra
speciali caratteri (THETA) intercalati nel blocco. Ogni gruppo, in genere,
corrisponde al contenuto di una scheda meccanografica. In corrispondenza aa
ogni carattere THETA e possibile cambiare la zona di memoria interessata
nell'istruzione. Questo cambiamento di indirizzo avviene nella fase MU. In ogni
fase MU si prepara l'indirizzo che si dovrà selezionare in memoria al prossimo
THETA.

Le operazioni che avvengono durante la fase interessano il canale interno
mentre la istruzione NIN interessa il canale esterno.

Si ha come al solito un flip-flop che dà i segnali MU e !MU. Esso viene
disposto all'M9 di BETA_w, pO nella NDN: all'M9 nella stessa istruzione se è
presente il segnale I_THETA indicante che sul canale esterno di memoria sta
uscendo il carattere THETA.

Il FF MU viene poi riposto dal segnale di fine generale dell'operazione; dal
segnale di sganoio da console; all'M9 di p6 se è presente il segnale I_THETA.
Per quello che riguarda la fase MU si veda anche il manuale GUN.


## Fase ETA

Questa fase caratterizza i trasferimenti di indirizzo da W ad un registro T
prescelto nella fase ALPHA. Il trasferimento avviene attraverso l'U.A.D., i
caratteri pervengono agli staticizzatori di uscita memoria e da qui sono
trasferiti ai T. Si passa attraverso l'U.A.D. per poter effettuare la modifica
dei caratteri provenienti dai T nella ITT.

I segnali ETA e !ETA vengono ottenuti dal flip-flop ETA. Questo FF viene
disposto all'M2, in ALPHA, p8 nell'istruzione ITT in cui ai sottrae il
contenuto delle prime 4 posizioni di un registro T da una costante lasciando
invariata la 5° cella di T (ETA viene riposto infatti in ETA, p4); nel le
istruzioni di ricerca in fase BETA, appena ii confronto ha dato esito positivo
(in queste istruzioni l'indirizzo cercato viene trasferito nei registri T);
nelle istruzioni di salto con condizione verificata in BETA, p0 poichè in
queste è necessario trasferire in un T prestabilito l'attuale indirizzo di W,
che è quello dell'istruzione da cui si salta.

Il flip-flop ETA viene riposto dal segnale di sgancio da console, e in ETA, p4,
M9.


##  Flip-flop per particolari operazioni


### Flip-flop p0

E' il flip-flop che dà il periodo di cifra 0. p0 è ottenuto da un FF poichè la
sua durata può essere anche diversa da quella normale dei p-pulsi (10 ps). pO
si potrebbe anche considerare una fase. Si veda guanto detto a proposito del
decodificatore dei p-pulsi, pag. 111.



### Flip-flop ALPHA_37

Questo flip-flop, quando è disposto dà un segnale che dura da ALPHA, P3 ad
ALPHA, p7 (compresi).

Questo segnale serve per esempio nella rete logica del trigger di conta KV. Si
risparmiano alcuni AND e OR in varie reti logiche.

Si ha infatti:

    ALPHA_37 = ALPHA * p3 + ALPHA * p4 + ALPHA * p5 + ALPHA * p6 + ALHA * p7

Il flip-flop ALPHA_37 viene disposto in ALPHA, p2, M9 e riposto in pO, M9 o in
p7, M9 o dal segnale di sgancio da console.


[^1]: Vedi Manuale propedeutico E.8.

