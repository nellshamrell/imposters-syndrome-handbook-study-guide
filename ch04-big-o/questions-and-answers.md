# Ch04 Big O

## What does Big O represent?

Scale - it mathematically describes the complexity of an algorithm in terms of time and space

## What does O(1) mean? Give an example.

Only one operation is required - i.e. retrieving an element from an array by its index

## What kind of time can O(1) be referred to as?

Constant time

## What does O(n) mean? Give an example.

Perform an operation on each element of an inpute - scale increases as the number of inputs increases.

Summing elements in an array.

```javascript
const nums = [1,2,3,4,5];

let sum = 0;

for(let num of nums) {
    sum += num
}
```

## What kind of time can O(n) be referred to as?

Linear scaling time

## Give an example of a situation where you can make an O(n) solution more efficient.

If you are summing an array and it is a sorted, contiguous array of integers that starts with 1

[1...n]
S = n(n+1)/2

In this case, we do not need to run the iteration and it makes our algorithm O(1) rather than O(n)

## What is O(n^2)? Give an example.

Nested loops - when you iterate over an array then iterate over another array for each element of the first array.

## What is O(log n)? Give an example.

Divide and conquer - often used with searching functions on sorted arrays. Ex: binary search - split a list in half, discard half we don't need, continue splitting until we have the value we are looking for

### Describe this equation in words:

log2(512) = x

"Log base 2 of 512 equals some number x" or "x = to how many times we need to multiply 2 to arrive at 512"

### Describe this equation in words:

log(100) = x

"How many times do you multiply 10 by itself to arrive at 100?"

### What is a binary search?

Splitting a list of numbers in half, continually, until you get down to a single value you want.

**How would you describe this with an equation?**

log2(n) = x

**How would you describe that equation in Big O notation?**

O(log n)

## What is O(n log n)? Give an example.

For each iteration n, search for something in the entire dataset using a binary search. Finding duplicate values in a list of numbers.

### Where is O(n log n) commonly used?

Sorts - quicksorts and merge sorts

### How would you find duplicates in a list of numbers?

Iterate over each number, for each iteration search for that number's duplicate in the entire array.

**What if you could assume there was only one duplicate number?**

You could find out what the sum should be for an array without duplicates

S = n(n+1)/2 where n is that last element of the array (this is O(1))

Then find the actual sum

Then subtract the expected sum from the actual sum.

Then find that number in the array (0(n))

## Describe the relevant Big O notation in these common scenarios:

### Random access to a given element in a collection

O(1)

### List iterations

O(n)

### Nested Loops

O(n^2)

### Divide and Conquer

O(log n)

### Iterations that divide and conquer

O(n log n)

### Adding a nested loop for every input.

O(n!)

## Describe time complexity vs. space complexity

Time is how long it will take to do a given operation, space refers to the resource requirements.

### How does a program remember things as it executes?

It has 2 ways of remembering things - heap and stack.

The stack is how the program remembers the variables in the scope of the currently executing routine.  When a variable is declared in a block of code, it is stored on the stack. When the block of code goes out of scope, the variable is removed from the stack. This means you can easily run out of resources before you run out of time - Stack Overflow exception. This often happens with a recursive routine - each value will remain on the stack until all functions have executed.