# Start Yolov5

### Requirements

[requirements.txt](https://github.com/ultralytics/yolov5/blob/712de55a20cd584a12a4aebe96226c92f816dcf3/requirements.txt)


### Prepare Train Data

Yolov5 model requires YAML files.

1. Collect PNG or JPEG images
   
   * Size is usually 640x640 or 416x416 

2. Create Labels - [Roboflow](https://roboflow.com/)

3. Save the dateset as a YOLOv5 YAML file


### How to Use YOLOv5
1. [Prepare Data](#Train-Data)
2. Install YOLOv5: [Quick Start](https://github.com/ultralytics/yolov5?tab=readme-ov-file)
```
git clone https://github.com/ultralytics/yolov5
```

3. Train YOLOv5 - [train.py](https://github.com/ultralytics/yolov5/blob/712de55a20cd584a12a4aebe96226c92f816dcf3/train.py)
```
python train.py --img 640 --batch 16 --epochs 100 --data your_data.yaml --cfg models/yolov5s.yaml --weights '' --name your_model
``` 
* --img: 이미지 사이즈, 디폴트 640
* --batch: 배치 사이즈, 한 번에 모델이 학습하는 데이터 샘플의 수
* --epochs: 학습 에포크 수
* --data: 데이터셋에 대한 YAML 파일 경로
* --cfg: YOLOv5 구성 파일 경로
* --weights: 사전 학습된 모델 가중치 경로 (옵션)
* --name: 학습된 모델 이름

4. Model Evaluation: return accuracy - [val.py](https://github.com/ultralytics/yolov5/blob/712de55a20cd584a12a4aebe96226c92f816dcf3/val.py)
```
python val.py --data your_data.yaml --img 640 --weights runs/train/your_model/weights/best.pt
```
5. Inference - [detect.py](https://github.com/ultralytics/yolov5/blob/712de55a20cd584a12a4aebe96226c92f816dcf3/val.py)
```
python detect.py --source your_image_or_video.jpg --weights runs/train/your_model/weights/best.pt
```
* --source: 입력 이미지/영상의 경로
* --weights: 학습된 모델의 가중치 경로

