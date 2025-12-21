### Matrice di controllo parità
Viene definita come $\underline{\mathcal H}$ ed è il controllo parità per il codice $\mathcal C$ se soddisfa:
$\underline{H}_\underline{\gamma} = 0 \Leftrightarrow \underline{\gamma} \in \mathcal C$ 

In particolare se $\underline{\gamma} = \underline{\mathcal G} \underline{b}$ dunque $\underline{\mathcal G}\,\underline{\mathcal H} = 0$ e il rango di $\underline{\mathcal H}=n-k$ allora $\underline{\mathcal G}$ è [[Codici lineari a blocco#Matrice generatrice di un codice lineare a blocco|generatrice]] di della codice lineare $\mathcal C$ avrà come matrice parità $\underline{\mathcal H}$. 


### Decodifica con sindrome
Una sindrome è: $\underline{\sigma} = \underline{\mathcal H}\,\underline{\gamma}$ , con:
- $\underline{\gamma}$ sequenza ricevuto (codeword)
- $\underline{\mathcal H}$ matrice di controllo parità
- $\underline{\sigma}$ sindrome associata a $\underline{\gamma}$

Dunque $\underline{\sigma} = 0 \Leftrightarrow \underline{\gamma} \in \mathcal C$
Si ha quindi $\underline{\gamma} = \underline{\hat c} + \underline{\varepsilon}$ con $\underline{\varepsilon}$ ha dimensione $n$, $||\underline{\varepsilon}||_H$ minimo e $\underline{\hat c}$ la parola più vicina a $\underline{\gamma}$

Passaggi della decodifica:
1) calcolo $\underline{\sigma} = \underline{\mathcal H}\,\underline{\gamma}$
2) cerco tra tutti i vettori $\underline{\varepsilon} = [\vdots]$ tali che $\underline{\sigma} = \underline{\mathcal H}\,\underline{\varepsilon}$ , uno che abbiamo il [[Codici lineari a blocco#Peso di Hamming|peso di Hamming]] minimo $\underline{\varepsilon}_{min}$
3) decodifico $\underline{\gamma}$ in $\underline{\hat c} = \underline{\gamma} + \underline{\varepsilon}_{min}$

$\underline{\sigma}$ ha lunghezza $n-k$ e ci sono $2^{n-k}$ possibili $\underline{\sigma}$.
Trovato un $\underline{\varepsilon}$ tale che $\underline{\sigma} = \underline{\mathcal H}\,\underline{\varepsilon}$ , allora tutti gli altri vettori che hanno la stessa sindrome si chiamano coset associati a $\sigma$ e sono tutti i $\underline{\varepsilon} + \underline{c} \; \forall\underline{c}$. Ho $2^{n-k}$ coset, ognuno con $2^k$ vettori, quindi in tutto ho $2^n \underline{\varepsilon}$ tra tutti i coset. Il coset con il peso di Hamming minimo si chiama, coset leader. 

In generale: 
- $\underline{\gamma} = \underline{c}_1 + \underline{\varepsilon}_2$ 
- $\underline{\gamma} = \underline{c}_2 + \underline{\varepsilon}_2$
- $\underline{\mathcal H}\underline{\varepsilon}_1=\underline{\mathcal H}\underline{\varepsilon}_2=\underline{\sigma}$ 
- $||\varepsilon_1||_H = ||\varepsilon_2||_H$ 


##### Costruzione di una tabella coset leader
Tabella cose

| $\underline{\sigma}$ | $\underline{\varepsilon}_{min}$ |
| -------------------- | ------------------------------- |
| 00                   | 00000                           |
| 01                   | 01000                           |
| 10                   | 00011                           |
| 11                   | 00100                           |

Dalla colonna $\underline{\epsilon}_{min}$ trovo $n$ quindi sapendo il numero di bit sulla colonna $\underline{\sigma}$ posso trovare $k$, quindi $2=n-k \Rightarrow k=3$. Posso quindi sapere che lo spazio occupato è $n*(2^{n-k} -1)$.

#codifica_di_canale 
