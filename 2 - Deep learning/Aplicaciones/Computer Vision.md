Las redes neuronales **densas** (standard) aprenden patrones globales

Necesitamos usar [[CNN]] para aprender patrones mas complejos (translation invariance)

### Image segmentation
Los pixels en cada mascara pueden tomar uno de tres valores enteros:
1. Foreground
2. Background
3. Contour

Como nos interesa mucho la ubicacion de la imagen en el espacio, usamos [[Stride (CNN)]] em lugar de [[Pooling]] para llevar a cabo la compresion

En el caso de image segmentation, la idea es que nuestro modelo tenga una prediccion por cada pixel -> para esto, vamos achicando la imagen con las capas convolucionales

Luego, necesitamos agrandarla. Para esto usamos [[Transposed Convolution]] layers, que multiplican cada valor por el kernel para volver a agrandar la imagen

