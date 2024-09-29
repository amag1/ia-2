- Es un tipo de [[Red Neuronal]]. La diferencia esta en las operaciones que realizan las capas.
- Se usan para procesamiento de imagenes ([[IA 2/2 - Deep learning/Aplicaciones/Computer Vision|Computer Vision]])
- Aprenden patrones locales -> en el caso de imagenes, son pequeñas ventanitas 2D de la input
## Features
- *Translation invariance*
	- Como aprende patrones locales, podemos mover, rotar, cropear la imagen y las sigue clasificando correctamente

## Spatial hierarchies of patterns
La primera capa convolucional aprende cosas pequeñas (como bordes). Las capas subsiguientes aprenden patrones mas grandes obtenidos en las capas anteriores

## Arquitectura basica
**Feature extraction**
1. Input
2. [[Convolution]]
	1. La red se encarga de aprender los kernels de la convolucion
3. [[Pooling]]

**Classification**
4. Fully connected
5. Output

## Capas
Cada capa de una CNN hace lo siguiente
1. Convolucion
2. [[Pooling]]
3. [[Funcion de activacion]]
4. Bias

Por lo general, las capas mas profundas tienen una mayor cantidad de filtros (kernels). **A mayor cantidad de filtros, la red puede detectar mas abstracciones**.
## Conceptos caracteristicos
Se pueden modificar parametros extra de las capas convolucionales. Algunos de ellos son
- [[Padding (CNN)]]
- [[Stride (CNN)]]

## Soluciones a problemas comunes
- [[Residual connections]]
- [[Batch Normalization]]

