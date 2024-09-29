> Entrenar con peso

De manera random (con una probabilidad $i$) apagar una neurona de la capa $==$ ponerla en 0
Lo hacemos diferente con cada batch

A la hora de usar la red neuronal entrenada, prendemos todas las neuronas

Matematicamente, la salida de una capa pasa a ser $$h^{(i)} = F(h^{(i-1)} \cdot W^i + b^i) \cdot \mu^i$$
Donde $\mu$ es una **mascara** para cada capa -> vector donde cada componente puede ser 0 o 1 dependiendo de una probabilidad **que tambien es un hiperparametro**