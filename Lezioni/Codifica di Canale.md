È una tecnica che trasforma un messaggio digitale con informazione $\{b_l\}$ in un altro messaggio $\{c_l\}$che è più "robusto" agli errori. La robustezza è data da un po' di ridondanza dovuta all'aggiunta di simboli addizionali determinati in modo univoco dal messaggio con informazione. 
L'insieme dei possibili messaggi trasmessi è $C$, che è un sottoinsieme dei possibili sequenze ricevute $\widetilde{C}$. In pratica ogni messaggio ricevuto $\widetilde{c_l}$ può appartenere a $\widetilde{C}$ se il messaggio contiene errori o a $C$ se il messaggio appartiene all'insieme dei trasmessi.

Quando si ricevono messaggi "non validi" allora ci sono due modi principali per gestirli.

### Automatic Retrasmission Query (o Automatic Repeat Request) 
Definito come ARQ, indica la ritrasmissione di tutto il messaggio (o di una sua parte).

### Foward Error Correction
Definito come FEC, consiste nel rimpiazzare il messaggio ricevuto non valido con un possibile messaggio trasmesso il più possibile simile. 

![[Codifica_di_canale_Blocchi.png]]

- $\vec b$ è lungo $k$ ed è una sequenza di bit del messaggio da codificare $\Rightarrow$ $2^k$ possibili sequenze di $\vec b$
- $\vec c$ è lungo $n$ ed è la codeword (sequenza di bit codificata), esiste una relazione biunivoca tra $\vec b$  e $\vec c$ $\Rightarrow$ $2^k$ possibili codeword e $2^n$ possibili sequenze binarie tra cui scegliere $2^k$ codeword
- $\underline{\widetilde c}$ è lungo $n$ ed è la sequenza di bit ricevuti $\Rightarrow$ $2^n$ possibili sequenze di in uscita dal demodulatore
- $\underline{\hat b}$ sequenza di $k$ bit
- $\underline{\hat c}$ la codeword corrispondente a $\underline{\hat b}$. In generale $\vec c \neq \underline{\widetilde c} \neq \underline{\hat c}$ poiché la prima e la terza sono codeword la seconda no

### Code Ratio
Rappresenta la ridondanza e si intende il rapporto tra il numero di simboli in input e il numero di simboli codificati: $\frac{k}{n}$ è sempre una quantità $\leq 1$ 

 
#codifica_di_canale
