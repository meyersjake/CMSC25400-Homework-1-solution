# CMSC25400-Homework-1-solution

Download Here: [CMSC25400 Homework 1 solution](https://jarviscodinghub.com/assignment/cmsc25400-homework-1-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1. (30 points) As we saw in class, k-means clustering minimizes the average square distance distortion
Javg2 =
∑
k
j=1
∑
x∈Cj
d(x,mj )
2
, (1)
where d(x, x
′
) = ∥x−x
′∥, and Cj is the set of points belonging to cluster j. Another distortion function
that we mentioned is the intra-cluster sum of squared distances,
JIC =
∑
k
j=1
1
|Cj |
∑
x∈Cj
∑
x′∈Cj
d(x, x
′
)
2
.
(a) Given that in k-means, mj =
1
|Cj |
∑
x∈Cj
x, show that JIC = 2Javg2 .
(b) Let γi ∈ {1, 2, . . . , k} be the cluster that the i’th datapoint is assigned to, and assume that there
are n points in total, x1, x2, . . . , xn. Then (1) can be written as
Javg2 (γ1, . . . , γn,m1, . . . ,mk) = ∑n
i=1
d(xi
,mγi
)
2
. (2)
Recall that k-means clustering alternates the following two steps:
1. Update the cluster assignments:
γi ← argmin
j∈{1,2,…,k}
d(xi
,mj ) i = 1, 2, . . . , n.
2. Update the centroids:
mj ←
1
|Cj |
∑
i : γi=j
xi j = 1, 2, . . . , k.
Show that the first of these steps minimizes (2) as a function of γ1, . . . , γn, while holding m1, . . . ,mk
constant, while the second step minimizes it as a function of m1, . . . ,mk, while holding γ1, . . . , γn
constant. The notation “i : γi =j” should be read as “all i for which γi =j”.
(c) Prove that as k-means progresses, the distortion decreases monotonically iteration by iteration.
(d) Give an upper bound on the maximum number of iterations required for full convergence of the
algorithm, i.e., the point where neither the centroids, nor the cluster assignments change anymore.
1
2. (30 points) Implement the k-means algorithm in a language of your choice (MATLAB, Python, or R
are recommended), initializing the cluster centers randomly, as explained in the slides. The algorithm
should terminate when the cluster assignments (and hence, the centroids) don’t change anymore.
Note: if you use a relatively high level language like MATLAB or Python, your code can use linear
algebra primitives, such as matrix/vector multiplication, eigendecomposition, etc. directly. However,
you are expected to write you own k–means and k–means++ functions from scratch. Please don’t
submit code consisting of a single call to some pre-defined “kmeans” function.
(a) The toy dataset toydata.txt contains 500 points in R
2
coming from 3 well separated clusters.
Test your code on this data and plot the final result as a 2D plot in which each point’s color or
symbol indicates its cluster assignment. Note that because of the random initialization, different
runs may produce different results, and in some cases the algorithm might not correctly identify
the three clusters. Plot the value of the distortion function as a function of iteration number for
20 sepearate runs of the algorithm on the same plot. Comment on the plot.
(b) Now implement the k–means++ algorithm discussed in class and repeat part (a) using its result
as intialization (except for the 2D plot). Comment on the convergence behavior of k–means++
vs. the original algorithm.
3. (up to 20 points extra credit) You likely found that on the “toydata” dataset, most of the time
even vanilla k–means clustering produces acceptable solutions. Create a dataset of your own for which
(on average over many runs) k–means++ improves the performance of k–means by at least a factor of
10 in terms of the distortion function value of the final clustering. Submit the code that you used to
generate the dataset.

