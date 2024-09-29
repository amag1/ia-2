#clase #ai 
Se pueden pensar como generelizaciones de las matrices a mas dimensiones (llamadas *axis*)
- 0D: escalar
- 1D: vector
- 2D: matriz

Un tensor esta definido por tres atributos
1. Numero de ejes (rango). Podemos obtenerlo con *ndim* en Numpy
2. Shape: tupla de enteros que dice cuantas dimensiones tiene
3. Data type
## Suma
Igual a la suma vectorial

## Producto escalar
Se puede generalizar para tensores de mas de una dimension

## Broadcasting
Para realizar operaciones entre tensores de diferente shape
Si quiero sumas un tensor x con shape (32,10) a uno y con shape (10,), lo que podemos hacer es repetir el tensor y 32 veces

## Producto tensorial
![[Pasted image 20240825113821.png]]
## Transpuesta
Solo bidimensional?

## Contraccion

## Derivada tensorial
Gradiente