Consideriamo un canale $M_ario$ senza memoria e periodo di simbolo $T$, avente [[Trasmissione di messaggi per la teoria dell'informazione#Capacità di un canale|capacità]] $C$. Sia $\{b_l\}$ una sorgente di simboli con [[Trasmissione di messaggi per la teoria dell'informazione#Tasso di informazione del canale|tasso di informazione]] nominale $R=\dfrac{log_2M_s}{T_s}$ dove $M_s$ è la cardinalità dell'alfabeto della sorgente e $T_s$ è il periodo di simbolo della sorgente. 
1) Se $R\leq C$ per ogni $\delta>0$  e ogni $n$ grande abbastanza, esistono:
	- un codice di canale con parole lunghe $n$ e numero di parole $2^{nRT}$ 
	- un decodificatore con probabilità di errore sulla parola inferiore a $\delta$
2) Se $R>C$ esiste un $\delta>0$ tale che ogni codice a correzione d'errore per questa sorgente e questo canale ha probabilità di errore sulla parole di codice $\geq \delta$

$c = max_{p_c}\dfrac{I_s(c;\widetilde{c})}{T}$  

Quando $M_s=M=2$ tutti i simboli sono binari.
Il codice è un insieme di $2^k$ parole lunghe $n$ e dal teorema $2^k=2^{nRT} \Rightarrow k=nRT$.
Quindi $\dfrac{k}{n}\leq CT$ e $\dfrac{k}{n} \leq max_pI_s(c;\widetilde{c})$ dove il termine a dx viene chiamato efficenza spettrale.

$I_s(c;\widetilde{c}) \leq min{H_s(c),H_s(\widetilde{c})}\leq 1$  bit

### Capacità del canale AWGN
$r_t = s_t + w_t$ con $w_t \sim \mathcal{N} (0, \sigma^2)$. Numeri reali ($I=1$).
$C=\dfrac{I}{2T}log_2(1+\dfrac{E_s}{\sigma^2})=max_{p_s}I_s(r;s)$ , con:
- $\dfrac{E_s}{\sigma^2}$ [[Rapporto Segnale-Rumore|SNR]] 
- $T$ periodo di simbolo
- $s \sim \mathcal N (0, E_s)$ [[Modulazioni Ortogonali e Biortogonali#Pulse Amplitude Modulation|PAM]] $M$ grande codice distribuzione gaussiana 

##### Capacità di un canale binario simmetrico senza memoria
Tempo di simbolo $T$ matrice di transizione del canale

| $b$ \ $\hat b$ | $0$         | $1$         |
| -------------- | ----------- | ----------- |
| $0$            | $1-P_{bit}$ | $P_{bit}$   |
| $1$            | $P_{bit}$   | $1-P_{bit}$ |

$c = max_{p_{\underline{b}}}\dfrac{I_s(\underline{b};\underline{\hat{b}})}{T}$  con canale senza memoria $\Rightarrow max_{p_b}\dfrac{I(b;\hat b)}{T}$ 

Si ha: $C = max_{p_b}\dfrac{1}{T}[H(\hat b)-H(\hat b|b)]$ dove devo scegliere $P_b$ che massimizza $H(\hat b)$ e:
$H(\hat b|b) = (1-P_{bit})log_2\dfrac{1}{1-P_{bit}} + P_{bit}log_2\dfrac{1}{P_{bit}}$

L'entropia max per $\hat b$: $1$ bit se $P_b(0)=P_b(1)=0.5$ e $P_{\hat b}(0)=P_{\hat b}(1)=0.5$

$C=\dfrac{1}{T}[1-P_{bit}log_2\dfrac{1}{P_{bit}}- (1-P_{bit})log_2\dfrac{1}{1-P_{bit}}]$   

#capacità_canale 