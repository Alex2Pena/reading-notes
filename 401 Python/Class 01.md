# A beginner's guide to Big O notation

### BigO - Describes the performace of an algorithm(time  space).
  
### O(1) 
Describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.
```
bool IsFirstElementNull(IList<string> elements)
{
    return elements[0] == null;
}
```

### O(N)
Describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.
```
bool ContainsValue(IList<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true;
    }

    return false;
}
```

### O(N2)
Represents an algorithm whose performance is directly proportional to the square of the size of the input data set.
```
bool ContainsDuplicates(IList<string> elements)
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

### O(2N)
Denotes an algorithm whose growth doubles with each additon to the input data set.
```
int Fibonacci(int number)
{
    if (number <= 1) return number;

    return Fibonacci(number - 2) + Fibonacci(number - 1);
}
```

### O(log N) - Logarithms 
Selects the center or median of data set then divides and conquers by continuing to half the data set.
