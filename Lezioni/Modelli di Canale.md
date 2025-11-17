Dato un [[Canale AWGN|AWGN]] $r(t) = As_{Tx}(t) + w(t)$
Dal [[Rapporto Segnale-Rumore|SNR]] sappiamo che $(A^2)_{dB} = 10log_{10}A^2 \Rightarrow \frac{E_r}{E_{s_{tx}}} = A^2$
- se $A>1$ parliamo di guadagno
- se $A < 1$ parliamo di attenuazione

### Trasmissione su cavo elettrico
![[Cavo Elettrico.png]]

Indichiamo con $l$ la lunghezza del cavo (nell'esempio: $2.2$Km). Ad ogni ampiezza $A$ il segnale cambia, nell'esempio:
- dopo il primo $A$ avremo $r_1(t) = As_{Tx}(t)$
- dopo il secondo avremo: $r_2(t) = Ar_1(t) = A^2 s_{Tx}(t)$

Il rumore viene aggiunto solo al ricevitore.

Il fattore moltiplicativo dei segnali complessivo è dato da $G=A^l$
Mentre il fattore di attenuazione $a=\frac{1}{A}$
Attenuazione totale: $(a^2_{TOT})_{dB}= l*(\hat a^2)_{\frac{dB}{Km}}$, dove $(\hat a^2)_{\frac{dB}{Km}} = 10log_{10}a^2$ è l'attenuazione per Km in dB 

##### Cavi in rame
Per i cavi in rame l'attenuazione complessiva di un cavo (in Km) dipende dalla frequenza: $(a^2)_{dB}= (\hat a^2_{ch})_{\frac{dB}{Km}}*\sqrt{\frac{f}{f_0}}*l$ , con $(\hat a^2_{ch})_{\frac{dB}{Km}}$ attenuazione rispetto alla frequenza $f_0$ di riferimento

##### Fibra Ottica
Stesso modello con $(a^2)_{dB}=(\hat a^2)_{\frac{dB}{Km}}*l$ , con $(\hat a^2)_{\frac{dB}{Km}} = 0.2$. Ad esempio per un Km di fibra avrò 0.2 di attenuazione

##### Canale Radio
Formato da un'antenna ricevente con area $A_{Ant,Tx}$ , con densità di [[Energia di un Segnale#Potenza|potenza]] ad una distanza $d$ dal trasmettitore è: $\Phi = \frac{P_{Tx}}{4\pi d^2} = [\frac{W}{m^2}]$

Si utilizza l'antenna direttiva per ricevere una maggiore potenza $\rightarrow$ c'è un guadagno in potenza $\delta_{Ant,Tx} \Rightarrow P_{Rx}=\Phi A_{Ant,Rx} \delta_{Ant,Tx}$

Possiamo riscrivere il guadagno in funzione dell'area:  $\delta = \frac{4\pi A}{\lambda^2}\mu_{Ant,Rx}$ , con $\lambda$ lunghezza onda e $\mu_{Ant,Rx}$ efficienza dell'antenna

$(a)_{dB} = (\frac{P_{Tx}}{P_{Rx}})_{dB} = 32.4+20lo_{10}(d)_{km} + 20 log_{10}(f)_{MHz} - \delta_{Ant,Tx}-\delta_{Ant,Rx}$
#canale