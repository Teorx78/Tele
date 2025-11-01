Un segnale è una qualsiasi funzione del tempo $f(t)$
### Tipologie
 Possono classificarsi in due tipologie:
 - Tempo continuo:  valutazione istante per istante
   ![[continuo.png]]
 - Tempo discreto: viene scelta un'unità di misura $K$ tra una data e l'altra
   ![[discreto.png]]
Oltre ai segnali a tempo continuo o discreto esistono anche segnali a valori continui o discreti, formando delle combinazioni o agendo in contemporanea, in particolare: 
- Segnali analogici: tempo e valori continui
- Segnali digitali: tempo e valori discreti

### Segnali Principali
##### Cosinusoidale
$s(t) = A \cos(2\pi f_0t+\varphi_0)$ , con:
- $A$ : ampiezza
- $f_0$ : frequenza
- $\varphi_0$: fase
È un segnale che usa una sola frequenza. 
![[cosinusoidale.png]]
Il valore oscilla tra $A$ e $-A$

##### Rettangolo
$A*rect(t)=
\begin{cases}  
1 &t\in[-\frac{1}{2}, \frac{1}{2}] \\  
0 &altrove
\end{cases}$

![[rect.png]]

con $A=1$ si ottiene un quadrato (se non avviene uno [[Segnali#Scalamento nel tempo|Scalamento nel tempo]])

##### Traingolo
$A*triang(t)=
\begin{cases}  
t+1 &t\in[-1, 0] \\ 
1-t &t\in[0,1] \\
0 &altrove
\end{cases}$

![[triang.png]]
### Operazioni segnali
##### Moltiplicazione per uno scalare
Moltiplicare un segnale per uno scalare, quindi con $A\neq1$, ne modifica l'altezza. 
##### Traslazione nel tempo
Significa passare da un segnale $s(t) \rightarrow y(t)=s(t-t_0)$. Quindi il segnale $s(t)$ viene traslato di un $t_0$ verso destra.
##### Scalamento nel tempo
Significa passare da un segnale $s(t) \rightarrow y(t)=s(\frac{t}{A})$. Avviene una deformazione lungo il tempo. All'aumentare di $A$ diminuisce l'argomento di $s$, il segnale subisce un "allargamento."
##### Traslazione + Scalamento
$s(t)\rightarrow y(t)=s(\frac{(t-t_0)}{A})$. Subisce una traslazione di un fattore $t_0$ e un scalamento di un fattore $A$.
È dunque possibile dividere in due fasi questa operazione:
- Scalamento: $s(t) \rightarrow z(t)= s(\frac{t}{A})$
- Traslazione: $z(t) \rightarrow y(t)=z(t-t_0) = s(\frac{(t-t_0)}{A})$

### Campionamento 
Produce un segnale a tempo discreto a partire da uno continuo. Si sceglie un periodo di campionamento $T_i$ e si segnano i punti del segnale continuo ogni $T_i$.

![[campionamento.png]]
Vale: $s_C(nT) = s(nT)$ , con $s_C$ segnale a tempo discreto post-campionamento. 
### Interpolazione
Produce un segnale a tempo continuo a partire da uno discreto.  Si usa un segnale $h(t)$ (che può essere di qualsiasi tipologia, rect, triang etc.) lo si moltiplica punto per punto al segnale a tempo discreto. Si ottiene dunque un segnale che ha i punti di max e min uguali al segnale discreto di partenza ma assume la forma del segnale $h(t)$.
![[Interpolazione.png]]
Vale $s(t) = \sum_{n=-\infty}^{+\infty}s_C(nT)*h(t-nT)$

### Somma di segnali
Viene eseguita istante per istante dell'altezza di ogni segnale.

![[sum.png]]