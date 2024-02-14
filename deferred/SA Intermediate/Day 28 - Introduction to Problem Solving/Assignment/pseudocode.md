Q1CountFactors

    Brute force approach
    1. Initialize count variable to zero
    2. All factors for a number N will be in the range [1, N]
    3. Iterate over each number from 1 till N
        a. If a number divides N without any remainder, it is a factor i.e. (N%i == 0)
        b. Increment count for no remainder
    4. Return count after end of loop

    Optimisation
    1. The Brute force will iterate N times for N input
    2. Under observation, If N%i == 0 then N/i and i both are factors of input
    3. We need to iterate till N/i and i both reach it's maximum value at once 
        i.e. N/i = i => N = i*i 
    4. Either find square root of input or simply in for loop modify condition from i<=N to i*i <= N
    5. Since if i divides N, then we can conlude i and N/i as factors
        a. increment count by 2 for each i divides N
        b. When i == N/i 
            increment count by 1
    6. Return count

Q2IsPrime

Definition of Prime numbers - Integer numbers which have only 2 integer factors
    
    Current Optimisation
    1. Fetch number of factors from the CountFactors function
    2. If count == 2 then prime, else non-prime

Q3PerfectSquareRoot

    Current approach
    1. Iterate till i*i <= N 
    2. For perfect square root i*i == N, for step value of square root i*i <= N

Q4SumEvens

    Brute force
    1. Iterate from 2 till i <= N, increment by 2
    2. Add each index to a sum variable (initilized out of the loop to zero)

    Optimised approach
    1. Similar to sum of all numbers from 1 to N is N*(N+1)/2, deduce the equation for sum of all even numbers from 1 to N when N is odd and when N is even


