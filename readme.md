### Folder 구조
```
  └── Object_Detection     
              ├── Annotations
              │
              ├── JPEGImages
              │
              ├── JPEGImages_resized
              │
              ├── runs
              │
              ├── train_test.py
              │
              ├── test.py
              │
              └── readme.md
``` 

### 과제 진행률

test를 구현하지 못했습니다. 기존에 생각하던 test.py 구동방식은
```
$python test.py [image_path]
```
를 통해 object detection된 그림과 box를 그리는 방식이었는데, 만들지 못했습니다.
이에 그냥 model의 prediction과의 loss값을 계산하는 방식으로만 만들어 놓았습니다.
test.py를 직접 실행시킬 수 없으며, train_test.py를 실행시키면 test 결과까지
터미널에 출력해줍니다.

### train 및 test 명령어
```
#python train_test.py  <--- 윈도우에서 실행시켰을 때의 명령어입니다. 리눅스에서도 같은 방식으로 가능할 것 같습니다.
```
### hyperparameters

| 값 | 의미 | 기본값 |
|---|:---:|---:|
| `lrate` | 학습률 | `0.001` |
| `epochs` | 학습 반복 횟수 | `20` |
| `b_size` | mini-batch 사이즈 | `50` |
| `lambda_hasobj` | YOLO Loss계산 시 obj존재 가중치 | `5` |
| `lambda_noobj` | YOLO Loss계산 시 obj존재x 가중치 | `0.5` |
| `Seed` | random seed값 | `100` |
| `img_path` | 원본 이미지 파일 경로 | `./JPEGImages` |
| `ann_path` | annotation 파일 경로 | `./Annotations` |
| `img_resize_path` | resizing된 이미지 파일 경로 | `./JPEGImages_resized` |

그 외 값들
| 값 | 의미 | 기본값 |
|---|:---:|---:|
| `resizing된 img size` | 256 * 256 | |
| `transform img size` | 224 * 224 | |
| `pretrained model` | resnet | |
