$M>2$ quindi ogni segnale rappresenta $log_2M$.
Significa che ogni simbolo porta più bit, dunque $\rightarrow P(E)$ diventa la [[Modulazione Binaria#Probabilità d'errore|probabilità d'errore]] sul simbolo e la probabilità sul bit è impostata sulla sequenza di bit.
- $P(E) = P(\hat a_0 \neq a_0)$
- $P_{bit} = P(\hat b_l \neq b_l)$

Definiamo l'evento: $\mathcal E_{m,n} \{d(\vec r,s_m > d(\vec r, s_n\}$, significa che rappresenta l'evento dove il vettore $\vec r$ è più vicino ad $s_m$ che ad $s_n$.

### Limite superiore e inferiore alla probabilità d'errore
##### Limite superiore alla probabilità d'errore
$P(E) \leq \frac{1}{M} \sum_{n=1}^M \sum_{m=1 , M \neq n}^M Q(\frac{d_{m,n}}{2\sigma_w})$
##### Limite inferiore alla probabilità d'errore
$P(E) \geq \frac{1}{M} \sum_{n=1}^M  Q(\frac{d_{min,n}}{2\sigma_w})$ , con $d_{min,n} = min_{\{1,\dots,M\}} d_{m,n}$

È quindi possibile scrivere:
$\frac{N_{min}}{M}Q(\frac{d_{min}}{2\sigma_w}) \leq P(E) \leq (M-1)Q(\frac{d_{min}}{2\sigma_w})$

#modulazione 