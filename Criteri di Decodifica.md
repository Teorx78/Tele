Considerando uno spazio $A^n$ (dove $A$ è un'alfabeto) di possibili word ricevute $\widetilde{c}_m = \xi \in A^n$. Lo dividiamo in $2^k$ insiemi disgiunti ${R_{\beta_i}, i=1,...,2^k}$, chiamate decoding regions, una per ogni information word $b_m = \beta_i$. Quindi la regola di decoding è: 
"Se $\widetilde{c}_m \in R_{\beta_i} \Rightarrow \hat b_m = \mu_d(\widetilde{c}_m) = \beta_i$" , con:
- $\hat b_m$ sequenza in uscita dal decoder
- $\mu_d(\widetilde{c}_m)$ decodifica di $\widetilde{c}_m$
In pratica il decoder associa ad ogni word $\widetilde{c}_m$ un'unica information word $\hat b_m$

Anche qui è presente la probabilità di decisione corretta molto simile a quella vista nella [[Regioni di Decisione#Probabilità di decisione corretta|modulazione]]:

$P(c)=\sum_{l=1}^{2^k}P(\hat c_0=c | c=c_l)*P(c_l)$

### MAP
$\hat c(\underline{\beta}) = argmax_{\underline{\alpha}\in l} f(\underline{\widetilde c}=\underline{\beta}|\vec c = \underline{\alpha})*f(\vec c=\underline{\alpha})$ , dove:
- $\underline{\hat c}(\underline{\beta})$ è la codeword decisa quando riceviamo la sequenza di $n$ bit $\beta$
- $l$ la codifica
- $f(\underline{\widetilde c}=\underline{\beta}|\vec c = \underline{\alpha})$ : probabilità di transizione del canale da $\underline{\alpha}$ a $\underline{\beta}$ (che sono sequenze binarie)
### ML
$\hat c(\underline{\beta}) = argmax_{\underline{\alpha}\in l} f(\underline{\widetilde c}=\underline{\beta}|\vec c = \underline{\alpha})$

### MD di Hamming
Considero le sequenze binarie:
$\underline{\alpha} = [sequenza\;di\;n\;bit]$
$\underline{\beta} = [sequenza\;di\;n\;bit]$

$d_H (\underline{\alpha} ,\underline{\beta}) = \sum_{i=1}^n (\alpha_i - \beta_i)$ , dove $(\alpha_i - \beta_i)$ è la differenza bianaria. 
$d_H$ indica la distanza di Hamming ovvero il numero di posizioni in cui le sequenze sono diverse.

Viene definito dunque il criterio di Minima Distanza di Hamming:
$\hat c(\underline{\beta}) = argmin_{\underline{\alpha}\in l} d_H(\underline{\alpha},\underline{\beta})$ 
 

#codifica_di_canale 