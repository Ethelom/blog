# Panel Data

In computing, **row-major order** and **column-major order** are methods for storing multidimensional arrays in linear storage such as random access memory (RAM). [[1]](https://en.wikipedia.org/wiki/Row-_and_column-major_order)

The difference between the orders lies in which elements of an array are [contiguous](#memory-contiguity) in memory. <br>
In row-major order, the consecutive elements of a row reside next to each other, whereas the same holds true for consecutive elements of a column in column-major order.

To better illustrate this, take a glance below:

| ![row_and_column_major_order](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4d/Row_and_column_major_order.svg/360px-Row_and_column_major_order.svg.png) | 
|:--:| 
| *Since a 2D array should be stored in linear storage we need a technique to flatten the array. Starting from the first element of the array (a<sub>11</sub>) simply follow the red/blue arrow each time to see the sequence in which elements are stored in RAM* |

## Memory Contiguity
According to [Merriam-Webster](https://www.merriam-webster.com/dictionary/contiguous), contiguous means:

> being in actual contact / touching or connected throughout in an **unbroken** sequence


```py
# example python code
import pandas as pd
df = pd.DataFrame(...)
```

