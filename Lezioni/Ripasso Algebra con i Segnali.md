### Spazio vettoriale dei segnali ad energia finita
I vettori sono tutti i segnali ad [[Energia di un Segnale|Energia]] finita: ${s(t):E_s < +\infty}$

Valgono le operazioni di uno spazio vettoriale:
- Somma: $z(t) = x(t) + y(t)$
- Prodotto con scalare: $z(t) = Ax(t) , con A \in R$
### Prodotto interno
$<x(t), y(t)> = \int_{-\infty}^{+\infty}x(t)*y(t) \, dt$
Vale quindi: $<x(t), x(t)> = \int_{-\infty}^{+\infty}x^2(t) \, dt = E_x$
### Linearità del prodotto
$<\alpha x_1(t) + \beta x_2(t), y(t)> = \alpha<x_1(t), y(t)> + \beta<x_2(t), y(t)>$

### Norma di un vettore
$||x(t)|| = \sqrt{<x(t), x(t)>} = \sqrt{E_x}$

### Sottospazio generato da $M$ segnali
Dati $M$ segnali $s_1(t),\dots,s_M(t)$ , il sottospazio da essi generato ha come vettori:
$S=\{s(t):s(t)=\sum_{m=1}^M\alpha_mS_m(t)\}$
$\forall x_1(t),x_2(t) \in S \Rightarrow Ax_1(t)+Bx_2(t) \in S$

### Base Ortonormale
Dato l'insieme dei segnali: $\phi_i(t), i \in [1,\dots,I]$, dove:
- Ortogonali: sono tale che il [[Ripasso Algebra con i Segnali#Prodotto interno|prodotto interno]]: $<\phi_i(t),\phi_j(t)>=0$
- Normalizzati: la [[Ripasso Algebra con i Segnali#Norma di un vettore|norma]] $||\phi_i(t)||=1$ , $\forall i$
In generale $I \leq M$

### Proiezioni vettori 
Sia $s(t) \in S$ , con $\phi_1,\dots,\phi_I$ base ortonormale di $S$. Viene definita la proiezione del segnale $S$ sul segnale $\phi_i(t)$:
$s(t)=\sum_{i=1}^{I}<s(t), \phi_i(t)>\phi_i(t)$

### Distanza tra vettori
Siano dati i segnali: $x(t) \rightarrow \vec x = [x_1,\dots,x_I]$ e $y(t) \rightarrow \vec y = [y_1,\dots,y_I]$. La distanza tra $\vec x$ e $\vec y$ è data dalla [[Ripasso Algebra con i Segnali#Norma di un vettore|norma]]:
$||\vec x - \vec y|| = \sqrt{\sum_{i=1}^I[x_i-y_i]^2}$

### Procedura di Gramn-Schimdt
Da $M$ segnali $s_1(t),\dots,s_M(t)$ ottengo i segnali $\phi_1(t),\dots,\phi_I(t)$, base ortogonale del sottospazio generato da $s_1(t),\dots,s_M(t)$
1) Considero $s_1(t)$:
   - se $s_1(t)$ è nullo ($s_1(t)=0 \forall t$), lo scarto e passo al successivo
   - altrimenti il primo segnale della base è $\phi_1(t) = \frac{s_1(t)}{\sqrt{E_{s_1}}}$
2) Al passo $n$-esimo avrò una base parziale: $\phi_1(t),\dots,\phi_k(t)$ , con $k \leq m$, considero il segnale:
   $\phi_{k+1}'(t)=s_m(t)-\sum_{i=1}^k<s_m(t),\phi_i(t)>\phi_i(t)$
   - se $\phi_{k+1}'(t)$ è identicamente nullo allora lo scarto
   - altrimenti aggiungo alla base parziale: $\phi_{k+1}(t) = \frac{\phi_{k+1}'(t)}{\sqrt{E_{\phi_{k+1}}}}$
#ripassi