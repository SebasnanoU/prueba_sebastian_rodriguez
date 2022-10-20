# Question 2 - Section 1

### Statement: 
Given an array A with n as length. Find the maximum contiguous 
subarray, which means, the contiguous subarray which has the largest 
sum of values and returns its sum.

Example:

```
Input: 
[-2, 1, -3, 4, -1, 2, 1, -5, 4],
Output:
6 
Explanation:
[4, -1, 2, 1] hast the largest sum = 6.  
```

### Question:
Write a pseudocode function to solve that problem. Do not forget to 
explain any important aspect of your code, so that anyone can 
understand its implementation.

### Solution:
After analyzing what is required in this program, it is found that the solution is performed by an algorithm called Kadane's Algorithm, which evaluates the array from left to right only by doing one run, making a function of O(n).

```
function max_subarray(arr : integer_array, n : integer, num : integer_array)//The function receives three parameters, two arrays and a number, the first array is the one that stores the section of the current numbers, the second array is the array to evaluate and from where the fragment to return is taken, the number entered is the highest value of the sum of the adjacent values in the array.
posfin = arr.index(n)                                   //The index of the first largest value in the array is found.
arr = arr[:posfin+1]                                    //The array is cut to where the index is indicated.
arrcer = [i for i in range(0, len(arr)) if arr[i]==0]   //The index of all the zeros in the array is found
posini = arrcer[-1]+1                                   //The last index of the previous array is taken
return num[posini:posfin+1]                             //The array is returned only from the start and end index.


function max_subarray(array : integer_array)            //The function receives an array for evaluation.
    integer best_sum = 0                                //Variable to store the cumulative sum
    integer current_sum = 0                             //variable to take the cumulative of the previous and current value
    integer arr = array[0]                              //Array defined to store the sequence of the evaluated numbers to find the final array
    loop ( for x in number:  )                          //Cycle through the original array
        current_sum = max(0, current_sum + x)           //The value carried by the summed cycle is compared with the previous one with 0
        best_sum = max(best_sum, current_sum)           //the accumulated sum is compared with the present value.
        arr.append(current_sum)                         //The current values of each iteration are stored in the array.
    num = mayoracero(arr, best_sum, numbers)            //A second function is called to solve the final array and is stored in a variable
    return num, "hast the largest sum = ", best_sum     //The solution of the exercise is returned with the indicated parameters.
    end_loop
end_function
```
