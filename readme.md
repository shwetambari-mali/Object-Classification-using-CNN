
## Cifar10 Tensorflow Project

### Get Started
- environment: `tensorflow-gpu1.8+cude9.0`
- datasets from kaggle : [CIFAR-10 - Object Recognition in Images](https://www.kaggle.com/c/cifar-10/data), first you can download the train and test dataset.
- then use the `utils/get_data_list.py` and `utils/get_dataset_mean.py` scripts to generate `train.txt` and `val.txt`.


## The optimization process

- run scripts `tools/trian_cifar10.py` **include adjust lr , add data augmentation ,add dropout ,weight decay,stack 3*3 conv training tricks. you can learn how train model acc from 70%+ to 91+%**, while add model depth through `conv4_1 and conv4_2` it can not imporve val acc.
![](https://github.com/ranjiewwen/TF_cifar10/blob/master/doc/image/base_val_acc.png)
- run scripts `tools/trian_cifar10_v2.py` include add batch_norm, we can see it make the training more unstable, maybe it not imporve val acc, while stack 3*3 conv it can improve val acc remarkable.
![](https://github.com/ranjiewwen/TF_cifar10/blob/master/doc/image/v2_val_acc.png)
- run scripts `tools/fintune_cifar10.py`. it frist load imagenet pretrain weights and then finetune resnet50.

