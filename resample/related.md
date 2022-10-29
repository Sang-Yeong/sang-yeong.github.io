---
layout: page
title: Related Work
description: >
  관련연구를 통해 다양한 방법론들을 분석한다.
sitemap: false
---

1. toc 
{:toc .large-only}

## ManTra-Net: Manipulation Tracing Network for Detection and Localization of Image Forgeries With Anomalous Features
> Wu, Yue, Wael AbdAlmageed, and Premkumar Natarajan. "Mantra-net: Manipulation tracing network for detection and localization of image forgeries with anomalous features." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2019.

### Abstract
- 다른 유형과 결합된 조작을 포함하는 이미지 위조에 대항하기 위해 ManTra-Net 아키텍처를 제안
- 추가 preprocessing and postprocessing 없이 detection and localization를 모두 수행하는 end-to-end network
- contributions
	- self-supervised learning task → classifying 385 image manipulation types
	- design a Z-score feature to capture local anomaly & propose a novel long short-term memory solution
	- carefully conduct ablation experiments


### ManTra-Net
- image forgery localization/detection (IFLD)를 위함.
	- localization: 모델이 주어진 이미지 안의 Object 가 이미지 안의 어느 위치에 있는지 위치 정보를 출력해주는 것
- local anomalous features를 식별 → detects forged pixels
- ⇒ not limited to a specific forgery or manipulation type
- end-to-end solution이기 때문에 pre- and/or post-processing을 할 필요 없음.

### ManTra-Net 개요

<img src='/assets/img/resample/0919-mantra_archi.png' height='30'>

- 2개의 sub-networks로 구성
	- unified(통합된) feature representation을 생성하는 the image manipulation-trace feature extractor
	- directly localizing forgery regions without post-processing 하는 the local anomaly(변칙) detection network (LADN)
		- adaptation: anomaly detection task에 대한 manipulation trace feature 적용
		- anomalous feature extraction: (human thinking에 영감 받아서) extracts anomalous features
		- decision: anomalous features(변칙적 특징)을 종합적으로 고려 & 픽셀이 위조되었는지 여부 분류







<br>

---

해당 포스트는 아래를 참고하여 작성되었습니다.

- [ManTra-Net] <https://openaccess.thecvf.com/content_CVPR_2019/html/Wu_ManTra-Net_Manipulation_Tracing_Network_for_Detection_and_Localization_of_Image_CVPR_2019_paper.html>