# Classifying Medical Image Using Resnet 20

Run statistics: 

Train size: 47163

Valid size: 11791

Test: [0/737]   Time 0.961 (0.961)      Loss 0.0966 (0.0966)    Prec@1 93.750 (93.750)

Test: [50/737]  Time 0.302 (0.282)      Loss 0.0031 (0.0441)    Prec@1 100.000 (98.039)

Test: [100/737] Time 0.293 (0.292)      Loss 0.0885 (0.0402)    Prec@1 100.000 (98.329)

Test: [150/737] Time 0.340 (0.302)      Loss 0.0019 (0.0348)    Prec@1 100.000 (98.634)

Test: [200/737] Time 0.315 (0.306)      Loss 0.0019 (0.0367)    Prec@1 100.000 (98.601)

Test: [250/737] Time 0.329 (0.308)      Loss 0.0114 (0.0328)    Prec@1 100.000 (98.730)

Test: [300/737] Time 0.300 (0.309)      Loss 0.0056 (0.0306)    Prec@1 100.000 (98.796)

Test: [350/737] Time 0.359 (0.309)      Loss 0.2528 (0.0309)    Prec@1 93.750 (98.825)

Test: [400/737] Time 0.331 (0.311)      Loss 0.0074 (0.0293)    Prec@1 100.000 (98.893)

Test: [450/737] Time 0.330 (0.312)      Loss 0.0009 (0.0309)    Prec@1 100.000 (98.808)

Test: [500/737] Time 0.325 (0.314)      Loss 0.0010 (0.0304)    Prec@1 100.000 (98.827)

Test: [550/737] Time 0.303 (0.314)      Loss 0.0058 (0.0302)    Prec@1 100.000 (98.843)

Test: [600/737] Time 0.298 (0.314)      Loss 0.0021 (0.0294)    Prec@1 100.000 (98.856)

Test: [650/737] Time 0.305 (0.315)      Loss 0.0021 (0.0296)    Prec@1 100.000 (98.867)

Test: [700/737] Time 0.311 (0.315)      Loss 0.0017 (0.0298)    Prec@1 100.000 (98.850)

 * Prec@1 98.847
 

# How to run: 

## setup environment

python3 -m venv env

source env/bin/activate

pip3 install -r requirements.txt

## run model for evaluation

python3 -u trainer.py --resume result-model/model.th --evaluate --arch resnet20 --batch-size 128 --save-dir result


### my training commands: 

#### Split data:

run data_preprocessing.ipynb
#### train model:

python3 -u trainer.py --save-dir result-model --epochs 1 --arch resnet20 --lr 0.005


## reference
Resnet implementation: https://github.com/akamaster/pytorch_resnet_cifar10?tab=readme-ov-file 

Custom dataset: https://medium.com/dejunhuang/learning-day-32-training-resnet-with-own-dataset-in-pytorch-547aa9d8a07b 
