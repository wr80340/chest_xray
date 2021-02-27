# Chest X-Ray Images (Pneumonia)
## Introduction
Using deep learning model to detect and classify human diseases from medical images
## Link 
link : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
## 


## Baseline information

### Augmentation
- random crop
- adjust contrast
- adjust saturation
- adjust hue
- per image standardize
### Parameter information
- IMAGE_SIZE_CROPPED : 200  
- IMAGE_HEIGHT, IMAGE_WIDTH, IMAGE_DEPTH : 224,224,3  
- BATCH_SIZE : 16  
- LR : 1e-5  
- EPOCH : 50  
- REPEATS : 3  
- optimizer : tf.keras.optimizers.Adam(lr = LR)
- loss : tf.keras.losses.SparseCategoricalCrossentropy(reduction=tf.keras.losses.Reduction.SUM)
### Structure information
- pretrained weights : resnet 
- top : 3 dense layer with dropout and batch normalization
- 
## Results
method | training accuracy | validation accuracy | testing accuracy 
---|---|---|---
baseline| 0.98 | 0.95 | 0.75
no augment | 1.00 | 0.97 | 0.80
no standardize | 0.98 | 0.97 | 0.84
no dropout | 0.98 | 0.96 | 0.77
no batch norm | 0.99 | 0.96 | 0.84
## wandb 
https://wandb.ai/wr80340/chest_xray
