# GeometricDistanceBasedFeatureSelection
It is a code that uses geometry measers to evaluate Feature subsets and to select optimal Feature subsets based on them.  
Feature subset's evaluation implements the 'Feature selection based on geometric distance for high-dimensional data.' introduced in the paper.  
__It can be used through 'pip install gdbfs'.  
Please refer to the Repository 'https://github.com/seo-young-kim/GDBFS_deploy' for details.__  
This page provides a brief description of the techniques.  

Reference 'Lee, J. H., & Oh, S. Y. (2016).
Feature selection based on geometric distance for high-dimensional data. Electronics Letters, 52(6), 473-475.'.  

## Distance measurement method of Feature subset
The measurement for Feature subsets is multiplied by two geometric distances.

### 1. Inter-class distance

First, the distance between classes from the corresponding Feature subspace is achieved.  
When referenced in the figure1, the further the distance between the center of the class and the smaller the intracranial partiality, the easier it will be classified.  
Therefore, (the distance between the center of the class) - (class Internal Variance) is used as measurement.
![compare_by_two_varible](https://user-images.githubusercontent.com/49013650/110815881-2de83a80-82ce-11eb-871e-1c628aa4e9b7.png)
()
### 2. Eveness of Inter-class distances
The more equal the distance between classes in the Feature subspace, the easier it can be expected to be classified.
Therefore, it is used as a second measurement.  
![Eveness](https://user-images.githubusercontent.com/49013650/110815885-2e80d100-82ce-11eb-842a-8e5e22fa907a.png)


## Implementation with Sequential Forward Selection
Through Sequential Forward selection, we can selects feature subsets with maximum gdbfs value.  

![SFS](https://user-images.githubusercontent.com/49013650/110815888-2f196780-82ce-11eb-8338-04a5195b42ea.png)  
Figure 3. Sequential forward selection from : https://www.cc.gatech.edu/~bboots3/CS4641-Fall2018/Lecture16/16_FeatureSelection.pdf
