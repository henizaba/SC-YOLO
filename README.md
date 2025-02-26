# SC-YOLO
A model for detecting the maturity of tomato fruits

## Requirements
- Python 3.7+
- PyTorch 1.7.1+ 
- CUDA 10.2+
- OpenCV
- NumPy

### Training Steps
#### 1. Data Preparation
- Prepare VOC-format dataset
- Place RGB images in `VOCdevkit/VOC2007/JPEGImages`
- Place annotation files in `VOCdevkit/VOC2007/TXT`

#### 2. Data Preprocessing
Modify parameters in `splitDataset.py` and run:
```python
python splitDataset_mul.py
```

#### 3. Modify path
Modify the dataset paths in the yolov8.yaml file (ultralytics/cfg/datasets/yolov8.yaml)
- train: /path/to/your/train_dataset  
- val: /path/to/your/val_dataset    
- test: /path/to/your/test_dataset  

#### 4. Start Training
```python
python train.py
```

### Val
1. Modify model path in `val.py`
2. Run prediction script:
```python
python val.py
```

## Predict
### VOC Dataset Evaluation
1. Modify model path path in `predict.py`
2. Run evaluation script:
```python
python predict.py
```
