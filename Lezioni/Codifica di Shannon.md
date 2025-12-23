$l_i= \lceil log_{\frac{1}{M_y}}p_x(\underline a_i) \rceil$ , con $\underline a_i\in \mathcal D_x$

Se $p_x(\underline a_i)$ sono potenze interne di $\dfrac{1}{M_y}$ allora la [[Codifica di sorgente#Teorema di Shannon per la codifica di sorgente|lunghezza media]] diventa:
$L_y = E[log_{\frac{1}{M_y}}p_x(\underline a_i)] = \dfrac{H(x)}{log_2M_y} \Rightarrow$ in questo caso il codice di Shannon è ottimo.


### Codifica di sorgente Ottima
Codice con lunghezza minima delle parole di codice ([[Codifica di Canale|codeword]])

Per un codice a prefisso ottimo, le codeword a più bassa probabilità hanno lunghezza maggiore

Nel dizionario di un codice a prefisso ottimo ci sono almeno due parole di codice $\underline b'$ e $\underline b''$ che hanno lunghezza massima e differiscono solo nell'ultimo simbolo

### Procedura di Hauffman
Data la distribuzione di dell'ingresso $p_x(\underline a_i) \;\;\;\; \underline a_i\in \mathcal D_x$
1) ordino le probabilità in ordine decrescente
2) raccogliamo le codeword con probabilità più bassa in un'unica soluzione parola di codice con probabilità somma delle due probabilità 
3) ripetiamo la procedura





#codifica_di_sorgente 