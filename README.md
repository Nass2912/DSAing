# DSAing
### Big O
# What's Big O ? 
    Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. It allows us to talk formally about how the runtime of an algorithm grows as the input grows.
<<<<<<< HEAD
    So, we say that an algorithm is O(f(n)) if the number of small operations the computer has to do is eventually less than a constant mulitplied by f(n) ,as n increases.
    So, for f(n) to be big O notated, the time to complete it must be constant so , f(n) = 2 . In this case, f(n) takes 2 seconds no matter what n is. So, we say that O(2) meaning the big O notation for this f(n) is 2.
    On the otherhand, if f(n) = n*2, then as n increases the times increases quadratically.

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
=======
    So, we say that an algorithm is O(f(n)) if the number of small operations the computer has to do is eventually less than a constant mulitplied by f(n) ,as n increases. In this case, f(n) takes 2 seconds no matter what n is. So, we say that O(2) meaning the big O notation for this f(n) is 2.
    On the otherhand, if f(n) = n*2, then as n increases the times increases quadratically.
>>>>>>> 1136a9606db90db516a28acb61274758b166a766
