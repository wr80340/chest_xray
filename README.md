# chest_xray



## Basline information
### parameter information
- IMAGE_SIZE_CROPPED : 200  
- IMAGE_HEIGHT, IMAGE_WIDTH, IMAGE_DEPTH : 224,224,3  
- BATCH_SIZE : 16  
- LR : 1e-5  
- EPOCH : 50  
- REPEATS : 3  
- optimizer : tf.keras.optimizers.Adam(lr = LR)
- loss : tf.keras.losses.SparseCategoricalCrossentropy(reduction=tf.keras.losses.Reduction.SUM)
