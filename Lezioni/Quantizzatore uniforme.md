È un tipo di [[Quantizzazione|quantizzazione]].
I valori dell'alfabeto sono spaziati linearmente$A_q=\{a_1, a_1+\Delta, a_1+2\Delta, \dots\}$ , con $\Delta$ : passo di quantizzazione.
La quantizzazione viene fatta a livelli $L$![[quantizzatore_uniforme.png]]ogni livello è rappresentato da un segmento orizzontale, prima del più basso e dopo il più altro quindi rispettivamente prima di $-\frac{L}{2}\Delta = -\mathcal v_{sat}$ e dopo $\frac{L}{2}\Delta = \mathcal v_{sat}$. 

Ogni segmento rappresenta una sequenza di bit (ne può rappresentare $log_2L$) e dista $\Delta$ in altezza e in lunghezza.
### Errore di quantizzazione
$e_q = x - x^{(q)} = x- Q(x)$ 
si ha con $x \notin [-\mathcal v_{sat}, \mathcal v_{sat}]$ ho errore di saturazione $|e| \geq \frac{\Delta}{2}$ e non limitato. Probabilità di saturazione: $P_{sat} = P(x \notin [-\mathcal v_{sat}, \mathcal v_{sat}])$ Con varianza $\sigma^2_{e_q} = \frac{\Delta^2}{12}$
### Errore granulare
Si ha quando $x \in [-\mathcal v_{sat}, \mathcal v_{sat}]$, se $L >>0$ abbiamo dunque molti livelli e intervalli di quantizzazione$e_{gr} \in \{-\frac{\Delta}{2}\frac{\Delta}{2}\}$ con varianza $\sigma^2_{e_{gr}} = \frac{\Delta^2}{12}$

#quantizzazione 