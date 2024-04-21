# DSAing

### Big O

# What's Big O ?

    Big O notation is a mathematical notation used to describe the asymptotic upper bound or worst-case scenario of the time or space complexity of an algorithm in computer science. It provides a way to quantify the efficiency of an algorithm by expressing how its performance or resource usage scales with the size of the input.

    Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. It allows us to talk formally about how the runtime of an algorithm grows as the input grows. Big O concern is to find the upper bound / infinity.

    In simpler terms, Big O notation tells us how the runtime or memory usage of an algorithm grows relative to the size of its input.

# Counting Operations

    So, suppose we have this function below.
        function upToN(){
            let total = 0; // assignment is 1st operation
            for(let i =0 // assignment is 2nd operation ; i<=n // n comparisons ;i++ // n additions and n assignments){
                total += i // n addition and n assignments
            }
            return total;
        }
    So depending on the data of n,  here we have an operation count ranging from as low as 2n + 5 upto 5n + 2. But regardless of the exact number, the number of operations grows roughly proportionate to n. If n doubles, so would the number of operations.
    So, we say that an algorithm is O(f(n)) if the number of small operations the computer has to do is eventually less than a constant mulitplied by f(n) ,as n increases. In this case, f(n) takes 2 seconds no matter what n is. So, we say that O(2) meaning the big O notation for this f(n) is 2.
    On the otherhand, if f(n) = n*2, then as n increases the times increases quadratically.

# Simplifying Big O (assumptions)

    When determining time complexity, we are going to follow these rules of thumb to make it simpler
        1. We don't count constants
            so,
            O(2n) is simplified as O(n)
            and
            O(500) is simplified as O(1)
            and
            O(13n*2) is simplified as O(n*2)
        2. Smaller terms don't matter
            so,
            O(10n) is simplified as O(n)
            and
            O(1000n + 50) is simplified as O(n)
            and
            O(n*2 + 50n + 8) is simplified as O(n*2) , since if n is 1000, n*2 gives us 1,000,000 and 50n gives us 50,000 . So it it pretty insignificant compared to a million.
        3. Arithmetic Operations are constants.
        4. Variable Assignments are constants.
        5. Accessing an element in an array or object (by index or by key) is constant
        6. In a loop, the complexity is the length of the loop times the complexity of whatever happens inside of it

# Key Concepts (time and space complexity)

    Time Complexity: This refers to the amount of time an algorithm takes to complete as a function of the size of its input. Big O notation is often used to express the upper bound of the time complexity in terms of the input size (n).

    Space Complexity: This refers to the amount of memory space an algorithm requires as a function of the size of its input. Similar to time complexity, Big O notation can also be used to express the upper bound of the space complexity.

    Asymptotic Analysis: Big O notation focuses on the behavior of an algorithm as the size of the input approaches infinity. It disregards constant factors and lower-order terms, focusing only on the dominant term that has the greatest effect on the algorithm's performance for large inputs.
    Types of Complexity:
        O(1): Constant time complexity. The algorithm's runtime or space usage remains constant regardless of the size of the input.

        O(log n): Logarithmic time complexity. The algorithm's runtime or space usage grows logarithmically as the size of the input increases.

        O(n): Linear time complexity. The algorithm's runtime or space usage grows linearly with the size of the input.

        O(n log n): Linearithmic time complexity. Common in efficient sorting algorithms like merge sort and quicksort.

        O(n^2): Quadratic time complexity. The algorithm's runtime or space usage grows quadratically with the size of the input.

        O(2^n): Exponential time complexity. The algorithm's runtime or space usage doubles with each additional input element.

        O(n!): Factorial time complexity. The algorithm's runtime or space usage grows factorially with the size of the input, making it extremely inefficient for large inputs.
        Best, Worst, and Average Case: Big O notation typically describes the worst-case scenario, but it's important to consider best and average-case complexities for a comprehensive understanding of an algorithm's performance.

# Space Complexity

    Space complexity refers to the amount of memory space required by an algorithm or a program to execute in a given environment. It's a measure of how much memory an algorithm consumes with respect to the size of its input.

    When analyzing space complexity, we consider the memory required for:

    Fixed memory: This includes the memory required by the code itself, as well as global variables and constants. This part of memory consumption does not vary with the size of the input.
    Variable memory: This includes the memory required for variables that change in size as the input size increases. This may include data structures like arrays, matrices, trees, etc., that are dynamically allocated during the execution of the algorithm.
    Space complexity is typically expressed using Big O notation, just like time complexity. For example, if an algorithm's space complexity is O(n), it means that the amount of memory it requires grows linearly with the size of the input.

# Logarithms Recap after 10+ years !!

    Logarithms are mathematical functions that describe the relationship between exponential growth and its inverse, exponential decay. They are essentially the inverse operations of exponentiation.
    (Exponential decay is a mathematical concept that describes the process of something decreasing over time at a rate proportional to its current value. It's the opposite of exponential growth, where something increases over time at a rate proportional to its current value.)
    Let's break it down:

    1. **Exponential Function**: An exponential function is one where the variable is in the exponent. For example, \(f(x) = a^x\), where \(a\) is a constant (the base) and \(x\) is the variable. Exponential functions can grow very rapidly as \(x\) increases.

    2. **Inverse Operation**: An inverse operation undoes another operation. In the case of exponentiation, the inverse operation is logarithm.

    3. **Logarithm**: The logarithm of a number is the exponent to which a given base must be raised to obtain that number. Mathematically, if \(y = \log_a(x)\), then \(a^y = x\), where \(a\) is the base, \(x\) is the argument, and \(y\) is the logarithm.

    For example, in base 10 logarithms (common logarithms), if \(y = \log_{10}(1000)\), then \(10^y = 1000\). Here, \(y = 3\) because \(10^3 = 1000\), so \(\log_{10}(1000) = 3\).
