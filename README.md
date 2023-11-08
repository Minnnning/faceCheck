# readme

하르케스케이드의 기본 모델을 이용한 얼굴인식 카메라 입니다

모델은 https://github.com/opencv/opencv/tree/master/data/haarcascades 이곳의 모델을 사용했고

코드는 공대선배 유튜브를 참고 했습니다



## 하르 케스케이드

<center>
<img src="https://github.com/Minnnning/minnnning.github.io/assets/80758613/07a12306-f94f-4f6c-94cb-578e8eb4ef20" style="zoom:50%;">
</center>

이와 같은 features 모형을 이용해서 같은 색 부분의 픽셀 밝기의 합과 어두운 부분으로 겹쳐진곳의 픽셀 밝기 합 차이를 이용해서 얼굴의 특정 패턴을 인식해서 사람을 특정하는 방법이다

<center>
<img src="https://github.com/Minnnning/minnnning.github.io/assets/80758613/5d740eb4-cfe2-4db1-82bc-c27b7279117d" style="zoom:50%;">
</center>

위 사진 처럼 features를 얼굴 사진에 넣어 해당 사진의 픽셀들의 밝기 차이를 이용한다 눈과 눈썹 사이는 특정한 밝기 차이가 존재하고 코와 양 쪽 광대 사이에도 밝기 차이가 존재한다 이런 특징들 몇가지가 동시에 한 부분에서 나타난다면 해당 부분은 얼굴이라고 판단하는 것이다 이런 원리로 얼굴을 판단한다 하지만 이 속에는 **Integral Images**(적분을 통해서 픽셀들의 밝기의 합을 빠르게 구함), **Adaboost** **Training**(밝기 차이를 이용해서 특정 패턴을 찾아냄) 이런 복잡한 과정이 있고 이것이 모두 코드의 haarcascade_frontalface_default.xml에 포함되어 있어 쉽게 사용할 수 있다

 

<center>
<img src="https://github.com/Minnnning/minnnning.github.io/assets/80758613/4072e390-a636-4969-b37b-2b09b6dbec80" style="zoom:30%;">
</center>

테스트 결과
