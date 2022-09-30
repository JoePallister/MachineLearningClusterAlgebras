# Machine Learning and Cluster Algebras
Here we are experimenting with machine learning techniques for classification problems in cluster algebras.

The file "Auxillary_code_for_generating_cluster_algebra_data.ipynb" is used to generate the cluster algebra data we wish to study. It uses the Sage kernel and the cluster algebra package here: https://doc.sagemath.org/html/en/reference/algebras/sage/algebras/cluster_algebra.html

The file "MachineLearningClustersKeras.ipynb" is where we use neural networks (Keras) to study the classification of b-matrices by cluster algebra. We first look at a binary classification for A5 and D5. We then try a binary classification of A6 and D6, where we have many more matrices. Finally we attempt a ternary classification of A6, D6 and E6. For both the binary and ternary classifications for 6 node quivers we are able to obtain accuracies of over 0.85.

In "MachineLearningClustersSupportVectorMachine.ipynb" we apply scikit-learn's support vector machine implementation to our classification problem. For the same binary classifications as before this is much better and faster than using neural networks. We have accuracies of 1 and 0.95 for the A5/D5 and A6/D6 problems respectively. For the A6/D6/E6 problem our accuracy drops to 0.83, so the models in Keras do better in that case.

In "MachineLearningClustersKerasConvolution.ipynb" we return to Keras. Contrasting with our previous neural networks, we here keep the matrix structure of the b-matrices and aim to apply Keras' convolution layers. For the binary classifications we have accuracies of over 0.9. For the ternary classifications this model suffers a bit and gets stuck around accuracy 0.8
