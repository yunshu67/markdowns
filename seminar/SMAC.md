### Advantages of SMBO

- It offers the appealing prospects of interpolating performance between observed parameter settings and of extrapolating to previously unseen regions of parameter space
- It can also be used to quantify importance of each parameter and parameter interactions.



### Drawbacks of SMBO

However, being grounded in the “blackbox function optimization” literature from statistics (see, e.g., [12]), SMBO has inherited a range of limitations inappropriate to the automated algorithm configuration setting

These limitations include 

- a focus on deterministic target algorithms

- use of costly initial experimental designs

- reliance on computationally expensive models

- and the assumption that all target algorithm runs have the same execution costs

Despite considerable recent advances [13, 14, 15], all published work on SMBO still has three key limitations that prevent its use for general algorithm configuration tasks: 

1. <u>it only supports numerical parameters;</u> 
2. <u>it only optimizes target algorithm performance for single instances;</u>
3. it lacks a mechanism for terminating poorly performing target algorithm runs early





### SMAC

- Here, we discuss the new model class we use in SMAC to support categorical parameters and multiple instances (Sections 4.1 and 4.2, respectively);
-  then, we describe how SMAC uses its models to select promising parameter configurations (Section 4.3)

##### 4.1 Generalization II: Models for Categorical Parameters

- SMAC’s models are based on random forests [16], a standard machine learning tool for regression and classification. 

- Random forests are collections of regression trees, which are similar to decision trees but have real values (here: target algorithm performance values) rather than class labels at their leaves.

- Regression trees are known to perform well for categorical input data; indeed, they have already been used for modeling the performance of heuristic algorithms (e.g., [18, 19]). Random forests share this benefit and typically yield more accurate predictions [16]

- they also allow us to quantify our uncertainty in a given prediction

  ---

**construct random forests:**

1. We construct a random forest as a set of B regression trees, each of which is built on n data points randomly sampled with repetitions from the entire training data set {(θ1, o1), . . . , (θn, on)}
2. At each split point of each tree, a random subset of ⌈d · p⌉ of the d algorithm parameters is considered eligible to be split upon;
   - the split ratio p is a parameter, which we left at its default of p = 5/6
   -  A further parameter is nmin, the minimal number of data points required to be in a node if it is to be split further; we use the standard value nmin = 10. 
3. Finally, we set the number of trees to B = 10 to keep the computational overhead small.



**acquisition function**

Having defined EI(θ), we must still decide how to identify configurations θ with large EI(θ), This amounts to a maximization problem across parameter configuration space.

*previous SMBO algorithms*:

- Previous SMBO methods [13, 14, 15] simply applied random sampling for this task (in particular, they evaluated EI for 10 000 random samples), which is unlikely to be sufficient in high-dimensional configuration spaces, especially if promising configu- rations are sparse.

*SMAC*:

<u>To gather a set of promising configurations with low computational overhead, we perform a simple multi-start local search and consider all resulting configurations with locally maximal EI.</u>

> ThissearchissimilarinspirittoPARAMILS[7,8],
>
> but instead of algorithm performance it optimizes EI(θ) (see Equation 1), which can be evaluated based on the model predictions μθ and σθ2 without running the target algo- rithm. 

Details:

1. We compute EI for all configuations used in previous target algorithm runs
2. pick the ten configurations with maximal EI 
3. initialize a local search at each of them.



<u>To seamlessly handle mixed categorical/numerical parameter spaces, we use a randomized one-exchange neighbourhood, including the set of all configurations that differ in the value of exactly one discrete parameter, as well as four random neighbours for each numerical parameter.</u>

In particular:

1. we normalize the range of each numerical parameter to [0,1] and then sample four “neighbouring” values for numerical parameters with current value v from a univariate Gaussian distribution with mean v and standard deviation 0.2, rejecting new values outside the interval [0,1]. ==为每个numerical参数随机加了四个neighbor==

   - Since batch model predictions (and thus batch EI computations) for a set of N configurations are much cheaper than separate predictions for N configurations, we use a best improvement search, evaluating EI for all neighbours at once; 

     由于一组N个配置的批处理模型预测（以及批处理EI计算）比N个配置的单独预测便宜得多，因此我们使用最佳改进搜索，一次评估所有邻居的EI；

2. we stop each local search once none of the neighbours has larger EI.



<u>In order to provide unbiased training data for future models</u>：we interleave randomly-sampled configurations

More specifically,

1. we alternate between configurations from the list and addi- tional configurations sampled uniformly at random
   - Since *Intensify* always compares at least two configurations against the current incumbent, at least one randomly sampled configuration is evaluated in every iteration of SMBO.
   - In finite configuration spaces, thus, each configuration has a positive probability of being selected in each iteration.




