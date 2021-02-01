# TPE

### Use Case

1. hyper-parameter optimization tasks will mean high dimension
2. small fitness evaluation budgets



### The way it works

##### Ｍodel 

1. Whereas the Gaussian-process based approach modeled p(y|x) directly, this
   strategy models p(x|y) and p(y)

   - The tree-structured Parzen estimator (TPE) models p(x|y) by transforming the graph-structured generative process of **hyperparameter space**
     $$
     p(y \mid x)=\frac{p(x \mid y) * p(y)}{p(x)}
     ?
     $$
	
     
     - in the experimental section, we will see that the configuation space is described using uniform, log-uniform, quantized log-uniform, and categorical variables.
     - TPE algorithm makes the following replacements: uniform → truncated Gaussian mixture, log-uniform → exponentiated truncated Gaussian mixture, categorical → re-weighted categorical.
     
   - replacing the distributions of the configuration $p(x \mid y)$ prior with non-parametric densities.

$$
p(x \mid y)=\left\{\begin{array}{ll}
\ell(x) & \text { if } y<y^{*} \\
g(x) & \text { if } y \geq y^{*},
\end{array}\right.
$$

> for l(x): ==the higher the likelihood is, the better the parameter is==
>
> for g(x): ==the lower the better== 



##### Acquisition Function: EI

we would like points x with high probability under "(x) and low probability under g(x):

- The tree-structured form of  l and g makes it easy to draw many candidates according to l 
- and evaluate them according to g(x)/l(x). 
- On each iteration, the algorithm returns the candidate x with the greatest EI.



### Details of Parzen Estimator

> The Tree-structured Parzen Estimator works by drawing sample hyperparameters from *l(x)*, evaluating them in terms of *l(x) / g(x)*, and returning the set that yields the highest value under *l(x) / g(x)* corresponding to the greatest expected improvement*.* These hyperparameters are then evaluated on the objective function. If the surrogate function is correct, then these hyperparameters should yield a better value when evaluated!





<u>Background</u>:

The models l(x) and g(x) are hierarchical processes involving discrete-valued and continuous-valued variables.



The Adaptive Parzen Estimator yields a model over X by placing density in the vicinity of K observations B = {x(1), ..., x(K)} ⊂ H

1. for continuous hyperparameter:

   - Each continuous hyper-parameter was specified by a uniform prior over some interval (a, b), or a Gaussian, or a log-uniform distribution
   - The TPE substitutes an equally-weighted mixture of that prior with Gaussians centered at each of
     the x(i) ∈ B.
     - The standard deviation of each Gaussian was set to the greater of the distances to the
       left and right neighbor, but clipped to remain in a reasonable range.
   - In the case of the uniform, the points a and b were considered to be potential neighbors.
   - The log-uniform hyper-parameters were treated as uniforms in the log domain

2. for discrete hyperparameter

   supposing the prior was a vector of N probabilities pi

   - the posterior vector elements were proportional to N pi + Ci
     - where Ci counts the occurrences of choice i in B


The two densities *l* and *g* are modeled using Parzen estimators, which are hierarchical processes involving discrete and continuous hyperparameters. This is also why this algorithm is called "Tree-Structured Parzen Estimator": It means that the hyperparameter space is tree-like: the value chosen for one hyperparameter determines what hyperparameter will be chosen next and what values are available for it. For each hyperparameter in the hyperaprameter space, a 1-D Parzen estimator is created, which has different forms depending on whether the hyperparameter is continuous or discrete. 



### H

Each time the algorithm proposes a new set of candidate hyperparameters, it evaluates them with the actual objective function and records the result in a pair (score, hyperparameters). These records form the **history**. The algorithm builds *l(x)* and *g(x)* using the history to come up with a probability model of the objective function that improves with each iteration.



### Advantages

The expected improvement criteria allows the model to balance [exploration versus exploitation](https://en.wikipedia.org/wiki/Multi-armed_bandit). *l(x)* is a distribution and not a single value which means that the hyperparameters drawn are likely close but not exactly at the maximum of the expected improvement. Moreover, because the surrogate is just an estimate of the objective function, the selected hyperparameters may not actually yield an improvement when evaluated and the surrogate model will have to be updated. This updating is done based on the current surrogate model and the history of objective function evaluations.



### Youtube

target performance: $\gamma$ quantile of search results:
$$
\gamma = p (c < c^{*}) = \int_{-\infty}^{c^{*}} p(y) \,dy
$$


- c<= $c^{*}$: good (hyperparameter)
- c > $c^{*}$: bad (hyperparameter)

> the split (of H) is done by $\gamma$ q





In the classical approach the parameter, $\theta,$ is thought to be an unknown, but fixed, quantity. A random sample $X_{1}, \ldots, X_{n}$ is drawn from a population indexed by $\theta$ and, based on the observed values in the sample, knowledge about the value of $\theta$ is obtained. In the Bayesian approach $\theta$ is considered to be a quantity whose variation can be described by a probability distribution (called the prior distribution). This is a subjective distribution, based on the experimenter's belief, and ==is formulated before the data are seen (hence the name prior distribution).== **A sample is then taken from a population indexed by $\theta$ and the prior distribution is updated with this sample information.** ==The updated prior is called the posterior distribution.== This updating is done with the use of Bayes' Rule (seen in Chapter 1), hence the name Bayesian statistics.

If we denote the prior distribution by $\pi(\theta)$ and the sampling distribution by $f(\mathbf{x} \mid \theta)$, then the posterior distribution, the conditional distribution of $\theta$ given the sample, $\mathbf{x}$, is
$(7.2 .7)$
$$
\pi(\theta \mid \mathbf{x})=f(\mathbf{x} \mid \theta) \pi(\theta) / m(\mathbf{x}), \quad(f(\mathbf{x} \mid \theta) \pi(\theta)=f(\mathbf{x}, \theta))
$$
where $m(\mathbf{x})$ is the marginal distribution of $\mathbf{X},$ that is,
$(7.2 .8)$
$$
m(\mathbf{x})=\int f(\mathbf{x} \mid \theta) \pi(\theta) d \theta
$$
Notice that the posterior distribution is a conditional distribution, conditional upon observing the sample. The posterior distribution is now used to make statements about $\theta$, which is still considered a random quantity. For instance, the mean of the posterior distribution can be used as a point estimate of $\theta$.