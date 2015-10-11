[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner1.png">](https://github.com/txt/mase/blob/master/README.md)   
[At a glance...](https://github.com/txt/mase/blob/master/OVERVIEW.md) |
[Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) |
[Models](https://github.com/txt/mase/blob/master/MODELS.md) |
[Code](https://github.com/txt/mase/tree/master/src) |
[Lecturer](http://menzies.us) 


What is the problem with local maxima?

1. In the following diagram, each square has the same x,y,z axis. What might the names of those x,y,z values?
![](https://github.com/timm/sbse14/wiki/etc/img/landscape/WrightFitness.jpg)

2. Explain the following, using the above diagram:

 * Holes
 
    The Holes are the pitfall regions of the diagram denoted by the symbol '-'

 * Poles
 
    The poles are the mountain regions of the diagram denoted by the symbol '+'

 * Saddles
 
    The saddle is the region of flat space between a pole '+' and a hole '-'. 
 * Local minima
 
    A point is termed as the local minima if it has the lowest value amongst all its neighbourhood values. The regions marked '-' are regions of local minima which may or may not be the global minima.
 * Flat
 
    A flat region in the above diagram is a landscape of the chart that is completely flat. A value in the flat region is neither better nor worse than its neighbours.

 * Brittle
    

3. Explain the following term and describe how it handles the problem of flat: Retries.

  Sometimes it may so happen that we may get stuck in a region of the landscape where we will not make good progress(e.g. flat space). Instead of trying to cross this flat region in the hopes of finding a good solution at the end, it is advisable to forget everything and start from scratch again. This forms the basis of retries. Using retry we eject ourselves into another region of the landscape and begin a fresh search for a good soluton.

4. How does the following techniques avoid the problems of local maxima?

  Simulated annealing
    - Retries
    - Momentum (make sure you explain momentum)
  
5. Local search can be characterized as follows

   + Jump all around the hills
   + Sometimes, sitting still while rolling marbles left and right
   + Then taking one step along the direction where the marbles roll the furthest.
   + Go to 1.

In the following code snippet, explain where you'd find 5.
```
FOR i = 1 to max-tries DO
  solution = random assignment
  FOR j =1 to max-changes DO
    IF  score(solution) > threshold
        THEN  RETURN solution
    FI
    c = random part of solution 
    IF    p < random()
    THEN  change a random setting in c
    ELSE  change setting in c that maximizes score(solution) 
    FI
RETURN failure, best solution found
```


_________

<img align=right src="https://raw.githubusercontent.com/txt/mase/master/img/pd-icon.png">Copyright © 2015 [Tim Menzies](http://menzies.us).
This is free and unencumbered software released into the public domain.   
For more details, see the [license](https://github.com/txt/mase/blob/master/LICENSE.md).

