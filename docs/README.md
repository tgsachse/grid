# grid
This Python class provides self-growing, coordinate-like list functionality where items can be accessed by indexing. See the example below.

# example
```
myGrid = Grid()

# Assign items using a [y, x] indexing scheme.
myGrid[0, 0] = "hello"
myGrid[0, 1] = "world"

# Assign entire rows
myGrid[1] = [x for x in range(10)]
myGrid[2] = 3.1415926

# Assign really far out of bounds because why not?
myGrid[10, 5] = True

# Even assign backwards!
myGrid[-1, 4] = False
myGrid[-2, 0] = "crazy right?"

print(myGrid)
print("\nSpecific accesses:")
print(myGrid[0])
print(myGrid[1, 5])
print(myGrid[-1, 4])
print("\nSize is {0}".format(len(myGrid)))

```
This prints out
```
[hello, world]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[3.1415926]
[]
[]
[]
[]
[]
[]
[crazy right?]
[None, None, None, None, False, True]

Specific accesses:
['hello', 'world']
5
False

Size is 20
```