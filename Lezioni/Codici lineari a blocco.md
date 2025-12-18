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
$d_H(\underline{x},\underline{y}) = ||\underline{x}-\underline{y}||_H$
Un codice a blocco lineare $l = \{\underline{c}_1,\dots,\underline{c}_n\}$ è un qualsiasi sottospazio lineare dello spazio delle sequenze lunghe $n$. 
$|l|=2^k$

### Matrice generatrice di un codice lineare a blocco
È una matrice $\underline{\mathcal G}$ di dimensione $n$ x $k$, tale che $\underline{\mathcal G}$ ha rango $k$.

Si ha che le word $\underline{c} = \underline{\mathcal G}\underline{b} \;\; \forall \underline{b}$ , con $\underline{b}$ sequenza lunga $k$ che viene codificata in $\underline{c} \Leftrightarrow \underline{c} \in l$ 
$\begin{bmatrix} c_1 \\ \vdots \\ c_n \end{bmatrix} = \underline{\mathcal G} \begin{bmatrix} c_1 \\ \vdots \\ b_k \end{bmatrix}$ 

Ogni colonna di $\underline{\mathcal G}$ è una word.

$\underline{\mathcal G}$  semplifica le operazioni di codifica:
- Se $l$ non è lineare serve una tabella di $2^kn$ bit
- Se $l$ è lineare serve una tabella di $nk$ bit

Matrice generatrie in forma sistematica: significa rappresentare il codice in modo tale che i bit di informazione compaiano esplicitamente e invariati all’interno della codeword, mentre i restanti bit sono bit di ridondanza calcolati come combinazioni lineari dei bit informativi.

#codifica_di_canale 