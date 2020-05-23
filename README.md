# GeoDist
## The geodesic (great-circle) that minimices the total cross distances to a series of given points on Earth's surface.

## Presentation
Given a series of points on the Earth's surface: which is the geodesic (great-circle) that minimizes the total distance between it and the reference points?

There may be an analytical solution but it seems complicated enough, so I have taken a numerical approach.
The expressions are taken from [MOVABLE-TYPE](https://www.movable-type.co.uk/scripts/latlong.html).

Attached is a Jupiter Notebook that provides a solution based on a double iteration:
* it starts navigating through a random selection of great-circles, looking for those which minimize the total sum, 
* then refines the result with a gradient search with the same objective.

## Results
The script provide visual checks on the convergence of the random approach:
![number of iterations](https://github.com/Rigonz/GeoDist/blob/master/Pics/Convergence%20R0.png)
![path of solutions](https://github.com/Rigonz/GeoDist/blob/master/Pics/Convergence%20R1.png)

Finally, it also provides a representation of the added distance from the set of points to "all" great-circles:
![all distances](https://github.com/Rigonz/GeoDist/blob/master/Pics/GEODIST_out%20R0.png)
