# Pain vs. Suffering
everyone is expected to face pain in some level of their lives, if that happened to you, ask for remedy! Ask questions that may be the answer to all your thoughts. search more! gatther informations and knowledge you need.

seek the solution to all your problems, that makes the pain power.
you, after this course is expected to master python and use it in many fields,

# Big O
Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

## O(1)
O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.
```
bool IsFirstElementNull(IList<String> elements)
{
    return elements[0] == null;
}
```
## O(N)
O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

```bool ContainsValue(IEnumerable<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true; 
    }     
    return false; 
}
```
## O(N²)
O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N³), O(N⁴) etc.

``` bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++) 
    {
        for (var inner = 0; inner < elements.Count; inner++) 
        { 
            // Don't compare with self 
            if (outer == inner) continue;             
            
            if (elements[outer] == elements[inner]) return true; 
        }
    }    
    return false;
} 
```
## O(2^N)
O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set. The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. An example of an O(2^N) function is the recursive calculation of Fibonacci numbers:

``` int Fibonacci(int number)
{
    if (number <= 1) return number;
       
    return Fibonacci(number - 2) + Fibonacci(number - 1); 
}
```

# Python names and values
name assignment to value:
```x = 25
print(x) 
# output: 25
```
***NOTICE THAT NAMES ARE REASSIGNED INDEPENTlY***
reference can be more than just a name
```names = [1,2 3, 4]
x = names[2]
# x = 3
```
***NOTICE THAT FUNCTIONS ARGUMENTS ARE ASSIGNMENTS***
``` # python suppports tha call by value/reference just like other languaes```

