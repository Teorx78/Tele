Dato $P(X)$ la probabilità che si verifichi l'evento $X$, si ha:
- $P( X \cup Y)$ : Probabilità che $X$ o $Y$ si verifichino (o entrambi, se disgiunti)
- $P( X \cap Y)$ : Probabilità che $X$ e $Y$ si verifichino 
- $P(X \cup Y) = P(X) + P(Y) - P(X \cap Y)$

### Variabili aleatorie Discrete
Una v.a. $X$ ha un alfabeto e può assumere un solo valore di esso alla volta.
$A_X = \{a_1,\cdots,a_N\}$ , con $a_i\in R$
Hanno una funzione densità:
$P_X(a_i) = P(X=a_i)$ , con $i = \{1, \cdots N \}$

Ha come proprietà che $\sum_{i=1}^N P_X(a_i)=1$

### Probabilità Condizionata 
 - Per Eventi : $P(X|Y) = \frac{P(X \cap Y)}{P(Y)}$ 
 - Per v.a. : $P(X=a_i | Y= b_j)$

### Variabili aleatorie Indipendenti
$X$ e $Y$ sono indipendenti se solo se $P(X=a | Y= b) = P_X(a) * P_Y(b)$

### Valore Atteso
- $E[X] = \sum_{a\in A}^N a\times P_X(a) = m_X$ con $m_X$ Media di $X$
- $E[X^2] = \sum_{a\in A}^N a^2\times P_X(a) = M_X$ con $m_X$ Potenza di $X$

Si ha che $M_X = m^2_X + \sigma^2_X$ dove $\sigma^2_x = E[(X - m_X)^2]$ 

Il valore atteso ha come proprietà:
- $E[A_X + B_Y] = A \times E[X] + B \times E[Y]$
- $E[X,Y] = E[X] \times E[Y]$ se $X$ e $Y$ sono indipendenti (dette anche incorrelate)

### Variabili aleatorie Continue
Sono caratterizzate da un alfabeto infinito e non numerabile (ad esempio $R$)

Viene definita la funzione di distribuzione di probabilità: $F_X(a)=P(X)\leq a)$. In particolare si ha che $P(X \in [A,B]) = F_X(B)-F_X(A)$

Viene definita invece densità di probabilità: $f_x(a) = \frac{df_X(a)}{dX}$
Ha come propietà:
- $\int_{-\infty}^{\infty} f_X(a) \, dx = 1$ : Normalizzazione
- $\int_{A}^{B} f_X(a) \, dx \geq 0$ 

### Variabile Aleatoria Gaussiana
Ha come densità:
$f_X(a)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2}(\frac{a-m}{\sigma})^2}$ 

![[gaussiana.png]]

Dove:
- $\sigma$ : varianza, indica la "larghezza" delle gaussiana
- $m$ : media, indica il punto di massimo lungo l'asse orizzontale

Ha come notazione $X \sim \mathcal{N}(m,\sigma)$

Vale che:
- se ho v.a. Gaussiane incorrelate $\leftrightarrow$ sono indipendenti
- se ho v.a. solo incorrelate $\rightarrow$ sono indipendenti
### Funzione Q
Per calcolare la densità di v.a. gaussiana in un determinato intervallo, si utilizza la funzione Q: $Q(A) = P(X \geq A)$ con $X$ una v.a. gaussiana standard($m= 0$ , $\sigma = 1$).

![[funzioneQ.png]]
In particolare $F_X(A) = P(X \leq A) = 1-Q(A)$, vale quindi $P(X \in [A,B]) = Q(A) - Q(B)$

### Variabile Aleatoria Non Standard
$P(X \geq A) = \int_{A}^{+\infty}f_X(a) \, da = Q(\frac{A-m}{\sigma})$ 

### Teorema del Limite Centrale
La somma di v.a. indipendenti qualsiasi con la stessa densità di probabilità (anche per le discrete) converge in una gaussiana:
$\frac{1}{\sqrt N}\sum_{i=0}^NY_i \rightarrow \mathcal{N}(m, \sigma)$ , con:
- $m$ : $E[Y_i]$
- $\sigma$ : $\sqrt{E[(Y_i-m)^2]}$
