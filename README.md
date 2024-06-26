# DSAing

### Data Structures

    A data structure is a way of organizing and storing data in a computer so that it can be accessed and manipulated efficiently. Think of it as a framework that defines how data is stored, arranged, and operated upon in a computer program.

    Data structures provide various operations such as insertion, deletion, searching, and traversal. Different data structures are optimized for different types of operations, and the choice of data structure can significantly impact the performance and efficiency of algorithms and programs.

    Common examples of data structures include arrays, linked lists, stacks, queues, trees, graphs, hash tables, and heaps. Each has its own strengths and weaknesses, and the choice of which to use depends on factors such as the specific requirements of the problem being solved, the type of operations that need to be performed frequently, and the efficiency requirements of the application.

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

# Objects in big O

    So, an object is an unordered way of storing data, like below:
        let instructor = {
            name: "telles",
            isInstructor: true,
            favoriteNumbers: [1,2,3,4]
        };

    and any action, to read, create, delete is O(1),
    while searching through the array is O(n), which is dependent on the object size.

    All the following methods on objects have these big O notation
    Object.keys => O(n) since it iterates over every element and extract the keys
    Object.values => O(n)
    Object.entries => O(n)
    Object.hasOwnProperties => O(1)

# Arrays in big O

    Contrary to objects, arrays is an ordered way to store data.
    so, we may have this array below:
        let team = ['tej', 'mika', 'greg']
        So,
        To access any element in the array is O(1), no matter how big it is, since arrays are indexed
        To search for an element is O(n), since we potentially have to go through every element
        To insert and remove depends on where we want to do it. For example if we add/remove from the end of the array, that is going to be O(1), but if we add/remove from the start, it becomes O(n), since the array indexing needs to be changed for every consequent item in our array, so the reindexing needs to happen for every element, hence O(n)
        So, in summary:

        push - O(1)
        pop - O(1)
        shift - O(n)
        unshift - O(n)
        concat - O(n)
        slice - O(n)
        splice - O(n)
        sort - O(n * log n)
        map/foreach/filter/reduce - O(n)

### Algorithms and Problem solving GamePlan ⛹️

# What is an algorithm?

    An algorithm is a step-by-step procedure or set of rules used to solve a problem or perform a specific task. It's essentially a sequence of well-defined instructions that are designed to achieve a particular outcome.

    Simply put, a process or set of steps to accomplish a certain task.

