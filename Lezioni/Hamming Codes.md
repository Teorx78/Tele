Un codice di Hamming ha le colonne della [[Decodifica di codici lineari a blocco#Matrice di controllo parità|matrice generatrice di parità]] che sono tutte le sequenze lunghe $n-k$ bit prese una sola volta tranne la colonna nulla. 

Per un codice di Hamming si ha $2{n-k}-1 = n$
Si scrive dunque la matrice:
$\underline{\mathcal H} = \left(\begin{array}{c|cccccc}  \dots & 1 & 0 & \dots &\dots & 0 \\  \dots & 0 & 1 & 0 & \dots & 0 \\ \dots & \vdots & \dots & \ddots & \dots & \vdots \\ \dots & 0 & 0 & \dots & 1 & 0 \\ \dots & 0 & \dots & \dots & 0 & 1 \end{array}\right)$  quindi alla destra avrà $n-k$ colonne della matrice identità

##### Capacità correttive
La distanza minima di un qualsiasi codice di Hamming è $d_{min} = 3$. Questo permette di:
- trovare al massimo 2 errori
- correggre al massimo un errore

Il codice di Hamming soddisfa il [[Criteri di Decodifica#Bound di Hamming|bound di Hamming]] all'eguaglianza per $t=1$ , dove $t$ è il numero massimo di errori sempre corretti. Cioè non si tratta più di disuguaglianza nella proprietà del bound ma di vera e propria uguaglianza.



#codifica_di_canale 