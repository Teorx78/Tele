Le word costituiscono uno spazio (sottospazio) [[Ripasso Algebra con i Segnali|vettoriale]] 

### Spazio vettoriale delle sequenze binarie di n bit
$\underline{x} = [x_1,\dots,x_n]$ , con $x_i \in \{0,1\}$
$\underline{y} = [y_1,\dots,y_n]$ , con $y_i \in \{0,1\}$

Proprietà:
- $\underline{x} +\underline{y} = \underline{z}$ , con $\underline{z}=[z_1,\dots,z_n]$ e si ha: $z_i=x_i\oplus y_i$ 
- dato $\alpha \in \{0,1\} \Rightarrow \alpha\underline{x} = [\alpha x_1,\dots,\alpha x_n]$ 
- $\underline{x} -\underline{y} = \underline{z}$ tale che $\underline{z}+\underline{y} = \underline{x}$
### Norma di Hamming
$||\underline{x}||_H$ ritorna il numero di $1$ presenti nella sequenza

Proprietà:
1) $||\underline{x}||_H > 0$
2) $||\underline{x}||_H = 0 \Leftrightarrow \underline{x}=0$
3) $||\alpha\underline{x}||_H=||\alpha||*||\underline{x}||_H$
4) $||\underline{x}+\underline{y}||_H \leq ||\underline{x}||_H+||\underline{y}||_H$

Si può riscrivere la [[Criteri di Decodifica#MD di Hamming|distanza di Hamming]] come:
$d_{min}=d_H(\underline{x},\underline{y}) = ||\underline{x}-\underline{y}||_H$
Un codice a blocco lineare $\mathcal C = \{\underline{c}_1,\dots,\underline{c}_n\}$ è un qualsiasi sottospazio lineare dello spazio delle sequenze lunghe $n$. 
$|\mathcal C|=2^k$

### Matrice generatrice di un codice lineare a blocco
È una matrice $\underline{G}$ di dimensione $n$ x $k$, tale che $\underline{G}$ ha rango $k$.

Si ha che le word $\underline{c} = \underline{G}\underline{b} \;\; \forall \underline{b}$ , con $\underline{b}$ sequenza lunga $k$ che viene codificata in $\underline{c} \Leftrightarrow \underline{c} \in \mathcal C$ 
$\begin{bmatrix} c_1 \\ \vdots \\ c_n \end{bmatrix} = \underline{\mathcal G} \begin{bmatrix} c_1 \\ \vdots \\ b_k \end{bmatrix}$ 

Ogni colonna di $\underline{\mathcal G}$ è una word.

$\underline{G}$  semplifica le operazioni di codifica:
- Se $\mathcal C$ non è lineare serve una tabella di $2^kn$ bit
- Se $\mathcal C$ è lineare serve una tabella di $nk$ bit

Matrice generatrice in forma sistematica: significa rappresentare il codice in modo tale che i bit di informazione compaiano esplicitamente e invariati all’interno della codeword, mentre i restanti bit sono bit di ridondanza calcolati come combinazioni lineari dei bit informativi.
In particolare una matrice generatrice sistematica $k$ può essere riscritta come:
$\underline{G} = \underline{\mathcal I} | \underline{A}$ , dove:
- $\underline{\mathcal I}$ è la matrice identità $k$ x $k$
- $\underline{A}$ è la matrice $n-k$ x $k$
Dunque sarà possibile riscrivere l'operazione $\underline{c} = \underline{ G}\underline{b} = [\underline{b}|\underline{b}\underline{A}]$. 

### Peso di Hamming
Il peso di Hamming di una sequenza binaria è: $w_H(\underline{x}) = ||x||_H$
Il peso di Hamming di un codice è: $w_H(\mathcal C) = min\,w_H(\underline{c})$ 

In un codice lineare a blocco il peso di Hamming del codice è uguale alla distanza minima del codice $\Rightarrow w_H(\mathcal C) = min\,d_H(\underline{c}_i,\underline{c}_j)$ 

### Bound di Singleton
Per codici lineari a blocco la distanza minima del codice è limitata superiormente:
$d_{min} \leq n-k+1$

$\Rightarrow w_H(l_i) \leq 1+(n-k)$ è il peso di ogni colonna della matice che si può riscrivere come:
$\underline{ G} = [\dfrac{\underline{\mathcal I}}{A}]$ il peso di ogni colonna sarà dato dal numero di uno per colonna.



#codifica_di_canale 