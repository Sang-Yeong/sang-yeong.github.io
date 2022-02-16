---
layout: post
title: (cvpr2021) Spatial-Phase Shallow Learning_Rethinking Face Forgery Detection in Frequency Domain
description: >
  spatial domain, frequency domain, amplitude, phase, up-sampling  
image: /assets/img/review/01_spsl_main.png
sitemap: false
---


```
본 논문은 generative모델에서 forged image가 만들어질 때의 필수 과정인 up-sampling 흔적을 frequency domain에서의 phase spectrum을 통해 찾아낼 수 있음을 증명한다. 또한 high-level semantic information을 억제하고 local 부분에 집중 할 수 있도록 shallow learning 방법을 사용하는 SPSL method를 주장한다.
```

# Contributions
- Amplitude vs. Phase
	- Up-sampling artifacts를 phase spectrum을 통해 capture
	- 수학적 유도를 통해 CNN이 위조 탐지에 유용한 phase spectrum의 implicit features를 capture할 수 있음을 보임

- Global vs. Local
	- Shallow learning
	- CNN의 receptive field를 줄여서 검증


## Motivation
Facial manipulation 과정은 다음과 같이 3가지로 나누어 진다.

<!-- <img src='' fig1. Facial manipulation progress > -->

- Facial manipulation 과정
	1. encoding source face
	2. swapping face in latent space
	3. decoding target face

3번 decoding 과정에서 up-sampling이 필수적으로 적용된다. 이러한 up-sampling artifact는 frequency domain에서 찾아볼 수 있다.


## Amplitude vs. Phase
## Global vs. Local
# Limitation