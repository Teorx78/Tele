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
1) 



#codifica_di_sorgente