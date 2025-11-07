AWGN : Additive White Gaussian Noise. Trasmette di bit su un sistema di comunicazione analogico.

### Trasformazione fatta dal canale AWGN
$r(t)=A*s_{T_X}(t-t_0)+w(t)$ , dove:
- $A*s_{T_X}(t-t_0)$ e $w(t)$ sono dei [[Segnali]]
- $A$ rappresenta l'ampiezza e smorza il segnale se $<1$
-  $t_0$ è il ritardo
- $A*s_{T_X}(t-t_0)$ è il segnale utile. Il solo $s_{T_X}(t-t_0)$ rappresenta il segnale trasmesso
- $w(t)$ rappresenta il rumore. Il rumore è una [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|Variabile aleatoria Gaussiana]] con media nulla e una certa varianza. $w(t_i)$ e $w(t_j)$, con $t_i \neq t_j$ sono v.a. indipendenti, poiché il rumore attuale è diverso da quello passato. $w(t)=\mathcal N(0,\sigma^2)$
- $r(t)$ segnale ricevuto

### [[Energia di un Segnale|Energia]] del segnale utile e rumore

Definiamo il valore medio dell'energia del segnale utile con il [[Ripasso Probabilità#Valore Atteso|Valore Atteso]] dove la v.a. è il bit che trasmetto (consideriamo il caso di trasmissione di un bit, con un segnale per lo $0$ e uno per l'$1$):
$E[E_{{As}_{TX}}]=P(bit=0)*A^2E_{s0}+P(bit=1)*A^2E_{s1}$

Per i rumore:
$E[E_w]=E[\int_0^Tw^2(t) \, dt]=\sigma^2T$ 

#segnali 