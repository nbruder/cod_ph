# Overcome the curse of dimension in persistent homology

Persistent homology is a method to discover topological features within point cloud data. Within this data, we construct a graph: two points are connected if and only if their distance is smaller than a parameter $2\epsilon$. At a specific $\epsilon$, enough points are connected to form a cycle-like structure which then can be detected by persistent homology. If $\epsilon$ is chosen too large, this cycle vanishes as the points on opposite sides are then connected. By a similar construction, even higher-dimensional topological features can be formed. Thus, by varying the scaling parameter $\epsilon$, one can study the appearance and disappearance of connected components, loops, voids or their higher-dimensional equivalents.

Using this method, one tries to differentiate between these topological features and surrounding noise by having a look at the "lifetime" of these features. The general interpretation is that noise forms a lot of cycles having a short "lifetime", whereas "true" cycles exist for a long time-span. Unfortunately, vanilla persistent homology based on the Euclidian distance is not robust against high-dimensional noise because the "true" topological features are blurred, leading persistent homology to detect "phantom cycles" within the noise. This phenomenon is known as the curse of dimension.

In the following, we start by giving a description of the curse of dimension and we give a short mathematical reasoning for its existence. An example shall illustrate the arising issues. Afterwards, we present two potential solutions to the curse of dimension. In a last chapter, we apply these solutions to different scenarios and compare their performance by inspecting their persistence diagrams and multi-dimensional scalings in two dimensions.

This work is based on work from the [pre-print](https://arxiv.org/pdf/2311.03087) by Damrich et al. 
