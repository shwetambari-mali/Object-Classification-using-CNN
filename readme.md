
## Cifar10 Tensorflow Project

### Get Started
- environment: `tensorflow-gpu1.8+cude9.0`
- datasets from kaggle : [CIFAR-10 - Object Recognition in Images](https://www.kaggle.com/c/cifar-10/data), first you can download the train and test dataset.
- then use the `utils/get_data_list.py` and `utils/get_dataset_mean.py` scripts to generate `train.txt` and `val.txt`.


## The optimization process

- run scripts `tools/trian_cifar10.py` **include adjust lr , add data augmentation ,add dropout ,weight decay,stack 3*3 conv training tricks. we can train model acc from 70%+ to 91+%**, but we notice that adding model depth through `conv4_1 and conv4_2` cannot imporve val acc.
<img width="532" alt="base_val_acc" src="https://user-images.githubusercontent.com/111578613/185714005-6b586538-a424-425b-be0a-0dda09895786.png">
