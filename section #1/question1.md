# Question 1 - Section 1

### Statement: 
Check the following pseudocode function:

```
function Doubler(number : integer)
    integer i = 1
    loop (while i < number)
        i = i * 2
        Display(i)
    end loop
end function
```

### Question:
What is the big O notation which describes in a better way its worst-case?

### Solution:
The following code is analyzed

```
function Doubler(number : integer)
    integer i = 1              //O(1)
    loop (while i < number)    //O(n)
        i = i * 2              //O(n)
        Display(i)             //O(1)
    end loop
end function
```

The big o notation indicates that all the results of each procedure defined in the function are added up and the most significant one is taken, being in this case a result of O(n).

