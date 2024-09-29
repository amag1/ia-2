La red mantiene un estado interno y se va retroalimentando.
En cada capa, la salida se calcula como $f(\text{input}, \text{estado\_interno})$ . Originalmente el estado interno vale cero

Esta red neuronal tiene dos matrices de pesos (W y U) y un vector de bias. Por lo tanto, la salida en una capa es
`activation(dot(W,input) +  dot(U, state) + b)`

> **En resumen**, una RNN es un bucle `for` que reutiliza salidas computadas en la iteración anterior


En la práctica, las RNN tienen algunos problemas, por lo que usamos [[LSTM]]

## Técnicas avanzadas
### Recurrent Dropout
Es diferente al [[Dropout]] tradicional. 
Se vuelve mucho más complicado porque la misma máscara de dropout se debería usar para cada instante en el tiempo -> si desconectáramos cosas al azar, estaríamos perdiendo la información temporal.