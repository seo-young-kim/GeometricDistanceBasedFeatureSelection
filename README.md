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

### 2. Eveness of Inter-class distances
The more equal the distance between classes in the Feature subspace, the easier it can be expected to be classified.
Therefore, it is used as a second measurement.

## Implementation with Sequential Forward Selection
Through Sequential Forward selection, we can selects feature subsets with maximum gdbfs value.

