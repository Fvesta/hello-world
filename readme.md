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
| `static` | 유형(기준) 없음 / 배치 불가능 | `static` |
| `relative` | 요소 자신을 기준으로 배치 |  |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 |  |
| `fixed` | 브라우저 창을 기준으로 배치 |  |

값 | 의미 | 기본값
---|:---:|---:
`static` | 유형(기준) 없음 / 배치 불가능 | `static`
`relative` | 요소 **자신**을 기준으로 배치 |
`absolute` | 위치 상 **_부모_(조상)요소**를 기준으로 배치 |
`fixed` | **브라우저 창**을 기준으로 배치 |
