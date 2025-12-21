Definiamo:
- spazio degli eventi $\Omega =\{A_1,\dots,A_n\}$ 
- [[Ripasso Probabilità|probabilità]] degli eventi$ P(A_i)$
Vogliamo misurare l'informazione portata da un evento, la indichiamo con $i(A)$

### Assiomi dell'informazione 
$i(A) \;\;\;\;\; A\in\Omega \;\;\;\;\; i(A)\in R$
1) $i(A) \geq 0 \;\;\; \forall A$
2) $P(A) \leq P(B) \;\;\;\;\; i(A) \geq i(A) \geq i(B)$
3) $i(\Omega)=0$
4) se $A$ e $B$ sono indipendenti $\Rightarrow i(A \cap B) = i(A) + i(B)$

L'insieme delle funzioni che soddisfano gli assiomi dell'informazione è:
$\{i(A) = - log_b(P(A)=log_b\frac{1}{P(A)})\}$ per $b>1$
In particolare si definisce:
- $b = 2 \;\;\;\; i(A) = -log_2(P(A))$ che ha come unità di misura il bit
- $b = e \;\;\;\; i(A) = -ln(P(A))$


#informazione_e_entropia