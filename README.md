# Structure-Aware Hierarchical Graph Pooling using Information Bottleneck


**Authors**
- [Kashob Kumar Roy](https://www.linkedin.com/in/forkkr/) 
- [Amit Roy](https://amitroy7781.github.io/)
- [Amin Ahsan Ali](http://www.cse.iub.edu.bd/faculties/53)
- [M Ashraful Amin](http://www.cse.iub.edu.bd/faculties/25) 
- [A K M Mahbubur Rahman](http://www.cse.iub.edu.bd/faculties/56)

This is a pytorch implementation of our [paper](https://arxiv.org/abs/2104.13012) "Structure-Aware Hierarchical Graph Pooling using Information Bottleneck" which has been accepted by IJCNN 2021.  Check the video presentation of our paper [here](https://youtu.be/L3amRKyaCsw).


# Abstract

Graph pooling is an essential ingredient of Graph Neural Networks (GNNs) in graph classification and regression tasks. For these tasks, different pooling strategies have been proposed to generate a graph-level representation by downsampling and summarizing nodes' features in a graph. However, most existing pooling methods are unable to capture distinguishable structural information effectively. Besides, they are prone to adversarial attacks. In this work, we propose a novel pooling method named as **HIBPool** where we leverage the Information Bottleneck **IB** principle that optimally balances the expressiveness and robustness of a model to learn representations of input data. Furthermore, we introduce a novel structure-aware Discriminative Pooling Readout **(DiP-Readout)** function to capture the informative local subgraph structures in the graph. Finally, our experimental results show that our model significantly outperforms other state-of-art methods on several graph classification benchmarks and more resilient to feature-perturbation attack than existing pooling methods. 

# HIBPool
![HIBPool](HIBPool.png?raw=true "Title")

To determine different substructures present in graph data, the input graph is partitioned into communities where  intra-community nodes are represented with same color and they are densely connected than inter-community nodes. After aggregating features from neighborhood using Messaging Passing Network (MPN) we apply structure-aware DiP-Readout to obtain distinguishable representations of communities with different substructures while the pooled graph of next layer is created with the edges connecting different communities. Summary representation is obtained by a readout function after the final layer. Optimizing with IB principal ensure minimal redundancy from graph data with sufficient information to predict the class labels.


# Baseline Comparison
![Baseline Comparison](comparison.png?raw=true "Title")

    Table : Comparison with Baselines: ’-’ denotes that results are not publicly available.

## Cite

If you find our paper or repo useful then please cite our paper:

```bibtex
@article{roy2021structure,
  title={Structure-Aware Hierarchical Graph Pooling using Information Bottleneck},
  author={Roy, Kashob Kumar and Roy, Amit and Rahman, AKM and Amin, M Ashraful and Ali, Amin Ahsan},
  journal={arXiv preprint arXiv:2104.13012},
  year={2021}
}

```
