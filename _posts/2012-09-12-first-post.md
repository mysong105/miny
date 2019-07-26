---
title: 리눅스 환경설정 
author: M.Y.
layout: post
---

### for gpu user  

예를 들어  
`
python test.py 
`

```python
import tensorflow as tf
import cv2
import numpy as np 
```


목표 : ubuntu 위 python + python packages(PIL,numpy,scipy,tensorflow-gpu...) + CUDA + CUDNN  
이때 각 패키지 사이 버전 충돌이 주 문제이며, 버전을 미리 맞춰서 깔아야 한다. 
나의 경우 ubuntu 및 pip  python 설치 되어있는 서버를 이용했다.

1) 우분투 버전 확인
`$ cat /etc/issue`  
`Ubuntu 16.04.5 LTS \n \l`    

2) GPU 확인 


`$ nvidia-smi`

GPU종류에 따라 compute capability 를 확인하여 CUDA를 설치 ($sudo)
https://developer.nvidia.com/cuda-gpus  


설치 후 확인  
'apt --installed list'

나의 경우   
`CUDA 10  
CUDNN 7
python3'  


2) python packages(PIL,numpy,scipy,tensorflow-gpu...)
pip 이라는 설치 도구로 편리하게 install 가능  
하지만, 버전 문제 해결을 간편하게 하기 위해 venv 로 가상 환경을 설정 후 설치 하자 

아래 가이드가 잘 나와 있다.
https://www.tensorflow.org/install/pip



