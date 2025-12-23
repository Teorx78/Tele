![[Schema_codifica_di_sorgente.png]]

- $\underline{x}_m \in \mathcal D_x$ : dizionario delle parole emesse dalla sorgente
- $\underline{y}_m \in \mathcal D_y$ : dizionario delle parole di codice con lunghezza variabile

1) La codifica è parola per parola (senza memoria)
2) L'operazione di codifica è invertibile. $\forall \underline{y}_m \in \mathcal D_y$ c'è una sola parola  $\underline{x}_m \in \mathcal D_x : \underline{y} = \mu_s(x)$

### Metrica di valutazione della codifica di sorgente
Se $p_{\underline{x}}(\underline{a}) \;\; \underline{a}\in\mathcal D_x$ è la probabilità che la sorgente generi la parola $\underline{a}$. 

Quindi la lunghezza media delle parole di codice:
$L_y = E_{\underline{x}}[l(\underline{y})]=E_{\underline{x}}[l(\mu_s(\underline{x}))]=\sum_{\underline{a}\in\mathcal D_x}l(\mu_s(\underline{a}))p_{\underline{x}}(\underline{a})$ , con $l(\underline{y})$ lunghezza della parola $\underline{y} \in \mathcal D_y$ 

### Codici a prefisso
In un codice a prefisso nessuna parola è prefisso (la prima parte) di un'altra. Un codice a prefisso è sempre decodifica.

### Teorema di Kraft-McMillan
1) Per ogni codificatore (e decodificatore) di sorgente senza perdite, con alfabeto di parole di codice di cardinalità (numero di elementi nell'alfabeto) $M_y$ vale sempre: $\sum_{\underline y \in \mathcal D_y}\dfrac{1}{M_y^{l(y)}} \leq 1$
2) per una sorgente con dizionario $\mathcal D_x$ di cardinalità $N$, se $l_1,\dots,l_N$ interi tali che: $\sum_{i=1}^N\dfrac{1}{M_y^{l(i)}} \leq 1$ con $M_y$ intero, allora esiste un codice a prefisso per la sorgente con alfabeto di cardinalità $M_y$ e parole di codice di lunghezza $l_1,\dots,l_N$

### Teorema di Shannon per la codifica di sorgente
1) Per ogni codice di sorgente con alfabeto di uscita di cardinalità $M_y$ la lunghezza media deve soddisfare: $L_y\geq\dfrac{H(\underline{x})}{log_2M_y}$ , con $\underline x$ parole $\in \mathcal D_x$ da codificare
2) esiste un codice prefisso con alfabeto di cardinalità $M_y$ e lunghezza media delle parole di codice: $L_y < \dfrac{H(\underline x)}{log_2M_y} + 1$
Dunque esiste sempre un codice a prefisso:
$\dfrac{H(\underline x)}{log_2M_y} \leq L_y < \dfrac{H(\underline x)}{log_2M_y} + 1$



#codifica_di_sorgente