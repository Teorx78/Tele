Permette il passaggio:
Segnale Digitale $\rightarrow$ Segnale Analogico $\rightarrow$ Segnale Digitale

Serve per far si che il segnale digitale al ricevitore, avrà un prob di rumore minore.

### Trasmettitore Digitale
Una sequenza di $l$ bit (inviati ad intervalli $T_b$) entra nel bit mapper, che associa ad ogni sequenza di bit un simbolo, quindi la nuova sequenza di $n$ simboli entra (ad intervalli $T$) nel modulatore. In uscita i avrà un segnale $s_{TX}(t)$. Dove:
$s_{TX}(t)=\sum_{n=-\infty}^{+\infty}s_{a_n}(t-nT)$

### Canale trasmissivo
Il segnale ricevuto può essere:
- Ideale: $r(t) = s_{T_X}(t)$
- AWGN: r(t) = $As_{T_X}(t) + w(t)$
- Multi cammino: $r(t) = \sum_{k=1}^NA_k*s_{T_X}(t) + w(t)$ rappresenta gli echi, ovvero la possibilità che il segnale arrivi al ricevitore in più percorsi, quindi si generano più copie. Quindi viene effettuata una [[Segnali#Somma di segnali|somma tra i segnali]]. Il multi cammino ha 2 effetti:
	  - Le singole forme d'onda trasmesse vengono modificate dal cammino
	  - Interferenza inter-simbolica: le trasmissioni di simboli vicini si disturbano.

### Ricevitore Digitale
Al ricevitore troviamo la situazione inverse al Trasmettitore. Un segnale $r(t)$ entra nel [[Demodulazione Digitale|demulatore digitale]] che dovrà scegliere quale forma d'onda è stata trasmessa sulla base del segnale ricevuto. Dunque produce sequenze di segnali $\hat a_n$ , che entrano nel bit demapper producendo una sequenza di $\hat b_l$. Con $\hat a_n \neq a_n$ e $\hat b_l \neq b_l$, poiché sono versione ricostruite.

#modulazione