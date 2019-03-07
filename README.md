# 4YP -  Learning to Segment Using Overlap Score

This repository is a heavily modified version of the code in [pytorch-semseg](https://github.com/meetshah1995/pytorch-semseg) which is used to explore the potential of IoU score as a learning objective.
I will only detail the information that cannot be found in the original [README.md](https://github.com/HMellor/4YP/blob/master/pytorch-semseg/README.md) to save writing it twice.

## Changes to original code
### Loss functions
Since the IoU surrogate I am working towards is highly non differentiable, I implemented all loss functions in hinge loss form to lower the number of variables when comparing the methods.

There are three loss functions explored are as follows:
  - Micro-average
  - Macro-average
  - SVM IoU from a previous 4YP (TODO - cite Zehan)
### Networks
I used an FCN version of AlexNet because it's small size meant I could run experiments in quick succession to validate code.

## Usage
Launch [visdom](https://github.com/facebookresearch/visdom#launch) by running (in a separate terminal window):
```
visdom
```
Train the model like this:
```
python train.py [-h] [-lr LR] [-wd WD] [-sp SP] [-n [NAME]] [-e] [config]
```
Where each of the arguments are defined as follows:
```
positional arguments:
  config                path of configuration file to use

optional arguments:
  -h, --help            show this help message and exit
  -lr LR, --learning_rate LR
                        learning rate to use
  -wd WD, --weight_decay WD
                        weight decay to use
  -sp SP, --superpixels SP
                        how many superpixels to use
  -n [NAME], --name [NAME]
                        name to give the experiment output directory
  -e, --evaluate        causes prediction/image pairs to be saved for later
                        evaluation
```
