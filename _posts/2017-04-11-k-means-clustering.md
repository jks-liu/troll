---
layout: post
title: "K-means clustering"
description: ""
category:
tags: [k-means, clustering, k-means++]
---
{% include JB/setup %}

# Table of context
* This line is important for toc, but will be ignored.
{:toc}

# Clustering
Purpose: to partition _n_ observations into _k_ clusters.

The _k_ clusters is a [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram) with repect to a distance function _d_.

![Varonoi diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/5/54/Euclidean_Voronoi_diagram.svg/382px-Euclidean_Voronoi_diagram.svg.png)

Euclidean distance. Source: WikiPedia [^3]

# Data preprocessing

For scalar, we often use [Minkowski distance](https://en.wikipedia.org/wiki/Minkowski_distance).

$$X=(x_{1},x_{2},\ldots ,x_{n}){\text{ and }}Y=(y_{1},y_{2},\ldots ,y_{n})\in {\mathbb  {R}}^{n}$$

$$\left(\sum_{i=1}^n |x_i-y_i|^p\right)^{1/p}$$

Apparently, Euclidean distance (let \\(p = 2\\)) and Manhattan distance (let \\(p = 1\\)) are 2 particular cases of it.

We do [Normalization](https://en.wikipedia.org/wiki/Normalization_(statistics)) on our data. In data processing, we often use [Feature scaling](https://en.wikipedia.org/wiki/Feature_scaling).

Other type of data, refet to [^2].
# _k_-means

We often use [Lloyd's algorithm](https://en.wikipedia.org/wiki/Lloyd%27s_algorithm). And we often call it the "k-means algorithm".

Initial k means \\(m_1^{(t)}, \ldots, m_k^{(t)}, t = 1 \\)

1. Assignment step

    Let is yields the least within-cluster sum of squares (WCSS).

    $$S_{i}^{(t)}={\big \{}x_{p}:{\big \|}x_{p}-m_{i}^{(t)}{\big \|}^{2}\leq {\big \|}x_{p}-m_{j}^{(t)}{\big \|}^{2}\ \forall j,1\leq j\leq k{\big \}}$$

2. Update step

    Update new means.

    $$m_{i}^{(t+1)}={\frac {1}{|S_{i}^{(t)}|}}\sum_{x_{j}\in S_{i}^{(t)}}x_{j}$$
# _k_-means++
# Gaussian Mixture Model
# Applications

[^1]: K-means clustering. https://en.wikipedia.org/wiki/K-means_clustering
[^2]: 张洋. 算法杂货铺——k均值聚类(K-means). http://www.cnblogs.com/leoo2sk/archive/2010/09/20/k-means.html
[^3]: Voronoi diagram. https://en.wikipedia.org/wiki/Voronoi_diagram
