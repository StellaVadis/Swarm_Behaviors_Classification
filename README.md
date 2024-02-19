# Swarm_Behaviors_Classification By Two Feature Fusion methods

There are three categories of swarm behaviors: Flocking, aligning, and grouping.

There are 200 boids in a swarm, each boid has features: positional x-axis, positional y-axis coordinate, x-axis velocity, y-axis velocity, alignment, separation, cohesion force on x- and y-axis, number of boids in radius of centroids, totally 12 features for each boid. Then 200 boids in a swarm has totally 200 * 12 = 2400 features.

However, since the boids has no 'order' with each other. It does not matter which boid appear at the first place and second place. We need to propose special feature fusion method to eliminate the order of boids and reduce the dimensionality of features.

In this paper, we adopt two data preprocessing method (two feature fusion methods): 
1. Centroid Method: Average the features over 200 boids in the swarm to get integrated features. The 12 features of 200 boids are fused into 12 mean features, such that the classification can be carried on the preprocessed dataset.
2. 2D mapping method: We map all the samples onto the 2D images, according to their positional coordinates. Then we create 11 channels for this 2D images, with these channels recording the corresponding features of boids.

Simple machine learning classfiers are used for classifications.
