<b>Final Validation accuracy for Base Network:<br>
Accuracy on test data is:</b> <br>
<b>83.34</b>

<h3>Model definition (model.add... ) with output channel size and receptive field</h>

model = Sequential()
model.add(SeparableConv2D(48, kernel_size=(3,3), input_shape=(32, 32, 3))) #30X30X48 #RF=3X3
model.add(BatchNormalization())
#model.add(Convolution2D(48, 3, 3, , input_shape=(32, 32, 3)))
model.add(Activation('relu'))

model.add(SeparableConv2D(48, kernel_size=(3,3))) #28X28X48 #RF=5X5
model.add(BatchNormalization())
#model.add(Convolution2D(48, 3, 3))
model.add(Activation('relu'))

model.add(MaxPooling2D(pool_size=(2, 2))) #14X14X48 #RF=6X6
model.add(Dropout(0.25))

model.add(SeparableConv2D(96, kernel_size=(3,3), border_mode='same')) #14X14X96 #RF=10X10
model.add(BatchNormalization())
#model.add(Convolution2D(96, 3, 3, border_mode='same'))
model.add(Activation('relu'))

model.add(SeparableConv2D(96, kernel_size=(3,3))) #12X12X96 #RF=14X14
model.add(BatchNormalization())
#model.add(Convolution2D(96, 3, 3))
model.add(Activation('relu'))


model.add(MaxPooling2D(pool_size=(2, 2))) #6X6X96 #RF=16X16
model.add(Dropout(0.25))

model.add(SeparableConv2D(192, kernel_size=(3,3), border_mode='same')) #6X6X192 #RF=24X24
model.add(BatchNormalization())
#model.add(Convolution2D(192, 3, 3, border_mode='same'))
model.add(Activation('relu'))

model.add(SeparableConv2D(192, kernel_size=(3,3))) #4X4X192 #RF=32X32
model.add(BatchNormalization())
#model.add(Convolution2D(192, 3, 3))
model.add(Activation('relu'))

model.add(MaxPooling2D(pool_size=(2, 2))) #2X2X192 #RF=36X36
model.add(Dropout(0.25))

model.add(SeparableConv2D(num_classes,kernel_size=(2,2))) #1X1X10 #RF=44X44
model.add(Flatten())

model.add(Activation('softmax'))

