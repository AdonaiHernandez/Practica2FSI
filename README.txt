 Practica2FSI

El objetivo de este modelo es clasificar imagenes segun el deporte que se está practicando. Cuenta con 100 deportes distintos (100 labels).
El rendimiento conseguido es de un 0.75 de val_acuracity.

El dataset que uso es:

https://www.kaggle.com/datasets/gpiosenka/sports-classification

Uso tecnicas de data augmentation y de dropout para intentar esquivar en lo posible en overfitting.

El modelo tiene una red notablemente densa:

_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_20 (Conv2D)          (None, 222, 222, 64)      1792      
                                                                 
 conv2d_21 (Conv2D)          (None, 220, 220, 64)      36928     
                                                                 
 max_pooling2d_8 (MaxPoolin  (None, 110, 110, 64)      0         
 g2D)                                                            
                                                                 
 dropout_12 (Dropout)        (None, 110, 110, 64)      0         
                                                                 
 conv2d_22 (Conv2D)          (None, 108, 108, 128)     73856     
                                                                 
 conv2d_23 (Conv2D)          (None, 106, 106, 128)     147584    
                                                                 
 max_pooling2d_9 (MaxPoolin  (None, 53, 53, 128)       0         
 g2D)                                                            
                                                                 
 dropout_13 (Dropout)        (None, 53, 53, 128)       0         
                                                                 
 conv2d_24 (Conv2D)          (None, 51, 51, 256)       295168    
                                                                 
 conv2d_25 (Conv2D)          (None, 49, 49, 256)       590080    
...
Total params: 76946852 (293.53 MB)
Trainable params: 76946852 (293.53 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
