Definiamo l'[[Teoria dell'informazione|informazione]] di una [[Ripasso Probabilità|variabile aleatoria discreta]], come la funzione di informazione della variabile aleatoria stessa:
$x \in A_x=\{a_1,\dots,a_n\} \;\;\;\;i_x(a) = i(x=a) \;\;\; a\in A_x$

Definiamo quindi l'entropia di una variabile aleatoria discreta come:
$H(x) = E[i_x(x)] = E[-log_2P_x(x)]$ , dove il pedice è il nome della variabile.

### Proprietà dell'entropia
1) $H(x) \geq 0$ poiché sia l'informazione che la densità di probabilità sono positive
2) $H(x) = 0 \Leftrightarrow x$ è deterministica, ovvero: $A_x{a} \;\; P(x=a)=1$

### Funzioni concave
Una funzione $f$ è strettamente concava se dati $k_1,\dots,k_N>0$ tali che $\sum_{i=1}^Nk_i =1$ e dati $a_1,\dots,a_n$ distinti, vale che: 
$\sum_{i=1}^Nk_nf(a_n) < f(\sum_{i=1}^Nk_na_n)$

### Disuguaglianza di Jensen
Sia f(x) una funzione per strettamente concava per una qualsiasi variabile aleatoria $x$ :
$E(f(x)) < f(E(x))$

### Limite superiore dell'entropia
Una v.a. discreta $x$ con alfabeto di cardinalità $M$ ha entropia limitata superiormente da $log_2M$:
$H(x) \leq log_2M$ che si misura in bit.
Inoltre $H(x) = log_2M$ se e solo se $x$ è uniforme nell'alfabeto (ogni risultato ha la stessa probabilità di verificarsi)

### Vettore aleatorio
$\underline{x} = [x_1,\dots,x_n]$ , dove $x_i$ è una variabile aleatoria discreta.
[[Ripasso Probabilità#Variabili aleatorie Discrete|Densità di probabilità]] del vettore aleatorio: $p_{\underline{x}}(\underline{a}) = P[\underline{x}=\underline{a}=[a_1,\dots,a_N]]= P(x_1=a_1,\dots,)$ 

Funzione informazioni di vettori:
$i_{\underline{x}}(a) =log_2\frac{1}{p_{\underline{x}}(\underline{a})}$ , con:
- $\underline{a} = A^N= A*A*\dots*A*A$
- $x_i\in A$
##### Entropia di vettori aleatori
$H(x) = E[i_x(x)] = \sum_{\underline{a} \in A_{\underline{x}}}p_{\underline{x}}(\underline{a})log_2\frac{1}{p_{\underline{x}}(\underline{a})}$

### y come funzione deterministica di x
Sia $y=f(x)$ , dove $b = f(a)$ funzione algebrica.

In [[Canale AWGN|AWGN]] si ha invece: $r=f(s)=s+w$. Dunque la presenza di un termine $w$ la rende non deterministica.

In caso deterministico si ha: $H([x,y]) = H(x)$

### Entropia congiunta di v.a.
Significa calcolare $H(x,y) \neq H([x,y])$, si divide in due casi:
- Se sono indipendenti: $H(x,y)=H(x)+H(y)$
- Se sono non indipendenti: $H(x,y)<H(x)+H(y)$

### Entropia di v.a. condizionate
Se $x$ è condizionata a $y$ la densità di probabilità condizionata è: $p_{x|y}(a|b)=P(x=a|y=b)$. Dunque si può riscrivere la funzione informazione come: $i_{x|y}(a|b)=-log_2p_{x|y}(a|b)$. Quindi l'entropia di una v.a. condizionata al valore di un'altra v.a. sarà:
$H(x|y=b)=\sum_ap_{x|y}(a|b)log_2\frac{1}{p_{x|y}(a|b)}$
Se invece $x$ e $y$ sono indipendenti $H(x|y=b)=H(x)$
##### Entropia condizionata
$H(x|y)=\sum_{a,b}p_{x,y}(a|b)log_2\frac{1}{p_{x|y}(a|b)}=E_{x,y}[log_2\frac{1}{p_{x|y}(a|b)}]$
Dunque si può anche riscrivere: $H(x,y) = H(y|x)+H(x)$

### Informazione mutua tra due v.a.
$I(x;y)=H(y)-H(y|x)=H(x)-H(x|y) \Rightarrow \, \leq min\{H(x),H(y)\}$ ma è sempre una quantità positiva.
Se $x$ e $y$ sono indipendenti $\Rightarrow I(x;y)=0$
Se $x$ è funzione deterministica di $y$ ($y=x$) $\Rightarrow I(x;y)=H(x)$






#informazione_e_entropia 

