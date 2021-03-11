# Geomteric Distance Based Feature Selection with SFS

---

# Summary of Paper.

Lee, J. H., & Oh, S. Y. (2016).
Feature selection based on geometric distance for high-dimensional data. Electronics Letters, 52(6), 473-475.

### Distance measurement method of Feature subset

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7082bb7-feed-49ae-a36e-664202ab4004/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7082bb7-feed-49ae-a36e-664202ab4004/Untitled.png)

### A. Inter-class distance : $D_B(X_Q)$

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3b61fa8-9658-416b-8734-254abd1f138b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3b61fa8-9658-416b-8734-254abd1f138b/Untitled.png)

[figure1] 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/05bc75fc-3e58-4a2f-9677-8a8e415fb219/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/05bc75fc-3e58-4a2f-9677-8a8e415fb219/Untitled.png)

figure1을 참고해보았을때, 클래스 중심간 거리가 멀수록, 그리고 클래스 내부 분산이 작을 수록 쉽게 분류할 수 있을거라 예상할 수 있다.

따라서 클래스 중심간 거리 - 클래스 내부분산 을 측정한다. (equation1.)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8eea30e0-f85d-45bf-aed2-9a7a5e2a8532/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8eea30e0-f85d-45bf-aed2-9a7a5e2a8532/Untitled.png)

equation 1. inter-class distance

### B. Eveness of Inter-class distances

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7f274ff-d8ab-4e41-b63d-be9f20658590/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7f274ff-d8ab-4e41-b63d-be9f20658590/Untitled.png)

class의 거리들이 균등할 수록, 쉽게 분류할수 있으리라 예상된다.

이에 균등도를 측정한다.(equation2)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/928afc9d-37c5-48db-83f4-0a023c15ad71/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/928afc9d-37c5-48db-83f4-0a023c15ad71/Untitled.png)

equation2. Eveness of inter-class distances

# Implementation with SFS(Sequential Forward Selection)

SFS방식을 사용해 gdbfs값이 최대인 feature subset을 선정했다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4f5e0dcb-dfb7-48fa-8ddc-8510363ba6a4/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4f5e0dcb-dfb7-48fa-8ddc-8510363ba6a4/Untitled.png)

출처 - [https://www.cc.gatech.edu/~bboots3/CS4641-Fall2018/Lecture16/16_FeatureSelection.pdf](https://www.cc.gatech.edu/~bboots3/CS4641-Fall2018/Lecture16/16_FeatureSelection.pdf)

[https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c0abd664-7fb3-4c74-a95c-81f788a68850/hhhhh_(online-video-cutter.com)_(1).mp4](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c0abd664-7fb3-4c74-a95c-81f788a68850/hhhhh_(online-video-cutter.com)_(1).mp4)
