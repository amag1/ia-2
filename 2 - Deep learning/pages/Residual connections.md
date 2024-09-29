Para resolver el [[Vanishing gradients problem]]. Fuerza a cada funcion en la cadena a mantener una version *noiseless* de la informacion del input anterior.
![[Pasted image 20240916194753.png]]
Hay que solucionar el problema de la diferencia de tamaños -> cuando pasamos un input por una capa convolucional, su tamaño cambia, asi que tambien necesitamos cambiar el tamaño del residuo para poder sumarlos

Un ejemplo es pasar el residuo por una capa convolucional con filtro de 1x1 para que coincidan las dimensiones sin modificar los datos.

[Articulo interesante](https://towardsdatascience.com/what-is-residual-connection-efb07cab0d55)



RNN