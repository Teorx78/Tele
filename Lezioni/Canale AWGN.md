AWGN : Additive White Gaussian Noise. Trasmette di bit su un sistema di comunicazione analogico.

### Trasformazione fatta dal canale AWGN
$r(t)=A*s_{TX}(t-t_0)+w(t)$ , dove:
- $A*s_{TX}(t-t_0)$ e $w(t)$ sono dei segnali
- $A$ rappresenta l'ampiezza e smorza il segnale se $<1$
-  $t_0$ è il ritardo
- $A*s_{TX}(t-t_0)$ è il segnale utile. Il solo $s_{TX}(t-t_0)$ rappresenta il segnale trasmesso
- $w(t)$ rappresenta il rumore. Il rumore è una [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|Variabile aleatoria Gaussiana]] con media nulla e una certa varianza. $w(t_i)$ e $w(t_j)$, con $t_i \neq t_j$ sono v.a. indipendenti, poiché il rumore attuale è diverso da quello passato
- $r(t)$ segnale ricevuto

