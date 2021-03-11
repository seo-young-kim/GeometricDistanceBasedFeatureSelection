# Geomteric Distance Based Feature Selection with SFS

---

# Summary of Paper.

Lee, J. H., & Oh, S. Y. (2016).
Feature selection based on geometric distance for high-dimensional data. Electronics Letters, 52(6), 473-475.

### Distance measurement method of Feature subset

![equ3](https://user-images.githubusercontent.com/49013650/110815880-2de83a80-82ce-11eb-803c-e236b53ef36a.png)

### A. Inter-class distance : $D_B(X_Q)$

![figure1](https://user-images.githubusercontent.com/49013650/110815881-2de83a80-82ce-11eb-871e-1c628aa4e9b7.png)
[figure1] 

![figure2](https://user-images.githubusercontent.com/49013650/110815882-2e80d100-82ce-11eb-8beb-e56e62e2c15a.png)

figure1을 참고해보았을때, 클래스 중심간 거리가 멀수록, 그리고 클래스 내부 분산이 작을 수록 쉽게 분류할 수 있을거라 예상할 수 있다.

따라서 클래스 중심간 거리 - 클래스 내부분산 을 측정한다. (equation1.)

![equ1](https://user-images.githubusercontent.com/49013650/110815873-2c1e7700-82ce-11eb-9429-a850fa531b73.png)

equation 1. inter-class distance

### B. Eveness of Inter-class distances

![figure3](https://user-images.githubusercontent.com/49013650/110815885-2e80d100-82ce-11eb-842a-8e5e22fa907a.png)

class의 거리들이 균등할 수록, 쉽게 분류할수 있으리라 예상된다.

이에 균등도를 측정한다.(equation2)

![equ2](https://user-images.githubusercontent.com/49013650/110815878-2d4fa400-82ce-11eb-892e-d72bec9d5ad7.png)

equation2. Eveness of inter-class distances

# Implementation with SFS(Sequential Forward Selection)

SFS방식을 사용해 gdbfs값이 최대인 feature subset을 선정했다.

![figure4](https://user-images.githubusercontent.com/49013650/110815888-2f196780-82ce-11eb-8338-04a5195b42ea.png)

출처 - [https://www.cc.gatech.edu/~bboots3/CS4641-Fall2018/Lecture16/16_FeatureSelection.pdf](https://www.cc.gatech.edu/~bboots3/CS4641-Fall2018/Lecture16/16_FeatureSelection.pdf)

https://user-images.githubusercontent.com/49013650/110815889-2fb1fe00-82ce-11eb-985d-6272e5c783d1.mp4

