# GeometricDistanceBasedFeatureSelection
It is a code that uses geometry measers to evaluate Feature subsets and to select optimal Feature subsets based on them.  
Feature subset's evaluation implements the 'Feature selection based on geometric distance for high-dimensional data.' introduced in the paper.  
__It can be used through 'pip install gdbfs'.  
Please refer to the Repository 'https://github.com/seo-young-kim/GDBFS_deploy' for details.__  
This page provides a brief description of the techniques.  

Reference 'Lee, J. H., & Oh, S. Y. (2016).
Feature selection based on geometric distance for high-dimensional data. Electronics Letters, 52(6), 473-475.'.  

## Distance measurement method of Feature subset
Feature subset Xq에 대한 측정 S(X_Q)는 두가지 기하학 거리를 곱해 이루어 진다.  
$$S_gdfs(X_Q) = D_B(X_Q) * E $$
### Inter-class distanc
첫번째로 해당 Feature subspace에서의 class 간 거리에 의해 이루어진다.  
그림을 참고했을때 클래스 중심간 거리가 멀수록, 그리고 클래스 내부분산이 작을 수록 쉽게 분류되리라 예쌍된다.
따라서 클래스 중심간 거리 - 클래스 내부분산을 고려한 값을 측정해 measure로 사용한다.

### Eveness of Inter-class distances
class의 거리들이 균등할 수록, 쉽게 분류되리라 예상할 수 있다.
따라서 균등도를 측정한다.

## Implementation with Sequential Forward Selection

