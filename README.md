# BiO-Net

Link to the official paper: https://arxiv.org/abs/2007.00243


## Datasets 

I have made use of the following dataset for the training and the evaluation purpose

**MoNuSeg**

- https://monuseg.grand-challenge.org/Data/

**TNBC**
- https://github.com/PeterJackNaylor/DRFNS

## Usage  


**For Training**

```
python3 main.py --epochs 300 --iter 3 --integrate --train_data PATH_TO_TRAIN_DATA_ROOT --valid_data PATH_TO_VALID_DATA_ROOT --exp 1 --backend YOUR_BACKEND
```

**For Evaluating**

```
python3 main.py --evaluate_only --save_result --valid_data PATH_TO_VALID_DATA_ROOT --exp 1  --backend YOUR_BACKEND
```
