Train on 60000 samples, validate on 10000 samples Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003. 60000/60000 [==============================] - 24s 400us/step - loss: 0.1741 - acc: 0.9436 - val_loss: 0.0487 - val_acc: 0.9842 Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0557 - acc: 0.9828 - val_loss: 0.0473 - val_acc: 0.9853 Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018. 60000/60000 [==============================] - 7s 113us/step - loss: 0.0436 - acc: 0.9869 - val_loss: 0.0323 - val_acc: 0.9894 Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0357 - acc: 0.9887 - val_loss: 0.0303 - val_acc: 0.9906 Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0318 - acc: 0.9899 - val_loss: 0.0245 - val_acc: 0.9921 Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0284 - acc: 0.9907 - val_loss: 0.0266 - val_acc: 0.9932 Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127. 60000/60000 [==============================] - 7s 114us/step - loss: 0.0278 - acc: 0.9912 - val_loss: 0.0221 - val_acc: 0.9934 Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307. 60000/60000 [==============================] - 7s 113us/step - loss: 0.0238 - acc: 0.9925 - val_loss: 0.0222 - val_acc: 0.9922 Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0220 - acc: 0.9928 - val_loss: 0.0230 - val_acc: 0.9928 Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0215 - acc: 0.9928 - val_loss: 0.0230 - val_acc: 0.9928 Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0191 - acc: 0.9942 - val_loss: 0.0220 - val_acc: 0.9930 Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0185 - acc: 0.9941 - val_loss: 0.0202 - val_acc: 0.9942 Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0171 - acc: 0.9944 - val_loss: 0.0217 - val_acc: 0.9932 Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638. 60000/60000 [==============================] - 7s 109us/step - loss: 0.0167 - acc: 0.9946 - val_loss: 0.0200 - val_acc: 0.9939 Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0164 - acc: 0.9944 - val_loss: 0.0198 - val_acc: 0.9938 Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0158 - acc: 0.9947 - val_loss: 0.0205 - val_acc: 0.9936 Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0138 - acc: 0.9955 - val_loss: 0.0208 - val_acc: 0.9938 Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0146 - acc: 0.9953 - val_loss: 0.0213 - val_acc: 0.9940 Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0131 - acc: 0.9953 - val_loss: 0.0215 - val_acc: 0.9936 Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869. 60000/60000 [==============================] - 7s 114us/step - loss: 0.0135 - acc: 0.9956 - val_loss: 0.0193 - val_acc: 0.9941

model.evaluate(on test data)[0.01932154694770652, 0.9941]

Summary
The accuracy of validation set is 99.41(>99.4).

For removing the bias we used "bias=False" in each layer.

Reduce the kernels from 32 to just 10 or 16 so parameter will be less than 15k.

Reduce the value of dropout to obtain validation accuracy above 99.4%.


Group
Arpit Gupta , Rishabh Sharma.
