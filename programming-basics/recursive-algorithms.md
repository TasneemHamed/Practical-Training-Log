# Recursive Algorithms

**What is Recursion?** Recursion is when you have a function that calls itself to solve a problem. This technique breaks down a big task into smaller, manageable parts, each time the function calls itself. You keep doing this until you reach the simplest form of the problem, which you can solve easily.

**Fibonacci Sequence** You've probably heard of the Fibonacci sequence, where each number is the sum of the two preceding ones, starting from 0 and 1. This sequence is a perfect candidate for recursion because to find a Fibonacci number, you just need the two before it, repeatedly, until you reach the base case of 0 or 1.

**Array Sum Example** Imagine you want to sum all the elements in an array. With recursion, you would add the first element to the sum of all the remaining elements. You repeat this process, reducing the size of your problem (the array) each time, until the array is empty, and you can’t go further.

**Recursive Factorial** Calculating the factorial of a number (all the integers from 1 up to that number multiplied together) can also be done recursively. If you need to find the factorial of a number, you multiply it by the factorial of the number one less than it, and so on, until you reach 1.

**Direct and Indirect Recursion** Direct recursion is straightforward: you call the same function from within itself. Indirect recursion involves a bit of a roundabout – you call another function, which in turn calls the original function again. This can be a bit trickier to keep track of but is useful in certain situations.

**Recursive Drawing** Think about drawing a shape, like a snowflake or a tree, where each part of the shape mirrors the whole. Recursively, you can draw these complex patterns by starting with a simple shape and progressively adding smaller versions of the same shape to it.

**Performance: Recursion vs Iteration** While recursion might make your code look clean and elegant, it’s not always the fastest or the most memory-efficient method, especially when compared to loops. Each recursive call uses a bit of memory, and if your problem is too big, you might run out or slow down your program significantly.

**When to Use Recursion** Use recursion for problems where you need to explore different outcomes at each step, like when you’re dealing with combinations or navigating through directories in a computer. It’s also great for problems that naturally fit into smaller repeating problems, like searching and sorting algorithms.

These topics highlight how recursion can be a powerful tool for solving complex problems by breaking them into smaller, more manageable tasks.

<figure><img src="../.gitbook/assets/Screen Shot 2024-04-26 at 2.24.35 AM.png" alt=""><figcaption><p>Haker Rnak HW</p></figcaption></figure>







```javascript
function diagonalDifference(arr) {
    let primaryDiagonalSum = 0;
    let secondaryDiagonalSum = 0;
    let n = arr.length;

    for (let i = 0; i < n; i++) {
        primaryDiagonalSum += arr[i][i];
        secondaryDiagonalSum += arr[i][n - i - 1];
    }

    return Math.abs(primaryDiagonalSum - secondaryDiagonalSum);
}

const matrix = [
    [11, 2, 4],
    [4, 5, 6],
    [10, 8, -12]
];


console.log(diagonalDifference(matrix));  

```

