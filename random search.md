- ~~RS works by iteratively moving to better positions in the search-space, which are sampled from a [hypersphere](https://en.wikipedia.org/wiki/Hypersphere) surrounding the current position.~~

  ---

- By contrast, Random Search sets up a grid of hyperparameter values and selects random combinations to train the model and score. ==This allows you to explicitly control the number of parameter combinations that are attempted.== The number of search iterations is set based on time or resources. 

### performance comparison

While it’s possible that RandomizedSearchCV will not find as accurate of a result as GridSearchCV, ==it surprisingly picks the best result more often== than not and in a *fraction* of the time it takes GridSearchCV would have taken. Given the same resources, Randomized Search can even outperform Grid Search. 



### figures

![Image for post](https://i.loli.net/2021/01/06/yNp5c3ozaYskT7w.png)

>  With grid search, nine trials only test three distinct places. With random search, all nine trails explore distinct values.

---

### 最基本的随机搜索

顾名思义，就是随机的搜索，没有特别的要说的，

这只是一个简单的样例，当然还有许多其他场景会用到随机搜索。但是这种模型非常简单，有时候并不能给出令我们满意的结果，我们还需要对其一步步进行改进。但是核心的思想就是这样的，以后的都是围绕这一思想进行的，这先提前说一下。



###　爬山搜索算法

爬山搜索算法是一种简单的贪心改进，通过基本的搜索算法我们发现，我们并没有利用到已经获得的最优解（假如十亿个数字按一定多项式分布），而是粗暴的进行了随机抽样求取最优解（简单粗暴有时候确实非常好）。贪心策略的假如，使随机搜索算法的效率和准确性有一个较好的提升。

![image-20210105213421354](https://i.loli.net/2021/01/06/ryLuo9hONHebq1i.png)

==由此我们可以发现爬山搜索算法的一个缺陷，就是比较容易陷入局部最优解中。==

一个简单的消除（可能也消除不了）该缺陷的方法就是，我们多次执行该搜索算法，以期随机选取的开始点落在B点两侧的下降曲线上。最后再比较多次执行爬山搜索算法的结果获取更理想的解。有时候被称为“多重爬山算法”。



> ==1、数据规模大，精确的结果难以在一定时间计算出。==
> ==2、结果的些许的不精确能够被接受。==



==The drawback of random search is that it yields high variance during computing. Since the selection of parameters is completely random; and since no intelligence is used to sample these combinations, luck plays its part.==



==This works best under the assumption that not all hyperparameters are equally important.== 