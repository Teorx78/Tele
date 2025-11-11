Ogni simbolo rappresenta un solo bit. M=2. SI assume che la regione di decisone corretta sia definita da [[Regioni di Decisione#MD|MD]] 

### Coefficiente di correlazione tra due segnali
$\rho = \frac{<s_1(t), s_2(t)>}{\sqrt{E_1E_2}}$ e indica quanto sono correlati i due segnali, in particolare:
- $\rho = 0$ indica che i segnali sono ortogonali
- $\rho = -1$ indica che i segnali sono antipodali ($s_2(t) = - s_1(t)$)
- $\rho = 1$ indica che i segnali sono perfettamente correlati (identici a meno di una costante)
### Energia media della segnalazione
$E_s = E[E_{s_{a_0}}] = \frac{1}{2}E_{s_1} + \frac{1}{2}E_{s_2}$  : [[Energia di un Segnale|l'energia media al rcevtore]] è il valore atteso della v.a. $a_0$. 
Dato il segnale ricevuto $r(t) = \alpha s_{Tx}(t) + w(t) \Rightarrow E_s = \alpha^2 E_{Tx}$ , con $E_{Tx}$ energia media in trasmissione

### Probabilità d'errore
$P[E]$ = $1-P[C]$, con $P[C]$ la probabilità di decisone corretta per una trasmissione binaria $\{s_1,s_2\}$ e $P[C] = 1 - Q(\frac{d}{2\sigma_w}) \Rightarrow P[E] = Q(\frac{d}{2\sigma_w})$. 
Dove:
- $d$ : [[Ripasso Algebra con i Segnali#Distanza tra vettori|distanza tra i segnali]] della costellazione
- $\sigma_w$ :  [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|varianza]] del rumore

Nella modulazione binaria $P[E]$ è anche detto bit error probability

Questa presenta dei casi particolari:
##### Segnali con la stessa energia
$P[E] = \sqrt{\frac{E_s(1-\rho)}{2\sigma^2_w}}$
##### Segnali Ortogonali
$P[E] = Q(\frac{d}{2\sigma^2_w})$
##### Segnali antipodali
$P[E] = Q(\frac{d}{\sigma^2_w})$

##### BPSK 
Binary phase Shift Keying formato da:
$s_1(t)=
\begin{cases}  
Acos(2\pi f_0t) &t\in[0, T] \\  
0 &altrove
\end{cases}$

$s_1(t)=
\begin{cases}  
-Acos(2\pi f_0t +\pi) &t\in[0, T] \\  
0 &altrove
\end{cases}$