<b>50 epoch logs:</b> </br>
Epoch 1/50
390/390 [==============================] - 30s 76ms/step - loss: 1.4527 - acc: 0.4782 - val_loss: 1.2126 - val_acc: 0.5647
Epoch 2/50
390/390 [==============================] - 28s 72ms/step - loss: 1.1111 - acc: 0.6022 - val_loss: 1.3880 - val_acc: 0.5239
Epoch 3/50
390/390 [==============================] - 28s 71ms/step - loss: 0.9823 - acc: 0.6511 - val_loss: 1.2030 - val_acc: 0.6008
Epoch 4/50
390/390 [==============================] - 28s 72ms/step - loss: 0.8989 - acc: 0.6818 - val_loss: 0.8591 - val_acc: 0.6941
Epoch 5/50
390/390 [==============================] - 28s 71ms/step - loss: 0.8374 - acc: 0.7047 - val_loss: 1.3850 - val_acc: 0.5941
Epoch 6/50
390/390 [==============================] - 28s 72ms/step - loss: 0.7973 - acc: 0.7202 - val_loss: 0.8138 - val_acc: 0.7175
Epoch 7/50
390/390 [==============================] - 28s 72ms/step - loss: 0.7611 - acc: 0.7337 - val_loss: 0.8042 - val_acc: 0.7217
Epoch 8/50
390/390 [==============================] - 28s 72ms/step - loss: 0.7326 - acc: 0.7436 - val_loss: 0.7775 - val_acc: 0.7305
Epoch 9/50
390/390 [==============================] - 28s 72ms/step - loss: 0.7081 - acc: 0.7513 - val_loss: 0.7410 - val_acc: 0.7460
Epoch 10/50
390/390 [==============================] - 28s 72ms/step - loss: 0.6913 - acc: 0.7571 - val_loss: 1.3077 - val_acc: 0.5924
Epoch 11/50
390/390 [==============================] - 28s 71ms/step - loss: 0.6716 - acc: 0.7653 - val_loss: 0.8207 - val_acc: 0.7186
Epoch 12/50
390/390 [==============================] - 28s 71ms/step - loss: 0.6537 - acc: 0.7691 - val_loss: 0.6772 - val_acc: 0.7656
Epoch 13/50
390/390 [==============================] - 28s 72ms/step - loss: 0.6368 - acc: 0.7774 - val_loss: 0.6586 - val_acc: 0.7775
Epoch 14/50
390/390 [==============================] - 28s 72ms/step - loss: 0.6261 - acc: 0.7820 - val_loss: 0.6282 - val_acc: 0.7811
Epoch 15/50
390/390 [==============================] - 28s 72ms/step - loss: 0.6129 - acc: 0.7868 - val_loss: 0.6869 - val_acc: 0.7658
Epoch 16/50
390/390 [==============================] - 28s 71ms/step - loss: 0.6023 - acc: 0.7890 - val_loss: 0.7043 - val_acc: 0.7609
Epoch 17/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5897 - acc: 0.7963 - val_loss: 0.6762 - val_acc: 0.7786
Epoch 18/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5811 - acc: 0.7974 - val_loss: 0.5904 - val_acc: 0.7958
Epoch 19/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5740 - acc: 0.8003 - val_loss: 0.6361 - val_acc: 0.7900
Epoch 20/50
390/390 [==============================] - 28s 71ms/step - loss: 0.5636 - acc: 0.8019 - val_loss: 0.5864 - val_acc: 0.8017
Epoch 21/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5581 - acc: 0.8026 - val_loss: 0.6258 - val_acc: 0.7905
Epoch 22/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5497 - acc: 0.8101 - val_loss: 0.5809 - val_acc: 0.8071
Epoch 23/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5423 - acc: 0.8109 - val_loss: 0.5855 - val_acc: 0.8025
Epoch 24/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5380 - acc: 0.8118 - val_loss: 0.6062 - val_acc: 0.8011
Epoch 25/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5277 - acc: 0.8153 - val_loss: 0.5845 - val_acc: 0.7957
Epoch 26/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5280 - acc: 0.8161 - val_loss: 0.6082 - val_acc: 0.7946
Epoch 27/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5167 - acc: 0.8186 - val_loss: 0.6018 - val_acc: 0.8032
Epoch 28/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5132 - acc: 0.8210 - val_loss: 0.6756 - val_acc: 0.7855
Epoch 29/50
390/390 [==============================] - 28s 72ms/step - loss: 0.5063 - acc: 0.8226 - val_loss: 0.6339 - val_acc: 0.7877
Epoch 30/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4983 - acc: 0.8240 - val_loss: 0.5459 - val_acc: 0.8149
Epoch 31/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4972 - acc: 0.8257 - val_loss: 0.5587 - val_acc: 0.8101
Epoch 32/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4907 - acc: 0.8279 - val_loss: 0.5683 - val_acc: 0.8069
Epoch 33/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4882 - acc: 0.8274 - val_loss: 0.5647 - val_acc: 0.8089
Epoch 34/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4820 - acc: 0.8312 - val_loss: 0.5654 - val_acc: 0.8118
Epoch 35/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4737 - acc: 0.8322 - val_loss: 0.5807 - val_acc: 0.8070
Epoch 36/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4748 - acc: 0.8334 - val_loss: 0.6140 - val_acc: 0.7985
Epoch 37/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4690 - acc: 0.8358 - val_loss: 0.7034 - val_acc: 0.7736
Epoch 38/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4702 - acc: 0.8343 - val_loss: 0.5743 - val_acc: 0.8115
Epoch 39/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4617 - acc: 0.8387 - val_loss: 0.6186 - val_acc: 0.7935
Epoch 40/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4616 - acc: 0.8376 - val_loss: 0.5518 - val_acc: 0.8135
Epoch 41/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4592 - acc: 0.8382 - val_loss: 0.5771 - val_acc: 0.8048
Epoch 42/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4513 - acc: 0.8415 - val_loss: 0.5046 - val_acc: 0.8361
Epoch 43/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4463 - acc: 0.8434 - val_loss: 0.5279 - val_acc: 0.8249
Epoch 44/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4470 - acc: 0.8429 - val_loss: 0.5408 - val_acc: 0.8235
Epoch 45/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4419 - acc: 0.8442 - val_loss: 0.5374 - val_acc: 0.8214
Epoch 46/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4419 - acc: 0.8456 - val_loss: 0.5281 - val_acc: 0.8235
Epoch 47/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4337 - acc: 0.8482 - val_loss: 0.5702 - val_acc: 0.8134
Epoch 48/50
390/390 [==============================] - 28s 72ms/step - loss: 0.4353 - acc: 0.8472 - val_loss: 0.5262 - val_acc: 0.8242
Epoch 49/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4287 - acc: 0.8489 - val_loss: 0.4900 - val_acc: 0.8368
Epoch 50/50
390/390 [==============================] - 28s 71ms/step - loss: 0.4268 - acc: 0.8496 - val_loss: 0.4921 - val_acc: 0.8334
Model took 1398.90 seconds to train
