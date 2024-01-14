Practica2FSI

El objetivo de este modelo es clasificar imagenes segun el deporte que se está practicando. Cuenta con 100 deportes distintos (100 labels).
El rendimiento conseguido es de un 0.75 de val_acuracity.

El dataset que uso es:

https://www.kaggle.com/datasets/gpiosenka/sports-classification

Las librerias usadas:

Tensorflow, Keras, PIL, numpy, skimage

Uso tecnicas de data augmentation y de dropout para intentar esquivar en lo posible en overfitting.

El modelo tiene una red notablemente densa:

_________________________________________________________________
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
                                                                 
 conv2d_26 (Conv2D)          (None, 47, 47, 256)       590080    
                                                                 
 max_pooling2d_10 (MaxPooli  (None, 23, 23, 256)       0         
 ng2D)                                                           
                                                                 
 dropout_14 (Dropout)        (None, 23, 23, 256)       0         
                                                                 
 conv2d_27 (Conv2D)          (None, 21, 21, 512)       1180160   
                                                                 
 conv2d_28 (Conv2D)          (None, 19, 19, 512)       2359808   
                                                                 
 conv2d_29 (Conv2D)          (None, 17, 17, 512)       2359808   
                                                                 
 max_pooling2d_11 (MaxPooli  (None, 8, 8, 512)         0         
 ng2D)                                                           
                                                                 
 dropout_15 (Dropout)        (None, 8, 8, 512)         0         
                                                                 
 flatten_2 (Flatten)         (None, 32768)             0         
                                                                 
 dense_6 (Dense)             (None, 2048)              67110912  
                                                                 
 dropout_16 (Dropout)        (None, 2048)              0         
                                                                 
 dense_7 (Dense)             (None, 1024)              2098176   
                                                                 
 dropout_17 (Dropout)        (None, 1024)              0         
                                                                 
 dense_8 (Dense)             (None, 100)               102500    
                                                                 
=================================================================
Total params: 76946852 (293.53 MB)
Trainable params: 76946852 (293.53 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
