---
marp: true
theme: default
paginate: true
footer: 'Derivation of Time Complexities'
---

<!-- _class: lead -->
# Derivation of Time Complexities
### Algorithms and Data Structures
### Christoph Brauer
### Date: 28th March 2023

---

<!-- Speaker notes -->
<!-- Notes: Welcome everyone to this presentation on the derivation of time complexities in the context of algorithms and data structures. We'll be covering the importance of time complexity, asymptotic notations, and how to analyze loops. -->

---

## Introduction to Time Complexity

- Measure of efficiency of an algorithm
- Function of the number of input elements
- Helps to compare different algorithms

<!-- Notes: Time complexity is a measure of the efficiency of an algorithm, expressed as a function of the number of input elements. It helps us to compare different algorithms and choose the most efficient one for a given task. -->

---

## Importance of Time Complexity in Algorithms

- Optimal resource usage
- Scalability
- Better understanding of the algorithm's behavior

<!-- Notes: Analyzing time complexity is crucial for optimal resource usage, ensuring scalability, and obtaining a better understanding of the algorithm's behavior in terms of its input size. -->

---

## Asymptotic Notations

- Big O Notation (O): Upper bound
- Big Omega Notation (Ω): Lower bound
- Big Theta Notation (Θ): Tight bound

<!-- Notes: Asymptotic notations are used to describe the growth rate of an algorithm's time complexity. Big O notation is the upper bound, Big Omega notation is the lower bound, and Big Theta notation is the tight bound, which represents both upper and lower bounds. -->

---

## Analyzing Loops (Counting Steps)

- Identify the basic operation
- Count the number of basic operations
- Express the count in terms of input size

<!-- Notes: To apply asymptotic notation for analyzing loops, first identify the basic operation of the loop, which is the operation that contributes the most to the time complexity. Next, count the number of basic operations executed, and express this count in terms of the input size. This will help us to determine the time complexity. -->

---

## Example 1: Linear Algorithm

```python
def linear_algorithm(arr):
    sum = 0
    for x in arr:
        sum += x
    return sum
```

Time Complexity: O(n)

<!-- Notes: Here is an example of a linear algorithm, which calculates the sum of elements in an array. The time complexity of this algorithm is O(n), as the loop iterates once for each element in the input array. -->

---

## Example 2: Quadratic Algorithm

```python
def quadratic_algorithm(arr):
    count = 0
    for i in range(len(arr)):
        for j in range(i + 1, len(arr)):
            if arr[i] > arr[j]:
                count += 1
    return count
```

Time Complexity: O(n^2)

<!-- Notes: This is an example of a quadratic algorithm, which counts the number of inversions in an array. The time complexity of this algorithm is O(n^2) because it has a nested loop, and the loops depend on the size of the input array. -->

---

## Example 3: Logarithmic Algorithm

```python
def binary_search(arr, target):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1
```

Time Complexity: O(log n)

<!-- Notes: This example demonstrates a logarithmic algorithm, which performs a binary search in a sorted array. The time complexity of this algorithm is O(log n) because it repeatedly divides the search interval in half, narrowing it down until the target element is found or the search interval is empty. -->

---

## Conclusion

- Importance of time complexity in algorithms
- Asymptotic notations: Big O, Omega, and Theta
- Analyzing loops using asymptotic notations

<!-- Notes: In this presentation, we discussed the importance of time complexity in algorithms, the concepts of asymptotic notations (Big O, Omega, and Theta), and how to apply these notations for analyzing loops. This knowledge will help you better understand and optimize the efficiency of your algorithms. Thank you for your attention! -->