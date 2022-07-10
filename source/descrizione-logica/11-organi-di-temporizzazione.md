```{sectnum}
---
start: 11
---
```

# Organi di temporizzazione

Le operazioni della macchina vengono effettuate in intervalli di tempo fissi o
variabili detti fasi. Nelle fasi si distinguono degli intervalli di tempo fissi
detti periodi di oifra (p.d.c.). In ognuno di questi intervalli la macchina
opera un carattere alfanumerico.

Un p.d.c. dura 10 µs. Si distinguono individualmente 9 p.d.c  pO + p8. Il
p.d.c. pO può durare (nella lettura da fotolettore) qualche ms anziché 10 µs.

Nel p.d.c. occorre poi individuare 1l µs. A ciò provvedono i mastri. Questi
sono impulsi di larghezza 0,5 µs e a fronti molto ripidi.

Si distinguono 10 mastri diversi MO + M10. Ognuno è presente su una propria
linea; su ciascuna linea perciò si ha un mastro ogni 10 µs.

I mastri sono ottenuti da una linea di ritardo in cui viene fatto circolare un
impulso di forma identica a quella dei mastri.


## Linea di ritardo

### Generalità

La linea di ritardo è l'elemento che crea i 10 mastri contenuti in ciascun
periodo di cifra. Essa è del tipo a parametri concentrati (vedi Manuale
propedeutico D).

Fra l'ingresso e l'uscita si ha un ritardo di 10 µs; perciò quando si introduce
nelle linea un mastro, lo si avrà all'uscita dopo 10 µsec.

Nei punti intermedi si possono prelevare altri mastri con ritardi variabili.

Si prelevano i mastri da MO ad M10. Quando la memoria non scambia informazioni
con il tamburo o i nastri, la circolazione del mastro nella l.d.r. è ottenuta
riportando M10 all'ingresso della linea stessa, tramite una porta che è aperta
se è presente il segnale Ie (vedi FF Ie pag. 109).

Quando è in funzione 11 tamburo magnetico, la cui velocità è legata alla
frequenza di rete e quindi non è rigorosamente costante, occorre sincronizzare
con esso la temporizzazione di macchina.

A tale scopo il Governo Tamburo fornisce all'unità centrale due segnali di
sincronismo, in forma di mastri, detti rispettivamente MoT ed M5T. Questi
segnali si ripetono ogni 11 µsec. circa e sono sfasati fra di loro esattamente
di 180°.

I due segnali MoT ed M5T vengono immessi rispettivamente nella prima e nella seconda metà della linea; la temporizzazione di macchina è così asservita al tamburo.

Si noti che i mastri non sono più spaziati uniformemente nel tempo: fra M4 ed
M5 ci sarà (nominalmente) 1,5 µs; e fra MO ed M10 ci sarà 0,5 µsec [^1].

Anche quando è in funzione un nastro magnetico occorre asservire la linea di
ritardo a un segnale da nastro, detto trig N, che si ripete ogni 18 µsec circa.
Il trig N viene immesso all'ingresso della linea, con le due metà collegate
normalmente.


### Flip-flop Cl

Il flip-flop Cl fornisce gli impulsi di ingresso alla prima metà della linea di
ritardo tramite un generatore di mastri. Il segnale di ingresso viene fornito
ogni volta che si attiva il FF Cl.

Il FF Cl viene attivato dal comando SCl, e viene riposto dal segnale di sgancio
da console e all'M8, in presenza di Cl.

Il FF Cl impedisce che entro la linea vengano immessi accidentalmente due
mastri distanti fra loro meno di 8 µsec.


### Flip-flop Te

Questo flip-flop fornisce i segnali alla seconda metà della linea quando c'è
sincronizzazione col tamburo magnetico. Esso funziona per la seconda metà della
linea nello stesso modo in cui Cl funziona per la prima metà.

Esso viene disposto, se sono presenti il segnale di aggancio tamburo e il
segnale indicante che si opera su canale esterno, dal mastro M5T. Viene riposto
dall'M3.

Il segnale T5 va alla seconda metà della linea di ritardo tramite un generatore
di mastri.

### Flip-flop Ie

Questo flip-flop stabilisce se la linea è chiusa su se stessa (Ie) o è invece
aperta (!Ie).

### Flip-flop Va

Questo flip-flop serve a dare inizio alle operazioni in macchina ed è
normalmente riposto. Quando si preme il tasto "VIA" in console esso viene
attivato.

Il segnale che si ottiene viene derivato e mandato a disporre il flip-flop Cl,
a fornire perciò il primo impulso alla linea di ritardo.

## Contatore principale (Cp)

Il contatore principale serve a stabilire il numero dei p.d.c. trascorsi
dall'inizio di ogni fase. Esso è formato da due gruppi di 4 flip-flop ciascuno,
connessi a contatore. Esso può contare avanti da 00 a 99. Arrivato a 99 ritorna
a 00: allora la rete logica != Cp (v. pag. 111) non dà più segnali in uscita,
la conta viene sospesa e la configurazione 00 viene interpretata come 100
[^2]).

