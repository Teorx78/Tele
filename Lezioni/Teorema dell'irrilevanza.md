
Considerando un segnale su [[Canale AWGN|canale AWGN]]: $r(t) = s_{a_0}(t) + w(t) + w_\perp(t)$, per il teorema posso non considerare $w_\perp(t)$

$f_{r_2|r_{1,a_0}}(\rho_2|\rho_1,n) = f_{r_2|r_1}(\rho_2|\rho_1)$

Dove:
- $r_1$ : segnale inviato, quindi $= s_{a_0} + w_{\phi}$
- $r_2$ : parte ortogonale del rumore, quindi $= w_\perp$
- $f_{r_2|r_{1,a_0}}(\rho_2|\rho_1,n)$: [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|densità di probabilità]] della parte ortogonale di $r_2$ dato che ho osservato $r_1=\rho_1$ e $a_0=n$
- $f_{r_2|r_1}(\rho_2|\rho_1)$ : [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|densità di probabilità]] della parte ortogonale di $r_2$ dato che ho osservato $r_1=\rho_1$

Va ad indicare che la distribuzione statistica di $r_2$ non dipende dal simbolo trasmesso. Che io trasmetta $s_1(t)$ o $s_n(t)$ la distribuzione di $r_2$ rimane la stessa.
#modulazione