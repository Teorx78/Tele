É un tipo di [[Modulazione M-arie|modulazione M-arie]]. 

Si consideri il segnale $s_n(t) = \alpha_{n,I} h_{Tx}(t) cos(2\pi f_0t) - \alpha_{n,Q} h_{Tx}(t) sin(2\pi f_0t)$
$I$ e $Q$ rappresentano le componenti dei coefficienti $\alpha_n$ , con $n=1,\dots,M$.

Dove $h_{Tx}(t)$ è la forma d'onda elementare trasmessa.  

$h_{Tx}(t) cos(2\pi f_0t) \, , \, h_{Tx}(t) sin(2\pi f_0t)$ sono [[Modulazione Binaria#Segnali Ortogonali|ortogonali]] con $T >> \frac{1}{f_0}$

Base ortonormale:
- $\phi_1(t)= \frac{h_{Tx}(t) cos(2\pi f_0t)}{\sqrt{\frac{E_{h_{Tx}}}{2}}}$
- $\phi_2(t)= -\frac{h_{Tx}(t) sin(2\pi f_0t)}{\sqrt{\frac{E_{h_{Tx}}}{2}}}$
In questo caso le [[Regioni di Decisione|regioni di decisione]] sono delimitate da $\phi_1$ e $\phi_2$

La costellazione è quindi rettangolare (in generale). Infatti $M=L^2$ , dove $L$ è il numero di livelli per ogni componente $I$ e $Q$. Inoltre il numero di bit per simbolo è  $2log_2L$
![[QAM.png]]

Si ha quindi che $d_{min}=\sqrt{2E_h}$

[[Energia di un Segnale|Energia Media]] : $E_s = \frac{M-1}{3}E_{h_{Tx}} = \frac{M-1}{3}\int_{-\infty}^{+\infty}|h_{Tx}(t)|^2 \, dt$

[[Modulazione Binaria#Probabilità d'errore|Probabilità d'errore]] : $P(E)=\frac{1}{M}\sum_{m=1}^{M}P(\vec r \notin \mathcal R_m|a_0=m)$

### Regioni di Angolo

SI hanno 3 tipologie:
- Tipo A $\Rightarrow 4$
- Tipo B $\Rightarrow 4(\sqrt M-2)$
- Tipo C $\Rightarrow M-4-4(\sqrt M -2)$
##### Tipo A - Regione centrale
- Si trova al centro della costellazione, tipico dei punti interni
- È delimitata soltanto da linee verticali/orizzontali → decisione basata quasi solo su valori di $I$ e $Q$, non sul loro angolo.
- Non ci sono lati che puntano verso l’origine.
$P(\vec r \notin \mathcal R_A|a_0=m (TIPO A)) = 1 - [1-Q(\frac{\sqrt{\frac{E_{h_{Tx}}}{2}}}{2\sigma^2_w})]^2$ 
##### Tipo B - Regioni Esterne diverse dal tipo A
- È a metà strada tra il centro e i bordi.
- Una parte della regione è delimitata da linee verticali/orizzontali (tipo A),
- ma una parte è delimitata da semirette che convergono nell’origine → decisione parzialmente angolare.
$P(\vec r \notin \mathcal R_B|a_0=m (TIPO B)) = 1 - (1-Q(\frac{\sqrt{\frac{E_{h_{Tx}}}{2}}}{2\sigma^2_w})(1-2Q(\frac{\sqrt{\frac{E_{h_{Tx}}}{2}}}{2\sigma^2_w}))$
##### Tipo C - Regioni interne
- Regione **esterna**, tipicamente ai bordi della costellazione, ancora più spesso negli angoli.
- Limitata da due linee che partono dall’origine, formando un cono (wedge).
- La decisione è completamente angolare: conta solo l'angolo del vettore ricevuto.
$P(\vec r \notin \mathcal R_C|a_0=m (TIPO C)) = 1-[1-2Q(\frac{\sqrt{\frac{E_{h_{Tx}}}{2}}}{2\sigma^2_w})]^2$

La probabilità d'errore diventa dunque : $P(E)=4(1-\frac{1}{\sqrt M})Q(\sqrt{\frac{E_s 3}{\sigma^2_w(M-1)2}})$

### Mappatura ai bit
Per ogni asse si usa la mappatura di Gray
![[mappatura_bitQAM.png]]

#modulazione 