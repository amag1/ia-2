#ai #math 
Encuentra el optimo local

Dado $\theta$ random, let $\theta = \theta - \lambda \dfrac{dL}{d\theta}$ 

**Problemas**:
- Hallar un buen $\lambda$ -> hyperparameter tuning
- Calcular la derivada es costoso -> usamos [[Backpropagation]]
## Algoritmo
1. Calcular el gradiente de la *loss function* (derivadas parciales con respecto a cada variable)
2. Elegr $\theta$ random
3. Calcular $\nabla(\theta)$ 
4. Calcular Step size = $\lambda \cdot \nabla(\theta)$ 
5. Actualizar lambda

> Neurons that fire together, wire together

- A veces, el error despues de un batch es mayor que en el anterior. Esto puede pasar si $\lambda$ es muy grande