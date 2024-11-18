# dtw_plot
DTW

**Dynamic Time Warping (DTW)** is an algorithm that can be used to determine the similarity between two time-series sequences. Usage of DTW is advantageous over methods that perform a direct comparison of time-series sequences like Euclidean Matching because of the flexibility inherent to DTW towards misalignment and stretching of time-series signals. As shown in Figure 1, DTW is better able to detect contour similarity between two time-series signals while Euclidean Matching could yield results that imply dissimilarity when two time-series signals actually have similar contours.

![Alt text](./images/f1.png?raw=true "Title")

We can perform DTW on two signals to determine their similarity by filling out a grid with the computational algorithm shown in Figure 2.

![Alt text](./images/f2.png?raw=true "Algo")

After filling out the grid, we identify the lowest path along the grid from the start (bottom left) to the end (top right). This path is identified by starting with the the cell at the top right and moving towards the bottom left diagonally, left, or down at each step, choosing the smallest value among the options. In the event of a tie between the values, move diagonally. An example can be seen in Figure 3, where the path is 1- 1- 1- 2- 2- 2- 3- 4- 5.


![Alt text](./images/f3.png?raw=true "DTW Example")

The resultant path is then converted to a distance value using a distance formula, **the smaller the value the more similar two signals are said to be according to DTW.**
