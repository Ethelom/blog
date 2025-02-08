# Panel Data

In computing, **row-major order** and **column-major order** are methods for storing multidimensional arrays in linear storage such as random access memory (RAM). [[1]](https://en.wikipedia.org/wiki/Row-_and_column-major_order)

The difference between the orders lies in which elements of an array are [contiguous](#memory-contiguity) in memory. <br>
In row-major order, the consecutive elements of a row reside next to each other, whereas the same holds true for consecutive elements of a column in column-major order.

To better illustrate this, take a glance below:

| ![row_and_column_major_order](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4d/Row_and_column_major_order.svg/360px-Row_and_column_major_order.svg.png) | 
|:--:| 
| *Since a 2D array should be stored in linear storage we need a technique to flatten the array. Starting from the first element of the array (a<sub>11</sub>) simply follow the red/blue arrow each time to see the sequence in which elements are stored in RAM* |

### Example
Consider the following 2D array:


$$
A = \left(\begin{array}{ccc}
      a_{11} & a_{12} & a_{13} \\
      a_{21} & a_{22} & a_{23}
    \end{array} \right)
$$

The matrix could be stored in these two ways:

|Memory Address|Row-major order|Column-major order|
|:--:|:--:|:--:|
|0xb02f1a|a<sub>11</sub>|a<sub>11</sub>|
|0xb02f1b|a<sub>12</sub>|a<sub>21</sub>|
|0xb02f1c|a<sub>13</sub>|a<sub>12</sub>|
|0xb02f1d|a<sub>21</sub>|a<sub>22</sub>|
|0xb02f1e|a<sub>22</sub>|a<sub>13</sub>|
|0xb02f1f|a<sub>23</sub>|a<sub>23</sub>|

## Memory Contiguity
According to [Merriam-Webster](https://www.merriam-webster.com/dictionary/contiguous), contiguous means:

> being in actual contact / touching or connected throughout in an **unbroken** sequence


```py
# example python code
import pandas as pd
df = pd.DataFrame(...)
```

- [Test](test.md)
