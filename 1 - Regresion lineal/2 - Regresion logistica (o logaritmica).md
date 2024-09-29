#clase #ai 
## Clasificacion
Dado un conjunto de variables cualitativas $\mathcal{C}$ : Podemos tomar un vector de features $X$ y una respuesta $Y \in \mathcal{C}$  $\rightarrow C(X) \in \mathcal{C}$ 

### Usando regrasion lineal
Si la usamos para una salida binaria, el resultado suele ser bueno. se llama **linear discriminant analysis**, pero en algunos casos diferentes, puede dar probabilidades < 0 o > 1, por lo que usamos regresion logistica.

### Fiteo de regresion logistica
Usamos *maximum likelihood*

