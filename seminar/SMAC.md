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



