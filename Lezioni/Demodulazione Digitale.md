Decidere quale simbolo è stato trasmesso a partire dal segnale ricevuto. Consideriamo il caso:
- no [[Modulazione digitale#Canale trasmissivo|interferenza inter-simbolica]]:
- trasmissione di un solo simbolo (sappiamo l'intervallo ma non sappiamo quale simbolo sia)

$s_{TX}(t) = s_{a_0}(t)$ , con $a_0$ simbolo trasmesso al tempo $0$

A meno del rumore (usando [[Canale AWGN|canale AWGN]]) ricevo le forme d'onda $s_1(t),\dots,s_M(t)$ , dove $\forall$ segnale c'è un solo vettore e viceversa: 
$s_i(t) \leftrightarrow \vec s_m(t)=[s_{m,1},\dots,s_{m,I}]$ ^dae514

### Costellazione associata alla segnalazione
È l'insieme dei vettori $\{\vec s_1,\dots,\vec s_N\}$ che rappresentano i simboli trasmessi dal [[Modulazione digitale|modulatore digitale]]. 

Questi vengono inseriti nel piano euclideo e delimitati dalle [[Regioni di Decisione|regioni di decisione]]. Ognuno di questi poi viene usato come riferimento dal demodulatore per decidere a quale simbolo appartiene il punto ricevuto.

Calcolare ogni vettore $\vec s_i$ bisogna moltiplicare la [[Ripasso Algebra con i Segnali#Norma di un vettore|norma]] di ogni sua componente e il vettore ortonormale: 
$\vec s_i = ||s_i(t)||*\phi_i(t)$ ricordando come viene rappresentato un [[Demodulazione Digitale#^dae514|vettore in questo caso]].

### Rumore dopo la proiezione
$w_i = \int_{-\infty}^{+\infty}w(t)*\phi(t) \, dt$ , ma $w(t) \sim \mathcal N(0, \sigma^2)$ indipendenti per tempi diversi quindi $w_i$ è ancora una gaussiana.

Nel demodulatore calcoliamo $\vec r = [r_1,\dots, r_I] = \vec s_{a_0}+\vec w$

In base alla dimensione abbiamo un piano e rappresentazione diverso del rumore, per esempio con dimensione 1:
![[Costellazione.png]]
La gaussiana indica "quanto spesso" può avvenire il rumore. Il rumore trasla lo spostamento dal segnale ricevuto rispettoa quello trasmesso.

#modulazione