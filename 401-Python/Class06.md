# Random module

**Randint** - Will output a random number between 2 parameters.
```
import random
print random.randint(0, 5)
```
**Random** - for a larger # output
```
import random
random.random() * 100
```
**Choice** - Chooses a random value from a sequence
```
random.choice( ['red', 'black', 'green'] ).
```
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```
**Shuffle** - Shuffles elements inplace so they are in random order
```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```
```
Output:
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
# of course your results will vary
```
**Randrange** - Generate a randomly selected element from range(start, stop, step)
```
random.randrange(start, stop[, step])
```
```
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```
