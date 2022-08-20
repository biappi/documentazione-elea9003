```{sectnum}
---
start: 10
---
```
`
# Organi di lunghezza operando da memoria

##  Registro di lunghezza RL

E' costituito da due gruppi di sei FF, detti rispettivamente LD ed LU.

### Lunghezza dell'operando da Memoria

La lunghezza dell'operando da memoria nelle operazioni
fra Memoria ed Accumulatore è indicata con idue caratteri
uscenti da Memoria nei p.d.c. 7 ed 8 della preparazione; questi caratteri sono immessi in RL.
Possono darsi due casi:

1. I caratteri sono numerici: durante la fase esecuti
va il contenuto di du viene alora conirontato ad
ogni p.d.c. con il contenuto del contatore principale [^1], per mezzo del comparatore di lunghezza Cl [^2]. La coincidenza dei due contenuti genera un segnale di fine dell'operando di memoria.

2. I caratteri sono alfabetici: si distinguono allora
due sottocasi, a seconda che in LD venga immesso uno dei
caratteri Q, P ovvero Z, Y.

Nel primo sottocaso (Q, P) durante la fase esecutiva il contenuto del solo LD viene confrontato (mediante il comparatore di ricerca) [^3] ad ogni p.d.c.
con il carattere uscente da Memoria: l'operando da
Memoria si considera terminato quando esce da Memoria un carattere uguale a quello immesso in LD (detto carattere chiave).

Il secondo sottocaso (2, Y), riguarda esclusivamente operandi numerici: il contenuto di LD non interessa e l'operando è considerato terminato non appena da Memoria emerge un carattere alfabetico qualsiasi, ovvero un segno.

Nelle operazioni su Memoria T la lunghezza dell'operando non puo superare 10: la si indica allora con
una sola cifra decimale (quella che esce da Memoria
nell'ultimo p.d.c. della preparazione), che viene
immessa in IU. La lunghezza 10 è indicata (per convenzione) dalla cifra 0. Il carattere uscente da Memoria nel penultimo pdc. delia preparazione (p7)
non va in questo caso in LU, ma in V dato che rappresenta l'indirizzo del reg. T su cui operare.

Nelle istruzioni di salto non esiste operando da Memoria: il carattere uscente da Memoria nel p.d.c. 7
della preparazione è l'indirizzo del registro T in
cui immagazzinare l'indirizzo raggiunto nel programma da cui si è saltato, e viene pertanto immesso in
IU (che resta inutilizzato). Il registro LD riceve
invece normalmente l'ultimo carattere dell'istruzione, che però indica (anzichè una lunghezza) la condizione sotto cui eseguire il salto.

Il registro LD serve quindi come registro di condizione nelle istruzioni di salto.

### Ingreasi al registro di lunghezza

Prima di introdurre informazioni in RL occorre azzerario,
col comando RL.

Si hanno due canali di ingresso, uno proveniente dalla
U.A.D. (e quindi dalla memoria), e uno proveniente dal
contatore principale.


1.  L'ingresso sul registro LD dalla unità aritmetica
si ha dall'M8 al M9 del p.d.c. 8 della fase o se non
ci sono operazioni DELTA_T.

L'ingresso in IU si ha se è presente il segnale XLC
cioè dall'M8 all'M9 del p.d.c. 7 della fase ALFA se non
ci sono operazioni DELTA_T oppure dall'M8 all'M9 del
p.d.c. 8 della fase O se ci sono operazioni DELTA_T [^4].

2. L'ingresso da contatore principale Cp è condiziona
to alla presenza del segnale XLB. Questo è presente
in fase BETA_W e alla fine della parola contenuta in accumulatore o in Mem T, nelle istruzioni FAM, FTM cioè
quando si vuol trasferire in memoria la lunghezza
della parola contenuta in accumulatore o in Mem T.

### Uscite dal registro di lunghezza

I segnali di uscita dai registri LU, LD vanno direttamente e continuamente al comparatore di ricerca e
al comparatore di lunghezza. Su comando di XLD, le uscite di RL possono andare invece alla memoria.

Le uscite di LD vanno direttamente anche al verificatore di condizione [^5].

## Comparatore di lunghezza (CI)

Il comparatore di lunghezza confronta le uscite del contatore principale con il contenuto del registro di lunghezza, dando un'indicazione in uscita nel caso di ugua
glianza.

Poichè si confrontano caratteri numerici, da ciascuno
dei due registri LD ed LU arrivano solo i quattro canali che si riferiscono ai bits a, b, c, d.

Nelle istruzioni tipo DELTA_T si ha a disposizione una sola
cifra per indicare la lunghezza [^6]. Questa cifra (l'ultima uscente da Memoria durante la preparazione) viene
immessa in LU. La lunghezza 10 (la massima su cui si può
operare nelle DELTA_T) è indicata dalla cifra 0 scritta in
LU. Nelle DELTA_T si limita quindi la comparazione alla sola
cifra delle unità.

La struttura logica del comparatore è impostata sulla
ricerca delle condizioni di disuguaglianza fra gli ingressi: l'uscita di uguaglianza si ottiene poi come negata della disuguaglianza. Cio` semplifica i circuiti di
confronto. Si scriverà perciò questa equazione di disuguaglianza.

    (Cp != L) = aCpU * !aLU + !aCpU * aLU + bCpU * !bLU + !bCpU * bLU +
                cCpU * !cLU + !cCpU * cLU + dCpU * !dLU + !dCpU * dLU +
                (aCpD * !aLD + !aCpD * aLD + bCpD * !bLD + !bCpD * bLD +
                cCpD * !cLD + !cCpD.cLD + dCpD * !dLD + !dCpD * dLD) * !DELTA_T

    (Cp = L) = !(Cp != L)

