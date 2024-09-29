Dados
$\theta = \{ w', b', ..., u,c\}$ los parametros de la red
$\mathcal{L} = \dfrac{1}{n}\sum error(\hat{y},y)$ una [[Funcion de error]]

Le aplicamos a cada termino de la funcion de la funcion de error una penalizacion
$\mathcal{L'} = \dfrac{1}{n}(\sum error(\hat{y},y) + \alpha \; penalty(\theta))$
$penalty_{L_2}(A) = sum(A^2)$ , donde A es una matriz y penalty(A) es un escalar 

Buscamos achicar el tamaño de los parametros para hacer el espacio de busqueda mas *narrow*


- Ridge y Lasso son exactamente lo mismo pero aplicado a la regresion lineal
- Vamos a usar regularizacion $L_2$

