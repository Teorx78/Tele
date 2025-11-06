Dividere lo spazio euclideo di dimensione $I$ in $M$ regioni di decisione per cui ogni vettore $\vec r \in R^I$ cade i una e una sola di queste regioni.

Se $\mathcal R_m$ (indico con $R$ l'insieme dei reali e con $\mathcal R$ il simbolo di regione), con $m \in [1,\dots,M]$ è la regione $m$-esima $\mathcal R \subseteq R^I$ :
$\bigcup_{m=1}^M\mathcal R_m=R^I$ e si ha $\mathcal R_i \cap \mathcal R_j=0$ per $i \neq j$

![[Regioni di Decisione.png]]

### Progetto delle Regioni
Ricordo $f$ [[Ripasso Probabilità#Variabile Aleatoria Gaussiana|densità]] di una v.a.

Obiettivo: massimizzare la probabilità di decisione corretta:
$maxP(\hat a_0=a_0)$ , con $a_0$ simbolo trasmesso al tempo $0$, $\hat a_0$ decisione in merito al simbolo trasmesso al tempo $0$.

### Probabilità di decisione corretta
$P(\hat a_0=a_0)=\sum_{m=1}^MP(\hat a_0=a_0 | a_0=m)*P(a_0=m)$ , con:
- $P(\hat a_0=a_0 | a_0=m)$ : canale + ricevitore
- $P(a_0=m)$ : trasmettitore, con $a_0 \rightarrow max$

$\Rightarrow P(\hat a_0=a_0) = \sum_{m=1}^{M} \int_{\mathcal R_m} P_{a_0}(m)*P_{\vec r|a_0}(\vec b|m) d\vec b$, dove: $P_{a_0}(m)*P_{\vec r|a_0}(\vec b|m) = \mathcal D(\vec b, m)_{max}$ che è definita come la funzione di probabilità per la determinazione della regione di decisione ottimale.

![[Probabilità di decisone corretta.png]]

Basta quindi integrare ogni $\mathcal D$ per ottenere le aree e poi sommarle per avere la probabilità di decisione corretta.

Ora per massimizzarla mi basterà associare ad ogni $\vec r$ la regione di regione $m$ con $\hat a_0=m$ , che ha il valore massimo di $D(\vec r, i)$ 
$\Rightarrow \hat a_0 = arg_mmaxD(\vec r,m)$ , con $m \in [1,\dots,M]$

### Criteri di Decisione
Definiamo $\vec r = \vec \rho$
##### MAP
Maximum A Posteriori
$\hat a_0 = arg_mmaxf_{r|a_0}(m|\vec\rho)$
È il caso generale, quindi viene usato quando a priori si hanno simboli con probabilità diversa
##### ML
Maximum Likehood
$\hat a_0 = arg_mmaxf_{r|a_0}(\vec\rho|m)$
Si usa quando i simboli sono equiprobabili
##### MD
Minimum Distance
$\hat a_0 = arg_mmin||\vec\rho-\vec s_m||^2=arg_mmin\ d(\vec\rho, \vec s_m)$
Si usa quando i simboli sono equiprobabili e siamo in presenza di rumore. Infatti si ha ha: $\vec r = \vec s_m + \vec w$

### Costruzione delle Regioni di decisione
Si tratta di trovare il punto medio dei segmenti che congiungono i segnali che compongono la costellazione

![[2.png]]
![[3.png]]
![[4.png]]
