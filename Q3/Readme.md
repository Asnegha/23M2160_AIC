# Q3. 
### a) Assume a 2D Grid of constrained straight interlocking paths with well defined start and end points. What metric should you use to compare distances between any two different paths? Why is it better than other metrics available? List out some of the other metrics.

**Answer:** One common metric for this purpose is the **Manhattan distance**, also known as the L1 distance. Manhattan distance measures the sum of the absolute differences in the x and y coordinates between two points. It is calculated as the sum of the horizontal and vertical distances between points. In a 2D grid, where movement is constrained to horizontal and vertical directions, the Manhattan distance is particularly relevant and intuitive.
It accurately reflects the distance one would travel if constrained to moving along the grid lines, making it well-suited for comparing distances between paths in such a scenario.

Other metrics that could be used for comparing distances between paths include:

1. **Euclidean Distance:** This measures the straight-line distance between two points in Euclidean space. While it provides a direct measure of spatial separation, it may not be as appropriate for constrained paths in a grid system because it doesn't account for the grid's structure.

2. **Chebyshev Distance:** Also known as the chessboard distance or maximum metric, it measures the maximum absolute difference between the coordinates of two points. It's suitable for movements in any direction but might not capture the actual path length effectively.

### b) While researching on Transformers you learn about embeddings and how words are transformed into Numerical Vectors of High dimensional space, and stored on what basis the ‘likeliness’ of any two vectors are. For eg. words like ‘happiness’, ‘success’ are more alike to each other on the contrary ‘sadness’ , ‘failure’ are alike to each other but opposite to‘happiness’, ‘success’ . 

What is the common criterion used to define this ‘likeliness’ mathematically between any two words?

**Answer:** **Cosine similarity** is used to define likeliness mathematically here. Dot product of two vector gives cosine similarity between them. Two vectors with high cosine similarity are positioned near to each other in geometric space and are semantically similar to each other.


