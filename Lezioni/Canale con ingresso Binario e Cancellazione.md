Consiste in un canale a ingresso ($x$) binario $\{b_l\} =\{0,1\}$ e uscita ($y$) ternaria $\{\hat b_l\} =\{0,1,E\}$ dove $E$ sta per "erasure" ovvero cancellazione. In pratica il canale non sbaglia mai simbolo, o lo si riceve corretto o lo si perde.

In pratica funziona in questo modo:

| $y$ \ $x$ | $0$           | $1$           |
| --------- | ------------- | ------------- |
| $0$       | $1-\alpha$    | $\varnothing$ |
| $1$       | $\varnothing$ | $1-\alpha$    |
| $E$       | $\alpha$      | $\alpha$      |
In pratica ricevo ciò che ho trasmesso con probabilità $1-\alpha$. Mentre con probabilità $\alpha$ ricevo $E$.

#capacità_canale 