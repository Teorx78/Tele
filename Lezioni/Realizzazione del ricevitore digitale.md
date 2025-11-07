Le fasi del ricevitore digitale son:
1) Proiezione della base ortogonale: dato il segnale ricevuto $r(t)=s_n(t) + w(t)$ , lo proietto sulla base ortogonale $\{\phi_1(t),\dots, \phi_N(t)\}$. Trasforma il segnale continuo in un vettore a componenti finite, dove $\phi$ è il filtro (sistema elettronico che trasforma un segnale in ingrasso in uno di uscita)
2) Moltiplicazione per le funzioni della base: $\forall\phi_i \rightarrow r_i=\int_{kT}^{(k+1)T}r(t)\phi_i(t)$
3) Ottengo così il vettore $\vec r$ con i suoi coefficenti $r_1,\dots,r_N$ che rappresenta il vettore ricevuto nello spazio dei segnali (la [[Demodulazione Digitale#Costellazione associata alla segnalazione|costellazione]]). 
4) Decisione del simbolo ricevuto, si applica quindi il [[Regioni di Decisione#Criteri di Decisione|criterio di decisione]] più appropriato

### Implementazione con la base con convoluzione
Viene definito Ricevitore di tipo 1.

Formula generale di un filtro:
$(x*h)(t) = \int_{-\infty}^{+\infty}x(t-\tau)h(t) \, d\tau = y(t)$ , con:
- $(x*h)(t)$ : convoluzione
- $x(t)$ : segnale d'ingresso
- $x(t-\tau)$ : segnale di ingresso ritardato di $\tau$
- $h(\tau)$ : risposta impulsiva del filtro, come il filtro reagisce all'impulso in ingresso al tempo $\tau$
- $y(t)$ : uscita

Nel ricevitore di tipo 1 si ha il segnale $r(t) = s(t) + w(t)$ e $\phi(t)$ come base ortogonale. Si sceglie $h(t) = \overline\phi (-t)$ 

$\Rightarrow r_i[k]=\int_{-\infty}^{+\infty}r(kT+T-\tau)\overline\phi_i(\tau) \, d\tau$

Poi si applicano i criteri di decisione per trovare $\hat a_k$

### Implementazione per il ricevitore a minima distanza

Viene eseguito semplicemente:
$\hat a_k = arg_mmax[<\vec r , \vec s> - \frac{1}{2}E_{s_m}]$

#modulazione 