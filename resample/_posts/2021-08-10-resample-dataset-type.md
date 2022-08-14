---
layout: post
title: Dataset-종류
description: >
  선행연구에서 사용한 데이터셋 살펴보기
image: /assets/img/resample/0810-dataset-main.png
sitemap: false
---

# Dataset-선행연구에서 사용한 Dataset 분석하기

> 선행연구에서 사용한 데이터셋 중 8가지를 뽑아서 분석한다. 멀티미디어 포렌식에서 주로 다루는 데이터셋을 살펴볼 수 있다.

## 1. Dresden Image Database
(현재 다운로드 불가능)

<img src='/assets/img/resample/0810-dataset-dresden.png'>

- 출처식별용 database
- 다양한 실내 및 실외 장면의 14,000개 이상의 이미지 ← 73개의 디지털 카메라에서 control되고 광범위하게 비교할 수 있는 조건에서 수집.
- 장치별 특성과 모델별 특성 분리 & 25개의 서로 다른 모델에서만 카메라를 가져옴.
- 기기별 센서 노이즈 패턴 추정을 위한 보조영상을 카메라별로 수집함.
- 모델별 JPEG 압축 알고리즘을 연구하기 위한 또 다른 이미지 하위 집합이 각 모델에 대해 컴파일됨.


## 2. The Kaggle Camera Model Identification(KCMI) dataset

<img src='/assets/img/resample/0810-dataset-kcmi.png'>

- 이미지를 촬영한 카메라를 식별
- 이미지에 본질적으로 남겨진 흔적을 사용하여 이미지를 캡처한 카메라 모델을 식별하는 알고리즘을 구축하기 위해 사용된 dataset

- 데이터 수집 방법
	- training set(10개의 카메라 x 275장)
        - 모델당 단일 장치인 10개의 서로 다른 카메라 모델로 캡처
        - 카메라 모델
            - Sony NEX-7
            - Motorola Moto X
            - Motorola Nexus 6
            - Motorola DROID MAXX ...
        - 각 장치에서 275개의 전체 이미지 촬영

	- test set(2640장)
		- 동일한 10개의 카메라 모델로 캡처되었지만 두 번째 장치를 사용
		- == test 데이터의 이미지는 train 데이터와 동일한 장치로 촬영X
		- iPhone 6에 대한 기차 데이터의 이미지가 Ben Hamner의 장치(카메라 1)로 촬영된 경우 테스트 데이터의 이미지는 Ben Hamner의 두 번째 장치(카메라 2)로 촬영
		- center crop(512, 512)된 이미지
		- 절반은 조작된 이미지로 구성
		- 조작 method
			- JPEG compression with quality factor = 70
			- JPEG compression with quality factor = 90
			- resizing (via bicubic interpolation) by a factor of 0.5 ...



## 3. Splicing Dataset

<img src='/assets/img/resample/0810-dataset-splicing.png'>

Deep Matching and Validation Network -- An End-to-End Solution to Constrained Image Splicing Localization and Detection

- 기존 splicing 알고리즘의 문제점
	- subsequent processing (e.g., compression)에 robust하지 않은 handcrafted features를 사용
	- pipeline의 각 단계가 optimized independently
- 본 논문의 idea
	- two input images, a query image and a potential donor image 고려
	- donor img가 query이미지를 splice하는데 사용되었을 확률 추정
	- query and donor images에 대한 splicing masks 얻음.



## 4. Copy-Move Dataset

<img src='/assets/img/resample/0810-dataset-copymove.png'>

BusterNet: Detecting Copy-Move Image Forgery with Source/Target Localization


## 5. PhotoShop-battle dataset

<img src='/assets/img/resample/0810-dataset-photoshop.png'>

The PS-Battles Dataset - an Image Collection for Image Manipulation Detection
- PS-Battles dataset ← large community of image manipulation enthusiasts에서 수집
	- 11,142개의 하위 집합으로 그룹화된 102,028개의 이미지로 구성
각각은 원본 이미지와 다양한 수의 조작된 파생 상품을 포함



## 6. NIST16, Nimble Challenge 16(NC 2016)

- 이미지 및 비디오 포렌식 기술(이미지에서 조작의 영역과 유형을 결정하는 기술)
- Image Manipulation Detection and Localization
	- single probe image 주어지면 probe가 조작되었는지 감지하고 발견된 조작의 "type"과 시스템이 감지하도록 설계된 조작 유형을 나타내는 마스크를 제공
- Splice Detection and Localization
	- 두 개의 이미지가 주어지면 donor 이미지의 영역이 probe 이미지에 접합되었는지 감지



## 7. CASIA

<img src='/assets/img/resample/0810-dataset-casia.png'>

- CASI-A Image Tampering Detection Evaluation Database
- 사실적인 변조 작업을 통해 natural color 이미지 데이터베이스를 수집
- 변조 탐지 기술을 비교하고 평가를 위해 고안



## 8. COVERAGE

<img src='/assets/img/resample/0810-dataset-coverage.png'>

- 정품이 있는 원본을 포함
- 위조 원본 쌍
	- (i) 복제 및 위조 영역 마스크
	- (ii) 변조 요인/유사성 메트릭 주석으로 표시



<br>

---

해당 포스트는 아래를 참고하여 작성되었습니다.

- [Dresden] <https://www.researchgate.net/publication/220998815_The_Dresden_Image_Database_for_Benchmarking_Digital_Image_Forensics>

- [KCMI] <https://www.kaggle.com/c/sp-society-camera-model-identification>

- [Splicing Dataset] <https://arxiv.org/abs/1705.09765>

- [PhotoShop-battle dataset] <https://arxiv.org/abs/1804.04866>

- [NIST16] <https://mfc.nist.gov/>

- [CASIA] <https://www.kaggle.com/sophatvathana/casia-dataset>