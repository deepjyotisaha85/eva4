Final Validation Accuracy: 99.22%

Model:
Total params: 18,988
Learning Rate:0.001
Batch Size: 64
Architecture:
* No FC Layer used
* Used BN, Dropout, Maxpooling
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 16, 26, 26]             160
       BatchNorm2d-2           [-1, 16, 26, 26]              32
            Conv2d-3           [-1, 16, 24, 24]           2,320
       BatchNorm2d-4           [-1, 16, 24, 24]              32
            Conv2d-5           [-1, 32, 22, 22]           4,640
       BatchNorm2d-6           [-1, 32, 22, 22]              64
         Dropout2d-7           [-1, 32, 22, 22]               0
         MaxPool2d-8           [-1, 32, 11, 11]               0
            Conv2d-9             [-1, 16, 9, 9]           4,624
      BatchNorm2d-10             [-1, 16, 9, 9]              32
           Conv2d-11             [-1, 16, 7, 7]           2,320
      BatchNorm2d-12             [-1, 16, 7, 7]              32
           Conv2d-13             [-1, 16, 5, 5]           2,320
      BatchNorm2d-14             [-1, 16, 5, 5]              32
        Dropout2d-15             [-1, 16, 5, 5]               0
           Conv2d-16             [-1, 10, 3, 3]           1,450
      BatchNorm2d-17             [-1, 10, 3, 3]              20
           Conv2d-18             [-1, 10, 1, 1]             910
================================================================