L'uscita di Cl è abilitata solamente in BETA_w poichè è interessante nella sola fase di esecuzione.

Poiché si potrebbe aver indicazione di uguaglianza al
p.d.c. 0 della fase BETA_w (quando Cp = 0) se in L è contenuto 100, l'uscita di Cl è condizionata alla presenza
del segnale !p0.

Inoltre essa è inibita nelle DELTA_RI e quando si ha in LU
uno dei caratteri P, Q, Y, Z.


### Comparatore di ricerca (Cr)

Il comparatore di ricerca confronta le uscite del registro di lunghezza con il contenuto di memoria. Esso
viene utilizzato soltanto in quei casi in cui un carattere chiave è staticizzato nel registro LD.

Quando dalla memoria esce il carattere chiave, da Cr
esce un segnale (I PHI I) il quale avverte che tutti i caratteri da memoria sono stati operati. Il carattere chiave
non viene operato.

I segnali che escono da LD, LU vanno direttamente e continuamente a Cr e quindi il confronto viene sempre fatto. Il risultato di tale confronto non viene prelevato
nella DELTA_АЕВ (1 'istruzione CM).

Anche la logica del comparatore di ricerca è impostata
sulla ricerca della disuguaglianza: l'uscita di uguaglianza è ottenuta come la negata della disuguaglianza.

Si ha la seguente equazione logica:

    IUCr!= = aMI * !aLD * aLU + !aMI * aLD * aLU + bMI * !bLD * bLU + !bMI * bLD * bLU +
             cMI * !cLD * cLU + !cMI * cLD * cLU + dMI * !dLD * dLU + !dMI * dLD * dLU +
             eMI * !eLD * eLU + !eMI * elD * eLU + fMI * !fLD * fLU + !fMI * fLD * fLU

    IUCr =  !IUCr!=

Il confronto come si vede, è condizionato alla presenza
dei bit del registro delle unità.

Esso avverrà solo per i bit UNO del carattere contenuto
in LU, che, come si ricorderà, è P, o Q, o I, o Z.


[^1]: Vedi 11.2. pag.  109

[^2]: Vedi 10.2. pag.  103

[^3]: Vedi 10.3. pag.  104

[^4]: Il registro di lunghezza viene azzerato col comando RL in ALPHA, p1, M7 nelle operazioni in cui sarà
attivo l'ingresso dall'U.A.D., in M7, nelle opera
zioni in cui sarà attivo l'ingresso dal contatore
principale.

[^5]: Vedi 16.1

[^6]: La struttura delle istruzioni DELTA_T è infatti la seguente: `L Tb IIII Ta F`

