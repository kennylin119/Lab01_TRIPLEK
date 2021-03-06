# TripleK

Kenny Lin, Kenny Li, Kendrick Liang  
APCS2 pd 1  
Lab #1 What Does the Data Say?  

## Hypothesis
Searching for the worst case scenario, a sorted array, with preset arrays of varying sizes should result in a quadratic runtime. This is because the partition
occurs in the first element each time and increments by 1. This is the least efficient way to perform this method because half of the recursive call is not
used. Searching for the best case scenario, in which the pivot is right in the middle, should result in n log n runtime becasue the partition part of the sort would result in the array being split into two equal sections each time, which is log n runtime.

## Background 
We are using preset arrays that vary in size for our experiment. The value of each element in the array corresponds to its index.

## Experimental Methology
Our experimental apparatus is to populate various set arrays from sizes of 1000 to 15000, increasing in size by 100 every iteration. We will conduct a sort for the worst case scenario and best case scenario each time on an already sorted array, 10 times each for every iteration. The 10 runs will be averaged into one value for that array size. This way we will have a consistent sort method each time. 

## Results 
Worst Case:
![Worst Case](https://github.com/kennylin119/Lab01_TRIPLEK/blob/master/Worst%20case.png "Worst Case Graph")

Best Case:
![Best Case](https://github.com/kennylin119/Lab01_TRIPLEK/blob/master/best%20case.png "Best Case Graph")

Both Case:
![Both Case](https://github.com/kennylin119/Lab01_TRIPLEK/blob/master/both%20case.png "Both Case Graph")

## Conclusions 
Overall the data proved that our hypothesis was correct. With a set array and constant sort of the worst case scenario, the only thing that was different was the size of the array. The data for the worst case scenario showed a curve similar to that of a quadratic, which shows that our algorithm has a run time efficiency of O(n^2) at worst case. For the best case, we saw a relatively huge spike in nanoseconds for the first 5 iterations of the algorithm that decreased over time. After those 5 iterations, it looked more like a linear relationship than a nlog(n) relationship. The pivot position on a sorted array has a big effect on the efficiency of the algorithm. The closer the pivot position is to the middle of the array, the faster it will run. If the pivot starts at one of the extremes, it will lead to a runtime of n^2. If we start from the middle, however, we will get a runtime of nlog(n).
