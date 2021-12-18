# BiO-Net

Paper: https://arxiv.org/abs/2007.00243

## Data

**Please refer to the official website (or project repo) for license and terms of usage.**
**We preprocessed the data for adaptating our data loaders. Please find the links below.**

**MoNuSeg**

- Official Website: https://monuseg.grand-challenge.org/Data/
- Baidu Disk: https://pan.baidu.com/s/1tqDzX52v8GYWXF4YfUGu1Q password: dqsr
- Google Drive: https://drive.google.com/file/d/1j7vEoq6YCBNKMoOZKPSQNciHZkVzkxGD/view?usp=sharing

**TNBC**

- Official Repo: https://github.com/PeterJackNaylor/DRFNS
- Baidu Disk: https://pan.baidu.com/s/1zPWTYAEffX55c2eyb3cU0Q password: zsl1
- Google Drive: https://drive.google.com/file/d/1RYY7vE0LAHSTQXvLx41civNRZvl-2hnJ/view?usp=sharing


## Usage  

Use ```--backend``` to switch between backends [keras, pytorch], default=keras.

**Train**
```
python3 main.py --epochs 300 --iter 3 --integrate --train_data PATH_TO_TRAIN_DATA_ROOT \
		  --valid_data PATH_TO_VALID_DATA_ROOT --exp 1 --backend YOUR_BACKEND
```

**Evaluate**

*Save metrics and segmentations:*
```
python3 main.py --evaluate_only --save_result --valid_data PATH_TO_VALID_DATA_ROOT --exp 1  --backend YOUR_BACKEND
```
*Print metrics only:*
```
python3 main.py --evaluate_only --valid_data PATH_TO_VALID_DATA_ROOT --exp 1  --backend YOUR_BACKEND
```
*NOTE:* ```--iter```,```--integrate```,```--multiplier``` need to be specidied on the above commands.

or
```
python3 main.py --evaluate_only --valid_data PATH_TO_VALID_DATA_ROOT --model_path PATH_TO_TRAINED_MODEL  --backend YOUR_BACKEND
```
