# CIFAR-10 homework

### Usage 

simply run the cmd for the training:

```bash
## 1 GPU for base model 

CUDA_VISIBLE_DEVICES=0 python -u train.py --work-path ./experiments/cifar10/densenet120bc

## 1 GPU for base model with cutout

CUDA_VISIBLE_DEVICES=0 python -u train.py --work-path ./experiments/cutout/densenet120bc

## 1 GPU for base model with mixup
CUDA_VISIBLE_DEVICES=0 python -u train.py --work-path ./experiments/mixup/densenet120bc

## 1 GPU for base model with cutout+mixup
CUDA_VISIBLE_DEVICES=0 python -u train.py --work-path ./experiments/cutout+mixup+cos/densenet120bc

## 2 GPU for large model

CUDA_VISIBLE_DEVICES=0,1 python -u train.py --work-path ./experiments/cutout+mixup+cos/densenet150bc
```
I use yaml file ``config.yaml`` to save the parameters, check any files in `./experimets` for more details.  
You can see the training curve via tensorboard, ``tensorboard --logdir path-to-event --port your-port``.  
The training log will be dumped via logging, check ``log.txt`` in your work path.




## Acknowledgement
This is code is heavily borrowed from \url{https://github.com/BIGBALLON/CIFAR-ZOO}


