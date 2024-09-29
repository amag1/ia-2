#clase #ai 
$$Y = \beta_0 + \beta_1 X + \epsilon$$
$\beta_0$ = intercept
$\beta_1$ = slope

Cada $X$ es una variable. El default y visualizable es con una variable pero se puede extender a N variables
Esos son valores reales, vamos a inferirlos con el modelo
$$\hat{y} = \hat{\beta_0} + \hat{\beta_1}X$$
Donde $\hat{\beta_0}$ y B1 son estimaciones.

### Least squares
Minimiza el error cuadrado. El de metodos numericos

$$RSS = (y_1-\hat{\beta_0}-\hat{\beta_1}x_1)^2+(y_2-\hat{\beta_0}-\hat{\beta_2}x_2)^2+...+(y_n-\hat{\beta_0}-\hat{\beta_n}x_n)^2$$

Se ve asi ![asi](Slides-3.pdf#page=10)

### Gradient descent
Lo va a dar el Jorch

### Intervalo de confianza
Probabilidad de que, para cierto dato desconocido, el intervalo contenga a ese dato

### Hipotesis nula
Partir de hipotesis y mostrar que no es verdadera
$H_0:$ No hay relacion entre X e Y -> $H_0: \beta_1 = 0$
$H_A$: Hay relacion entre X e Y -> $H_0: \beta_1 \neq 0$

#### Tests
- Para testear la hipotesis nula, computamos una *t-statistic* que crea una distribucion *t*. Nos da un **valor p**. Si $p \lessapprox 5\%$ se rechaza la hipotesis nula
- **Residual sum of squares**: $RSS = \sum_{i=1}^n(y_i - \hat{y_i})^2$
- **Residual standard error**: $RSE = \sqrt{\dfrac{1}{n-2}RSS}$ 
- **Total sum of squares**: $TSS = \sum_{i=1}^n(y_i - \bar{y_i})^2$ donde $\bar{y_i}$ es la media
- **R-squared**: $R^2 = \dfrac{TSS-RSS}{TSS} = 1 - \dfrac{RSS}{TSS}$. Buscamos que sea cercano a 1
- **MSE** = $\dfrac{RSS}{n}$ o $Var(\theta) + Bias(\theta)^2$ 


### Correlacion
Lo ideal es que las variables no esten correlacionadas (pueda ser estimada y testeada por separado)
- La varianza de todos los coeficientes suele aumentar
- Las interpretaciones son mas peligrosas -> cuando una variable cambia, todas las demas cambian

Un coeficiente de regresion $B_j$ estima el cambio esperado en $Y$ por cambio en $X_j$, suponiendo que todos los demas coeficientes quedan fijos. Pero, por lo general, **todos cambian juntos!** 

> Esencialmente, todos los modelos estan equivocados, pero algunos son utiles

## Regresion
La salida es un numero

## Consideraciones en la salida
$R^2$: Nos dice cuanto mejor que la media es nuestro modelo y tambien nos habla de la varianza de la distribucion
