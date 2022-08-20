```{sectnum}
---
start: 9
---
```

# Organi di funzione

## Registro di funzione F

Il primo carattere uscente da Memoria durante la preparazione di una
istruzione è il carattere F, che stabilisce il tipo di operazione che la
macchina deve eseguire.

Questo carattere deve essere presente per tutta la durata dell'istruzione e
viene perciò immagazzinato nel registro di funzione F, costituito da 6
flip-flop.

Esso viene azzerato soltanto all'inizio dell'istruzione successiva.

Le uscite del registro F vanno direttamente al decodificatore di funzione.


## Decodificatore di funzione


### Decodificati parziali

I sei bit contenuti nel registro E possono dar luogo a 64 combinazioni
diverse.

L'individuazione di queste 64 combinazioni avviene in due stadi successivi. Il
decodificatore di funzione produce un certo numero di segnali (detti
decodificati parziali) ognuno dei quali caratterizza una certa classe di
funzioni.

Questi decodificati vengono poi combinati fra loro nelle reti che generano i
comandi dei singoli organi, in modo che ciascun comando sia attivato solo per
l'istruzione (o le istruzioni) desiderata.

I decodificati parziali possono essere raggruppati nelle due seguenti classi,
a seconda di come sono stati generati:

1. decodificati primari, ottenuti direttamente da coppie di bit del registro
   F;

2. decodificati secondari, ottenuti da combinazione dei decodificati primari
   (eccezionalmente da bit dal reg. F).


### Decodificati primari

I decodificati primari sono 12 e sono ottenuti con le
seguenti equazioni logiche:

    DELTA_S = !f * !e       DELTA_P = !d *  a       DELTA_SIGMA =  c *  b
    DELTA_A = !f *  e       DELTA_M =  d *  a       DELTA_X     =  c * !b
    DELTA_T =  f * !e       DELTA_R = !d * !a       DELTA_U     = !c * !b
    DELTA_V =  f *  e       DELTA_B =  d * !a       DELTA_E     = !c *  b

Ogni istruzione è individuata da tre decodificati primari (uno per ciascuno dei
tre gruppi sopraesposti), secondo le seguenti quattro tabelle:


**Istruzioni DELTA_A**

|             | DELTA_M | DELTA_P | DELTA_R | DELTA_B |
| ----------- | ------- | ------- | ------- | ------- |
| DELTA_U     | MA      | DA      | MS      | CMA     |
| DELTA_E     | AM      | AoM     | FAM     | CM      |
| DELTA_SIGMA | -MA     | +MA     |         | +AM     |
| DELTA_X     | -X      | +X      |         |         |


**Istruzioni DELTA_T**

|             | DELTA_M | DELTA_P | DELTA_R | DELTA_B |
| ----------- | ------- | ------- | ------- | ------- |
| DELTA_U     | MT      |         |         | CMT     |
| DELTA_E     | TM      | ToM     | FTM     |         |
| DELTA_SIGMA | -MT     | +MT     |         | +TM     |
| DELTA_X     | XLN     | XLD     | +LD     |         |


**Istruzioni DELTA_S**

|             | DELTA_M | DELTA_P | DELTA_R | DELTA_B |
| ----------- | ------- | ------- | ------- | ------- |
| DELTA_U     | Y       | MEM     | SALTI   | CIT     |
| DELTA_E     | RIi     | RIa     | SIN     | CMM     |
| DELTA_SIGMA | -MM     | +MM     | ITT     | PUM     |
| DELTA_X     | AV      | +IT     | -IT     | IT      |


**Istruzioni DELTA_V**

|             | DELTA_M | DELTA_P | DELTA_R | DELTA_B |
| ----------- | ------- | ------- | ------- | ------- |
| DELTA_U     | PRN     | TOL     | NAN     | DUB     |
| DELTA_E     | ZN      | LNi     | LNa     | TN      |
| DELTA_SIGMA | PLP     |         | NDN     | PSP     |
| DELTA_X     | EM      |         | RN      |         |


Come si vede, il decodificato DELTA_A individua prevalentemente istruzioni che
interessano l'Accumulatore; il decodificato DELTA_T individua prevalentemente istruzioni che
interessano la Memoria T; il decodificato DELTA_S individua
istruzioni varie (di unità centrale); il decodificato V
individua infine istruzioni che interessano unità elettromeccaniche esterne (nastri, tamburo, unità in linea).


## Decodificati secondari

I decodificati secondari sono invece i seguenti (è stato omesso il prefisso DELTA nei decodificati primari),

    DELTA_K    = c
    DELTA_N    = !(_SIGMA * _M + _SIGMA * _B) * _V
    DELTA_AER  = _A * _E * _R + _T * + _E * _R
    DELTA_VUR  = _V * _U * _R = DELTA_NN
    DELTA_AEB  = _A * _E * _B
    DELTA_AUR  = _A * _U * _R
    DELTA_RI   = _S * _E *  a
    DELTA_PI   = _V * _X * _B + _S * _SIGMA * _B
    DELTA_SXM  = _S * _X *  _M
    DELTA_I    = _S * _X * !_M + _S * _U * _B
    DELTA_Z    = _S * _R * !c
    DELTA_1AUP = _A * _U * _P
    DELTA_MM   = _S * _SIGMA * _M + _S * _SIGMA * _P + _S * _E * _B + _S * _U * _P

Ogni decodificato secondario individua un gruppo di istruzioni diverse: i
decodificati secondari sono quindi soltanto dei segnali di comodo che
semplificano la logica dei comandi.

Le istruzioni che la macchina può eseguire sono in numero maggiore delle 64
possibilità di individuazione offerte dal carattere di funzione.

Infatti tutta la classe delle istruzioni di salto è individuata dalla cifra zero (000000) immessa in F (decodificato parziale secondario 2): le diverse istruzioni sono poi caratterizzate dalla condizione sotto cui
eseguire il salto, condizione che è rappresentata dal
carattere uscente da memoria nel p.d.c. 8 della fase di
preparazione[^1].

Questo sistema consente di individuare fino a 64 diverse istruzioni di salto. Ne sono utilizzate soltanto 34.

[^1]: Questo carattere è immesso come sempre in LD, che comunica con il
      verificatore (vedi 16.1.).

