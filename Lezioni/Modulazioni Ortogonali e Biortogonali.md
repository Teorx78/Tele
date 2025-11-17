Sono un sottoinsieme di [[Modulazione M-arie|modulazioni M-arie]]. 

### Ortogonali
Sono tutte le forme d'onda M-ary che sono [[Modulazione Binaria#Segnali Ortogonali|ortogonali]] tra loro. 

Se tutti $s_n(t) \neq 0 \Rightarrow \phi_i(t)=\frac{s_i(t)}{\sqrt E_{s_i}}$ , con $i \in  [1,\dots,M]$ 
$d_{m,n} = \sqrt{E_{s_n} + E_{s_m}} = \sqrt{\sum_{i=1}^I(s_{n,i}-s_{m,i})^2}$ , se hanno tutti la stessa energia:
- $d_{m,n} =\sqrt{2E_s} = d_{min,n}$

### Pulse Position Modulation
Sono una tipologia di segnali ortogonali, in pratica sono segnali che vengono inviati con ampiezza $A$ e periodo $T$ costanti. 

Inoltre si ha che hanno tutti la stessa [[Energia di un Segnale|energia]]: $E_{s_n} = E_{s_m} = E_s$

### Biortogonali
Significa che dati $M$ segnali, $\frac{M}{2}$ sono [[Modulazione Binaria#Segnali Ortogonali|ortogonali]] tra loro e gli altri $\frac{M}{2}$ sono [[Modulazione Binaria#Segnali antipodali|antipodali]] ai primi.
- $<s_i(t),s_j(t)> = 0$ , con $i\neq j, i,j \in [1,\dots,\frac{M}{2}]$
- $s_i(t) = - s_{i + \frac{M}{2}}(t)$ , con $i \in [1,\dots,\frac{M}{2}]$

$d_{m,n}=
\begin{cases}  
\sqrt{2E_s} &se \,s_m\,e \,s_n \, non \, antipodali \\  
2\sqrt{E_s} &se \,s_m\,e \,s_n \, antipodali
\end{cases}$

In generale ogni vettore ha $(M-2)$ segnali a lui ortogonali e uno a lui antipodale
$P(E) \leq \frac{(M-2)}{M}Q(\frac{\sqrt{2E_s}}{2\sigma_w})+\frac{1}{M}Q(\frac{2\sqrt{E_s}}{2\sigma_w})$

### Pulse Amplitude Modulation
I segnali della segnalazione sono versioni scalate in ampiezza di un segnale prototipo chiamato "impulso".

![[impulso.png]]

$s_m(t) = \alpha_mh_{Tx}(t)$ , con $\alpha_m = 2m-1-M$ e $m \in [1,\dots,M]$ dunque $\alpha_m \in valori\,dispari\{-M+1 , M-1\}$
Ad esempio se $M = 64 \Rightarrow \alpha_m \in \{-63,\dots,-3,-1,1,3,\dots,63\}$

La base è: 
$\phi_1(t)= \frac{h_{Tx}(t)}{\sqrt{E_{h_{Tx}}}} \Rightarrow s_m(t) = \alpha_m\sqrt{E_{h_{Tx}}}\phi_1(t)$ , dove $\alpha_m\sqrt{E_{h_{Tx}}}=s_{m,1}$
$d_{min} = 2\sqrt {E_{h_{Tx}}}$

L'[[Modulazione Binaria#Energia media della segnalazione|energia media]]:
$E_s = \frac{M^2-1}{3}E_{h_{Tx}}$

Le [[Regioni di Decisione|regioni di decisione]] sono divise in:
- interne, quindi tutte quelle regioni $\mathcal R_i$ , con $i \in ]1,\dots,M[$
- esterne, quindi $\mathcal R_1$ e $\mathcal R_M$
Ho sempre $2$ regioni interne e $(M-2)$ regioni esterne
La probabilità d'errore: $P(E)=\sum_{m=1}^MP(\vec r \notin \mathcal R_m|a_0=m)\frac{1}{M}$, che diventa:
- interne: $2Q(\frac{d_{min}}{2\sigma_w})$ 
- esterne: $Q(\frac{d_{min}}{2\sigma_w})$
Sempre con $d_{min} = 2\sqrt {E_{h_{Tx}}}$

La probabilità di errore corretta sul simbolo è: 
$P(E) = 2(1-\frac{1}{M})Q(\sqrt{\frac{E_s*3}{\sigma_w*(M^2-1)}})$
$P_{bit}\simeq\frac{P(E)}{log_2M}$

#modulazione 
