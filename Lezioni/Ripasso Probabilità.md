Dato $P(X)$ la probabilità che si verifichi l'evento $X$, si ha:
- $P( X \cup Y)$ : Probabilità che $X$ o $Y$ si verifichino (o entrambi, se disgiunti)
- $P( X \cap Y)$ : Probabilità che $X$ e $Y$ si verifichino 
- $P(X \cup Y) = P(X) + P(Y) - P(X \cap Y)$

### Variabili aleatorie discrete
Una v.a. $X$ ha un alfabeto e può assumere un solo valore di esso alla volta.
$A_X = \{a_1,\cdots,a_N\}$ , con $a_i\in R$
Hanno una funzione densità:
$P_X(a_i) = P(X=a_i)$ , con $i = \{1, \cdots N \}$

Ha come proprietà che $\sum_{i=1}^N P_X(a_i)=1$

### Probabilità Condizionata 
 - Per Eventi : $P(X|Y) = \frac{P(X \cap Y)}{P(Y)}$ 
 - Per v.a. : $P(X=a_i | Y= b_j)$

### V.A. Indipendenti
$X$ e $Y$ sono indipendenti se solo se $P(X=a | Y= b) = P_X(a) * P_Y(b)$

### Valore Atteso
$E[X] = \sum_{a\in A}^N a\times P_X(a) = m_X$ con $m_X$ media di $X$
