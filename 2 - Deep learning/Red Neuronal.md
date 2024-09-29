#clase #ai
Tiene una capa de entrada, una o mas hidden layers y una capa de salida
Cada elemento en una capa es un [[Perceptron]]

Por lo general, se usa una [[Funcion de activacion]] para las capas de entrada y ocultas, y otra para la funcion de salida

Gracias al [[Universal Approximation Theorem]] se sabe que podemos aproximar cualquier funcion con una red neuronal
![[Pasted image 20240825112227.png]]
## Componentes
Estos componentes están directamente relacionados a la [[Model Architecture]]
### Pesos
Es una matriz W

### Bias
Vector b. Se le aplica una funcion de [[Tensores#Broadcasting|broadcast]] para trabajar con tensores 

### Matriz U
Pesos de la ultima capa?

### c
Bias de la ultima capa

Por lo tanto $\mathcal{L}(W,b,U,c)$
La salida de la red neuronal puede 
- Un escalar (para el caso de clasificacion binaria o regresion) -> usamos [[Sigmoid]].
	- En el caso de la clasificacion, si la salida es un numero != 0 o 1, usamos un valor de **threshold** para redondear.
- O una distribucion de probabilidad (para el caso de clasificacion no binaria) -> [[Softmax]]
## Definicion
$$h^{(i)} = F^{(i)}(h^{(i-1)}W^{(i)} + b^{(i)})$$
$$y = G(h^{(i)}U + c)$$

Donde:
- h es el resultado de la capa anterior
- W son los pesos en una capa especifica
- F y G son funciones de activacion
- b es un bias externo
- c es el bias de la capa de salida
- U son los pesos de la capa de salida

## Entrenamiento
La salida de una red es una **distribucion de probabilidad** -> buscamos minimizar la [[Funcion de error]].
Entrenar es encontrar los parametros que minimizan el error
- La tecnica que mas se usa es [[Gradient descent]]

Si quisieramos entrenar de a "1 iteracion", podriamos usar algebra matricial. Para procesar de a lotes, necesitamos del [[Tensores|algebra tensorial]]

Tiene dos objetivos
1. Disminuir error de entrenamiento
2. Minimizar diferencia entre *err_Train* y *err_Test*

## Generalizacion
Buscamos que la red siga funcionando bien aun cuando le paso datos que no ha visto.

- **Error de generalizacion**: Error de la RN para datos no vistos = error en test vs error en train
- **Metricas**: estimadores para saber como anda mi red

Buscamos minimizar la diferencia entre el *train error* y el *test error*
1. Disminuir *train_error* -> si no lo hacemos tenemos [[Underfitting]]
	1. Podemos solucionarlo con mas datos -> [[Augmentation]]
	2. Podemos agrandar la red
2. Minimizar diferencia entre train y test error -> [[Overfitting]]
	1. Podemos disminuir el tamaño de la red

![[Pasted image 20240902184800.png]]

## Hiperparametros
Tuneo de hiperparametros que no estan relacionados a la red *per se*
- Learning rate $\lambda$
- Arquitectura de la red (cantidad y tamaño de las capas)
- Optimizador

Train -> **buscar parametros** *(weights, bias)*
Test -> **obtener [[Metricas|metricas]] que evaluan error de generalizacion**

Podemos dividir el conjunto de train en **validation** y train. Con este conjunto podemos tunear hiperparametros.
## Regularizacion
**Conjunto de tecnicas para evitar overfitting**
### Tecnicas
- [[Penalizacion del tamaño de parametros]]
- [[Ensemble]]
- [[Stacking]]
- [[Bootstrap]]
- [[Dropout]]
- [[Inverted Dropout]]
- [[Early Stopping]]
