##### University of Vienna  
##### Faculty of Computer Science  
Assoz. Prof. Dr. Nils M. Kriege  
Thomas Lang, MSc  
Megi Teneqexhi, BSc  
Scientific Data Management  

### 2024S
# Programming Assignment 1: Hierarchical Clustering
## General Remarks:
• This is one of three programming assignments in this lecture. In each, you can achieve 100 points.  
• The deadline is on 30.04.2021 at 2:00 pm. No deadline extensions can be granted. After the deadline,  
your results are presented to the other students and the peer-review process starts.
• If you encounter any problems do not hesitate to post a question on the dedicated Moodle forum.  
• Upload your solution as a zip archive with the following naming scheme group X.zip, where X is  
your team number. The archive should contain your code as well as a report in PDF or HTML format.
• You may use a programming language of your choice. Your code must be well documented and readable.  
• Work in teams of up to 5 students. We assume a fair distribution of work. If this was not possible, please  
indicate the individual contributions within the report.


## Task 1-1 Naive Implementation (25P)

Implement the naive greedy approach for hierarchical clustering as discussed in the lecture with time complexity of O(n3) and O(n2) memory usage.  
You can freely choose the distance function and the linkage method. Do not use a built-in implementation of hierarchical clustering.  
Keep track of the order in which the clusters are merged and build a hierarchy of clusters. Test your algorithm,
e.g., by comparing your results to the results obtained by publicly available implementations.


## Task 1-2 Efficient Implementation (50P)

Implement one of the more efficient algorithms, either based on priority queues, minimum spanning trees or
nearest neighbor chains. Use the same distance and linkage method as in the naive approach if possible. Test
your implementation thoroughly.

#### Option 1:  
Implement the hierarchical clustering algorithm utilizing priority queues to achieve O(n^2 log n) time. You may choose between the variant using a single priority queue and the variant using a priority queue for every object. Further implementation details for the first method are described in [1]; refer to Chapter 17 of [2] for details on the second approach. Do not use a built-in implementation of hierarchical clustering. You may implement a binary heap by yourself or use available priority queue data structures such as [heapq](https://docs.python.org/3/library/heapq.html). Note that both methods require updating and deleting entries in the heap. Finding these entries efficiently often requires maintaining an additional data structure.

#### Option 2: 
Implement the hierarchical clustering algorithm based on minimum spanning tree computation with Prim’s algorithm. Make a well-founded decision as to whether a custom implementation makes sense or whether a library for graph algorithms containing Prim’s algorithm should be used and implement the approach.  

##### Option 3: 
Implement the hierarchical clustering algorithm utilizing a nearest-neighbor chain with time complexity O(n2) based on the discussion in the lecture. Do not use a built-in implementation of hierarchical clustering, but collections such as [deque](https://docs.python.org/3/library/collections.html#collections.deque) are allowed.

## Task 1-3 Experimental Evaluation and Documentation (25P)

Evaluate your implementations with a focus on runtime.  
• Use randomly generated data and the credit card dataset of the [Kaggle notebook](https://www.kaggle.com/vipulgandhi/hierarchical-clustering-explanation). The website also contains detailed information on how to use hierarchical clustering in Python.  
• Compare your implementations to those available in [Python libraries](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html). Verify your algorithm by comparing on a small subset of the data and visualize your result. Evaluate the runtimes.  
• Is the observed runtime in agreement with the theoretical analysis? Try to explain your findings. Describe your hardware in terms of cache and memory sizes and try to reason about runtime behavior in a
discussion of your results.  

Write a report which describes your results and any important implementation details. The documentation
should make your work reproducible, legible, and comparable. Prepare a short presentation of your most
relevant findings taking 5-7 minutes.  


##### References  

[1] KURITA, T. An efficient agglomerative clustering algorithm using a heap. Pattern Recognition 24, 3
(1991), 205–209.  
[2] MANNING, C. D., RAGHAVAN, P., AND SCHUTZE ¨ , H. Introduction to information retrieval. Cambridge
University Press, Cambridge, UK, 2008, ch. 17.  