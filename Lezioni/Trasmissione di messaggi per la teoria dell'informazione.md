![[Trasmissione.png]]
La sorgente emette il simbolo $x_n$ al tempo discreto $nT$ e a valori discreti presi da un alfabeto (segnale digitale) $A_x$ con periodo di simbolo $T$. I simboli $y_n$ emessi al tempo $nT$ sono presi da un alfabeto $A_y$

### Entropia di vettori di simboli di sorgente
L'[[Entropia|entropia]] $H([x_{-N},x_{-N+1}, \dots,x_{-1},x_0,x_1,\dots ,x_N])$ dove tutto l'argomento è lungo $2N+1$.
Se $x_n$ sono indipendenti ed equidistanti $\Rightarrow H([x_{-N},\dots, x_N])=\sum_nH(x_n)=(2N+1)H(x_n)$

### Entropia per simbolo
$H_s(\underline{x})=\frac{H(\underline{x})}{2N+1}=\frac{H(\underline{x})}{L(\underline{x})}$ , dove $L(\underline{x})$ è la lunghezza del vettore
Per simboli indipendenti ed equiprobabili: $H_s(\underline{x})=H(x_n)$

Se x ha lunghezza infinita $H_s(\underline{x})=lim_{n\rightarrow \infty}\frac{H([x_{-N},\dots, x_N])}{2N+1}$

##### Informazione mutua per simbolo tra sequenze
$I_s(\underline{x};\underline{y})=H_s(\underline{x})+H_s(\underline{x})-H_s(\underline{x},\underline{y})$ 
##### Tasso di informazione della sorgente
$R(\underline{x})=\frac{H_s(\underline{x})}{T}$ e si misura in bit/s

### Tasso di informazione del canale
$R(\mathcal G)=\frac{I_s(\underline{x};\underline{y})}{T}$ , con $\underline{x}$ e $\underline{y}$ rispettivamente ingresso e uscita del canale.
Dalla [[Entropia#Informazione mutua tra due v.a.|informazione mutua tra due v.a.]] si ha: $R(\mathcal G)\leq R(\underline{x})$

### Capacità di un canale
Consiste nel tasso di informazione del canale massimo rispetto a tutte le statistiche d'ingresso.

$C=max_{p_\underline{x}(\underline{a})}R(\mathcal G)$

#capacità_canale 