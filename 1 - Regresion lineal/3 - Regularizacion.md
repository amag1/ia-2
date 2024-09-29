#clase #ai
Como encontrar coeficientes de regresion lineal si tenemos muchas features?

### Subset selection
Es la solucion naive. Tomar todas las combinaciones de features y entrenar un modelo. Tomar el mejor.

No sirve porque overfitea y el espacio de busqueda es de $2^n$

## Ridge regression
Linear regression fitting: $RSS = \sum_{i=1}^n(y_i - \hat{y_i})^2$
Ridge regression fitting: $RSS + \lambda \sum_{j=1}^p\beta_j^2$, donde $\lambda$ es un parametro de tuneo

Si $\lambda = 0$, el termino no tiene efecto
Si $\lambda \rightarrow \infty$ el impacto crece y los coeficientes tienden a cero

### Estandarizacion de predictores

### Tradeoff de varianza y sesgo
$$E(y_0-\hat{f}(x_0))^2 = Var(\hat f(x_0)) + [Bias(\hat f(x_0))]^2 + Var(\epsilon)$$

Sesgo: distancia de $\hat y$ a $y$
Varianza: dada por los intervalos de confianza

A medida que $\lambda$ aumenta, aumenta el sesgo y baja la varianza. Una explicacion es que, como los $\beta$ tienen a cero, se parecen mucho y por lo tanto la varianza baja

## The Lasso
Lasso fitting = $RSS + \lambda \sum_{j=1}^p \vert \beta_j \vert$ 
Cambiando de la norma L2 a la norma L1, lo que obtenemos es **feature selection**. Se eliminan las features innecesarias

## Comparacion entre Lasso y Ridge
Ninguna domina a la otra. Se usan en situaciones distintas.
Lasso es mejor cuando no todas las variables son importantes, pero por lo general no podemos saberlo a priori.

Por lo general corremos ambos y asi inferimos mas info del problema

