## Table of Contents

This folder contains several examples of applying graph machine learning (ML) algorithms on network-structured
data to solve several common problems including node attribute inference (inferring
entity properties) and link prediction (predicting relations and/or their properties). The
examples demonstrate using the `StellarGraph` library to build machine learning
workflows on both homogeneous and heterogeneous networks.

Each folder contains one or more examples of using the StellarGraph implementations of the
state-of-the-art algorithms, GraphSAGE [3], HinSAGE, GCN [5], GAT [6], Node2Vec [1], and Metapath2Vec [2]. 
GraphSAGE, HinSAGE, and GAT are variants of Graph Convolutional Neural networks [5]. Node2Vec and
Metapath2Vec are methods based on graph random walks and representation learning using the
Word2Vec [4] algorithm.

The examples folder structure is shown below.

* [`/embeddings`](https://github.com/stellargraph/stellargraph/tree/master/demos/embeddings)

    Examples of unsupervised node representation learning for homogeneous networks, heterogeneous networks, and homogeneous networks with node features
    using Node2Vec, Metapath2Vec, and Unsupervised GraphSAGE algorithm, respectively.

* [`/link-prediction`](https://github.com/stellargraph/stellargraph/tree/master/demos/link-prediction)

    Examples of using StellarGraph algorithms for link prediction on homogeneous and heterogeneous networks.

* [`/node-classification`](https://github.com/stellargraph/stellargraph/tree/master/demos/node-classification)

    Examples of using StellarGraph algorithms for node classification on homogeneous and heterogenous networks.

* [`/ensembles`](https://github.com/stellargraph/stellargraph/tree/master/demos/ensembles)

    Examples of using ensembles of graph convolutional neural networks, e.g., GraphSAGE, GCN, HinSAGE, etc., for
    node classification and link prediction. Model ensembles usually yield better predictions than single models, 
    while also providing estimates of prediction uncertainty as a bonus. 

* [`/calibration`](https://github.com/stellargraph/stellargraph/tree/master/demos/calibration)

    Examples of calibrating graph convolutional neural networks, e.g., GraphSAGE, for binary and
    multi-class classification problems.

* [`/community_detection`](https://github.com/stellargraph/stellargraph/tree/master/demos/community_detection)

    Examples of using unsupervised GraphSAGE embeddings in a context of community detection. Community detection is demonstrated on a terrorist network, where groups of terrorist groups are found using dbscan on top of the graphSAGE embeddings.
    Note that this demo requires the installation of `igraph-python`, see the `README.md` in this directory for more details.

* [`/use-cases`](https://github.com/stellargraph/stellargraph/tree/master/demos/use-cases)

    Example use-cases/applications for graph neural network algorithms.

## References

1. Node2Vec: Scalable Feature Learning for Networks. A. Grover, J. Leskovec. ACM SIGKDD International Conference on 
Knowledge Discovery and Data Mining (KDD), 2016. ([link](https://snap.stanford.edu/node2vec/))

2. Metapath2Vec: Scalable Representation Learning for Heterogeneous Networks. Yuxiao Dong, Nitesh V. Chawla, and 
Ananthram Swami. ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD), 135–144, 2017
([link](https://ericdongyx.github.io/metapath2vec/m2v.html))

3. Inductive Representation Learning on Large Graphs. W.L. Hamilton, R. Ying, and J. Leskovec arXiv:1706.02216 
[cs.SI], 2017. ([link](http://snap.stanford.edu/graphsage/))

4. Distributed representations of words and phrases and their compositionality. T. Mikolov, 
I. Sutskever, K. Chen, G. S. Corrado, and J. Dean. In Advances in Neural Information Processing
 Systems (NIPS), pp. 3111-3119, 2013. ([link](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf))

5. Semi-Supervised Classification with Graph Convolutional Networks. T. Kipf, M. Welling. 
ICLR 2017. arXiv:1609.02907 ([link](https://arxiv.org/abs/1609.02907))

6. Graph Attention Networks. P. Velickovic et al. ICLR 2018 ([link](https://arxiv.org/abs/1710.10903))

7. On Calibration of Modern Neural Networks. C. Guo, G. Pleiss, Y. Sun, and K. Q. Weinberger. 
ICML 2017. ([link](https://geoffpleiss.com/nn_calibration))