La conta si ha in fase ALFA e, esclusa la fase BETA della DELTA_AEB, anche in
tutte le altre fasi di macchina. Essa avviene in M9, p0; in M9 per tutti gli
altri p.d.c., se e' presente I != Cp [^3].

Quando si legge da fotolettore (DELTA_AEB) si opera un carattere ogni 1,25 ms
anzichè ogni 10 µs come avviene normalmente: percio' anche al contatore
principale dovrà essere dato un segnale di conta ogni 1,25 ms. Nella DELTA_AEB
il registro V, che altrimenti rimarrebbe inattivo, viene utilizzato per la
temporizzazione della fase esecutiva di questa istruzione; a questo scopo lo si
fa contare, con una conta ogni 10 µs da 00 a 76 e lo si azzera appena è finito
il carattere. La conta riprende al carattere successivo. Quando V è nella
configurazione 40 si ha la conta di Cp.

Il contatore Cp viene azzerato all'M9 di ogni p.d.c. se
è presente 11 segnale !KZ.

### Il flip-flop KZ

Il FF KZ serve per la cancellazione del contatore principale. Esso viene
riposto in !KZ alla fine delle diverse fasi per esempio con il segnale di
sgancio da console, all'M8 di ALFA, p8, di RO, p2, di MU, p6, ecc.

Infatti finite queste fasi il contatore principale va azzerato e deve
riprendere la conta nella fase successiva dalla posizione 00. KZ viene disposto
in KZ al p0 in fase ALFA, BETA_w, RO, TAU, ecc.


### Rete logica != Cp

Essa indioa che il contenuto del contatore principale è
diverso da 00. In tal caso si ha un segnale in uscita
(I != Cp).

E' costituito da una rete logica che ha la seguente equazione:

    I != Cp = !(!aCpD * !cCpD * !dCpD * !aCpU * !cCpU * !dCpU)


### Decodificatore dei p-pulsi (A p-pulsi)

Il decodificatore dei p-pulsi deve fornire in uscita segnali della durata di un
p.d.c. (10 µs) susseguentesi in un ordine prestabilito. Cio' si ottiene
decodificando le uscite del contatore principale e poichè interessano solo i
p-pulsi da p1 a p8 si decodificano solo le uscite da 01 a 08.

I decodificati sono:

    p1 =  aCpU * !bCpU * !dCpU * DELTA_OD
    p2 =  bCpU * !cCpU * !dCpU * DELTA_OD
    p3 =  bCpU *  cCpU * !dCpU
    p4 = !bCpU *  cCpU * !dCpU
    p5 = !aCpU * !cCpU *  dCpU
    p6 =  aCpU * !bCpU *  dCpU
    p7 =  bCpU * !cCpU *  dCpU
    р8 =  bCpU *  cCpU *  dCpU

Nella fase ALFA il contatore delle decine è certamente zero per cui in questa
fase non occorrerebbe il decodificato dello O decine. In fase BETA basta poter
distinguere solo i primi 3 p-pulsi (pO, p1, p2). La stessa cosa succede per le
altre fasi. Per cui basterà mettere il decodificato delle O decine in and con i
soli decodificati di 1. e 2.

Il decodificato delle O decine è:

    DELTA_OD = !aCpD * !cCpD * !dCpD

Il primo p-pulso di ogni fase, cioè p0, viene generato invece da un apposito
flip-flop (p0).

Tale FF viene disposto in p0 all'M9 se è presente !KZ.

Viene riposto dal segnale di sgancio da console; al primo M9 di ogni fase
escluse le operazioni da fotolettore; in queste ultime all'M9 di ALFA e quando
è terminato il periodo di lettura di ogni cifra.


[^1]: La complicata procedura di sincronizzazione con due mastri serve appunto
      a suddividere in due metà di 0,5 µsec l'una il margine fra p.d.c. di
      tamburo (11 µsec) e p.d.c. di unità centrale (10 µsec)

      Cio' è richiesto dai circuiti di scrittura e lettura sul tamburo.


[^2]: Il contenuto del contatore principale Cp viene confrontato con quello del
      registro di lunghezza RL, nel caso che quest'ultimo contenga caratteri
      numerici. Poiché il massimo contenuto in RL può essere 100 è sufficiente che il
      contatore principale abbia 100 posizioni.


[^3]: In pO occorre dare il trigger di conta per una via diversa dalla normale
      poichè in questo p.d.c. il segnale I != Cp non è presente essendo Cp ancora
      nella posizione 00. Si osservi anzi che quando Cp, dopo 100 conte, riassume la
      configurazione 00 la conta resta sospesa poichè non sono presenti ne I != Cp,
      ne p0.

