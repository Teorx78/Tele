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
[[Ripasso Probabilità#Variabili aleatorie Discrete|Densità di probabilità]] del vettore aleatorio: $P_{\underline{x}}(a) = P[\underine{x}=\underline{a}=[a_1,\dots,a_N]]= P(x_1=a_1,\dots,)$ 



#informazione_e_entropia 

