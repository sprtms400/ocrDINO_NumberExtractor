## 마라톤, 자전거 대회 사진에서의 배번표 검출기
마라톤, 자전거 대회 사진에서 배번표의 번호를 추출하는 프로그램입니다.
Grounding DINO 를 이용하여 이미지에 대하여 segmentation을 진행하고 전처리 후 easyOCR을 이용하여 번호정보를 획득합니다.
![image](https://github.com/sprtms400/ocrDINO_NumberExtractor/assets/26298389/e157fdf9-2e86-480e-b495-0f242ef19c1c)


## 개발된 환경 및 구성

OS : Ubuntu 20.04

Python version : 3.10
``` 
conda create <project-name> python=3.10
```
의존 패키지 설치
```
pip install
```

해당 프로젝트 구동을 위해서는 CUDA 환경이 필요합니다. CUDA가 설치되어있고 CUDA_HOME 환경변수가 설정 되어있다는 가정 하에 GroundingDINO 설치합니다.
Installation:

1.Clone the GroundingDINO repository from GitHub.

```
git clone https://github.com/IDEA-Research/GroundingDINO.git
```

다운로드된 GroundingDINO 저장소 디렉토리로 이동합니다.

```
cd GroundingDINO/
```

해당 디렉토리에서 Grounding DINO를 설치합니다.


weight파일 다운로드
```
wget -q https://github.com/IDEA-Research/GroundingDINO/releases/download/v0.1.0-alpha/groundingdino_swint_ogc.pth
```
weight파일을 프로젝트에 포함시키기
```
mkdir segementation/weights
mv groundingdino_swint_ogc.pth segementation/weights/
```

### 마라톤, 그란폰도 대회 이미지 검색 서비스에서의 담당부분
![image](https://github.com/sprtms400/ocrDINO_NumberExtractor/assets/26298389/735db180-18c0-46ae-b431-ac28083485e5)
본 리포지터리에서는 마라톤, 그란폰도 대회 이미지 검색 서비스에서 녹색 박스에 해당된 부분을 담당합니다. 프로젝트에 대한 자세한 설명은
다음 저장소를 확인하세요.
https://github.com/sprtms400/Granfondo_Photo_Search/tree/main
