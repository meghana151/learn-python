# Slicing Arrays
Slicing of arrays is taking a subset of elements from one index to another index.

**Syntax**
```python
array[start_index: stop_index: step]
```
Where, ‘start_index’ is the index from where we start accessing the elements. ‘stop_index’ is the stopping point. ‘step’ is the interval between each element. The start index is inclusive while the stop index is exclusive.

**Example 1**<br>
```python
import numpy as np
arr = np.array([1,2,3,4,5,6])
print(arr[1:4])
```
**Output**<br>
```python
[2 3 4]  #Since it is a 0-based index, the slicing starts from the 1st index element-‘2’(included) and stops at the 3rd index element-‘4’.
```
<br>

If we do not specify the step, it is taken 1 by default.

**Example 2**<br>
```python
import numpy as np
arr = np.array([1,2,3,4,5,6])
print(arr[1:6:2])
```
**Output**<br>
```python
[2 4 6]  #Here we specified the step as 2, so every second element is taken.
```
<br>

If we do not specify the ‘start_index’, it is considered 0 and starts from the starting element of the array.

**Example 3**<br>
```python
import numpy as np
arr = np.array([1,2,3,4,5,6])
print(arr[:3])
```
**Output**<br>
```python
[1 2 3] 
```
<br>

If we do not specify the ‘stop_index’, it is taken as the length of the array and is considered till the last element.

**Example 4**<br>
```python
import numpy as np
arr = np.array([1,2,3,4,5,6])
print(arr[3:])
```
**Output**<br>
```python
[4 5 6]
```
<br>

Negative slicing is used to access the elements from the end of the given array. ‘-1’ is the last element, ‘-2’ is the second to the last element, and so on. It can also be used to reverse the elements of an array.

**Example 5**<br>
```python
import numpy as np
arr = np.array([1,2,3,4,5,6])
print(arr[-3:-1])
```
**Output**<br>
```python
[4 5]  # Here,the start element is ‘-3’ so the last to the third element is – ‘4’, stop index is ‘-1’ so the last element but since it is exclusive, the element is ‘5’.
```
<br>

### Let us look into two-dimensional arrays now. 
A 2d array is like a nested structure, arrays inside an array. Each element in a 2D array is identified by two indices: one for the row and one for the column. So the syntax will change to  
```python
array[row_start: row_end: row_step, column_start:column_end, column_step]
```
**Example 6**<br>
```python
import numpy as np
arr = np.array([[1, 2, 3],
                [4, 5, 6],
		            [7, 8, 9]])
sliced_arr= arr[0:2, 0:2]
print(sliced_arr)
```
**Output**<br>
```python
[[1 2]
 [4 5]]  #Here, we slice the arrays row-wise and column-wise. First, we start from the 0 index row i.e., the first row till the 1st index row. And slice from 0 index column to 1st index column as 2 is not included.
```
<br>

For a higher dimensional nd array, the basic syntax is 
```python
array[start1:stop1:step1, start2:stop2:step2, ..., startN:stopN:stepN]
```
