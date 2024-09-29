#math #ai 
Son teoremas de la siguiente forma:

> *Dada una familia de redes neuronales, para cada funcion $f$ de cierto [[Espacio de funciones|espacio de funciones]] existe una secuencia de RN $\phi_1, \phi_2, ...,\phi_n$ de la familia tal que $\phi_k \rightarrow f$ de acuerdo con algun criterio*

Esto quiere decir que la familia de redes neuronales es **densa** en ese espacio de funciones
Por lo tanto: **se puede usar una RN para computar cualquier cosa**

## Ejemplo Sigmoid
Sea $F: [0,1]^k \rightarrow [0,1]$ 
Para todo $e$ existen $W, b, U$ tales que $F(a) = sig(x W + b) \cdot U$  y ademas se verifica $| f(x) - F(a) | < e$, para todo $x \in [0,1]^k$ 

En otras palabras, para toda funcion arbitraria, existe una RN que la aproxima