# GamePlan ⛹️

    1. Understand the problem
        .Be able to restate it in your own words
        .What are the inputs
        .What are the expected outputs
        .How to label/name the important pieces of data that are part of the problem

        So for example we have this
        // Write a function that takes two numbers and return their sum //
            .Be able to restate it in your own words
                "Do addition of 2 numbers"
            .What are the inputs
                integers ? floats ...
            .What are the expected outputs
                integer ? float ? string
            .How to label/name the important pieces of data that are part of the problem
                the function name will be add, the two params will be num1 and num2, the result will be called sum

    2. Concrete examples
        So, kindof TDD here, we write the functions with the expected output.
        we start with simple ones, to more complex ones, some with empty inputs, invalid inputs and edge cases to finish with. So, let's take the problem below :

        // Write a function which takes in a string and returns counts of each character in the string
            .Be able to restate it in your own words
                "Return occurence of every character in a string"
            .What are the inputs
                string
            .What are the expected outputs
                object, eg {a: 4}
            .How to label/name the important pieces of data that are part of the problem
                the function name will be charCount, the param will be inputString, the result will be called count

            .Concrete Examples :
                charCount("aaaa")  => {a: 4}
                charCount("hello")  => {h: 1, e: 1, l:2, o:1}
                charCount("hello world")  => {h: 1, e: 1, l:2, o:1} , should we account for empty spaces
                charCount("hello world 12312 #$%")  => {h: 1, e: 1, l:2, o:1} , what about special characteers and numbers ?
                charCount("hello Hi")  => {h: 1} , is it case insensitive?

    3. Break It down
        No need for pseudocode necessarily, comments work too!! The basics is good enough
        SO, let's go simple

        const countChar = (str) => {
            <!-- Iterate over every element in the string -->
            <!-- ignore unecessary values (#$%^) -->
            <!-- Downcase letters -->
            <!-- add it to object count, create key if not yet available -->
            <!-- returns an object with keys that are lowercase alphanumeric characters in the string -->
            return obj;
        }

        const countChar = (str) => {
            let obj = {};
            const alphaRegex = /[a-z0-9]+/i;
            for(let abet of str){
                abet = abet.toLowerCase();
                if(!abet.match(alphaRegex)) continue;
                Object.keys(obj) ? Object.keys(obj).includes(abet) ? obj[abet] ++ : obj[abet] = 1 : obj[abet] = 1 ;

            }
            return obj;
        }

        refactored and simplified
            const countChar = (str) => {
                let obj = {};
                const alphaRegex = /[a-z0-9]+/i;
                for(let abet of str){
                    abet = abet.toLowerCase();
                    if(!abet.match(alphaRegex)) continue;
                    obj[abet] > 0 ? obj[abet] ++ : obj[abet] = 1 ;
                }
                return obj;
            }

# Common Problem Solving patterns

### Frequency Patterns

# Prolemo Uno 1

    We use objects or sets to collect values or frequency of values. This avoid the need for nested loops O(n^2)
    eg:
    Write a method called same which accept 2 arrays and returns true if every value in the array has it's corresponding value squared in the second array. The frequency of values must be same

    const same = (arr1, arr2) => {
        let result = true;
        if(arr1.length !== arr2.length){
            return false;
        }
        arr1.forEach((el) => {
            if(arr2.includes(el * el)){
                arr2.splice( arr2.indexOf(el * el) ,1)
            }else {
                result = false
            }
        })
        return result;
    }

    same([1,2,3,7], [1,9,4,4])
    For this function Big O notation is O(n^2). The forEach loop is O(n) and nested in it there is the includes, another O(n) . We avoid nested loops as much as we can, since the big O becomes quadratic!

    So, to refactor this we can do the following
        const same = (arr1, arr2) => {
            let freqCounter1 = {}
            let freqCounter2 = {}
            for(let val of arr1){
                freqCounter1[val] = (freqCounter1[val] || 0) + 1
            }
            for(let val of arr2){
                freqCounter2[val] = (freqCounter2[val] || 0) + 1
            }
            for(let key in freqCounter1){
                const valContains = (key * key) in freqCounter2
                const freqSame = freqCounter1[key] == freqCounter2[key*key]
                if(!valContains || !freqSame){
                    return false;
                }
            }
            return true;
        };

        Now, this might seems longer, but in term of time complexity, it is better.
        we have 3 seperate for loops, so it is O(3n), which is simplified to O(n)

# Prolemo Dos 2

    Given 2 strings, write a function to determine if the second string is an anagram of the first.Return true if it is the case.(An anagram is a word formed by rearranging the letters to make a new word eg: cinema's anagram is iceman)

        const validAnagram = (str1, str2) => {
            if(str1.length != str2.length){
                return false;
            }
            const freqCounter1 = {};
            const freqCounter2 = {};
            for(let letter of str1){
                letter = letter.toLowerCase()
                freqCounter1[letter] = (freqCounter1[letter] || 0) + 1;
            }
            for(let letter of str2){
                freqCounter2[letter] = (freqCounter2[letter] || 0) + 1;
            }
            for(let key in freqCounter1){
                const valContains = key in freqCounter2
                const freqSame = freqCounter1[key] == freqCounter2[key]
                if(!valContains || !freqSame){
                    return false;
                }
            }
            return true
        }

        or simpler
            const validAnagram = (str1, str2) => {
                if(str1.length != str2.length){
                    return false;
                }
                const freqCounter2 = {};
                for(let letter of str2){
                    freqCounter2[letter] = (freqCounter2[letter] || 0) + 1;
                }
                for(let letter of str1){
                    if(!freqCounter2[letter]){
                        return false;
                    }else {
                        freqCounter2[letter] -= 1
                    }
                }
                return true
            }

            validAnagram("aaz", "zaa")

        validAnagram("aaz", "zza")

### Multiple Pointer Pattern

The multiple pointer pattern is a technique to solve problems efficiently, particularly in arrays, linked lists, or strings. It involves using multiple pointers (usually two or more) to traverse the data structure in a specific way, often to find a solution in linear or sublinear time complexity.

# Problemo Tres 3

    Write a method that return an array of two numbers which sums up to 0 from a sorted array of numbers
    for example [-5,-4,-3,0,2,3,4] should return us [-4,4]
        Costly Version using nested for loops :-
        const sumPairFinder = (arr) => {
            for(let i = 0 ; i < arr.length ; i++){
                for(let j = 0; j < arr.length ; j++){
                    if(arr[i] + arr[j] === 0){
                        return [arr[i],arr[j]]
                    }
                }
            }
            return "no match"
        }

        More efficient version like below would use a pointer system, one from the start and another at the end of the array. We then compare the first one with the last one, if the sum is greater than 0, it means that the value at the end of the array is too big.(Remember, this is a sorted array). Then we move to the before last element in the array and so on. In the case that the sum is less than zero, this means that the LHS is too small, we then move to the second element of the array and see if we get our zero back.

        const efficientSumPairFinder = (arr) => {
            let start = 0;
            let end = arr.length - 1;
            while (start < end){
                let sum = arr[start] + arr[end];
                if(sum === 0){
                    return [arr[start], arr[end]]
                }else if (sum > 0) {
                    end --
                }else {
                    start ++
                }
            }
            return "no value"
        }
        console.log(efficientSumPairFinder([-5,-4,-3,3,4,5]))

# Problemo Quattro 4

    Implement a method called countUniqueValues which accepts a sorted array, and counts the unique values in the array. There can be negative values in the array, but they will be sorted.

    const countUniqueValues = (arr) => {
        let first = 0;
        let last = arr.length
        let sum = 0;
        while(first < last){
            const same = arr[first] === arr[first + 1]
            if(!same){
                sum += 1
            }
            first ++
        }
        return sum ;
    }

    or simpler
        const countUniqueValues = (arr) => {
            let i = 0;
            for(let j = 1 ; j < arr.length ; j ++){
                if(arr[i] != arr[j]){
                    i++
                    arr[i] = arr[j]
                }
            }
            return i + 1
        }
        console.log(countUniqueValues([1,1,1,2,3,4,4]))

### Sliding Window Pattern

The sliding window pattern is mainly used when invloved with problems involving arrays or strings. It's especially handy for problems where you need to find a substring, subarray, or any other data subset satisfying certain constraints.

The sliding window pattern involves creating a window of a certain size (can be fixed or variable) and moving that window across the given data structure (like an array or string) to perform some operation within the window.

# Problemo Cinqo 5

    Write a method called maxSubarraySum which accepts an array of integers and a number called n and the function returns the maximum sum of n consecutive elements in the array.

    costly version O(n^2)
        const maxSubarraySum = (arr, num) => {
            let maxSum;
            for(let i = 0 ; i < arr.length - num ; i++){
                let temp = 0;
                for(let j = 0 ; j < num ; j++){
                    temp += arr[j]
                }
                if(temp > maxSum){
                    maxSum = temp
                }
            }
            return maxSum;
        }
        maxSubarraySum([1,2,3,4,2,3,1,2,3], 3)

    Using thw sliding window pattern, we achieve O(n), We do not need to recalculate all 3 digits at index 1,2,3 when we calculated the sum of 0,1,2. We could just remove the number at index 0 and add the number at index 3.


        const maxSubarraySum = (arr, num) => {
            let maxSum = 0;
            for(let i = 0 ; i < num ; i++){
                maxSum += arr[i]
            }
            let tempSum = maxSum
            for(let j = num; j < arr.length ; j++){
                tempSum = tempSum + arr[j] - arr[j-num]
                maxSum = Math.max(maxSum, tempSum)
            }
            return maxSum;
        }
        maxSubarraySum([1,2,3,4,2,3,1,2,3], 3)
