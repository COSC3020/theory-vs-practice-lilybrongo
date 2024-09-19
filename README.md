# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

       
Add your answers to this markdown file.

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

      1. Asymptotic analysis does not account for constants. Even though they do affect the run time, the complexity is used to explain how the runtime should be, not the actual outcome. Since it is typical to ignore the constant, in situations where constant factors could dominate the run time, an asymptotically algorithm may perform better than the origionally percieved algorithm.

      2. Asymptotic analysis does not account for lower order terms. In practice with say n^6 and n^7, n^6 is disreagrded even though it would make a difference in the runtime. 

      3. Asymptotic comparisons are also dependent on their environment. The hardware itself is not typically taken into consideration which can modify the best, average, and worst case.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

    A binary search tree has an asymptotic complexity of O(log(n)), knowing this we can assume log(1,000) and for this problem log(10,000)

    log(1000) ≈ 10 seconds (9.965784285 seconds)
    log(10,000) ≈ 13.3 seconds (13.28771238 seconds)

    In order to find the timing for 10,000 elements we can divide the two numbers and multiply it by the 5 seconds it took for the 1,000 elements

    log(10,000) / log(1,000) ≈ 13.3 / 10 ≈ 1.33 x 5 = 6.65 seconds

    We can now assume that it would take around 6.65 seconds to find the same element in a search tree with 10,000 elements


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

    This could be the case because 

      1. If the tree is not balanced then this could lead to a longer run time. If this is the case then it would lead to worst case scenerio instead of returning the estimated best case asymptotic analysis 
      2. The implementation of the code could also lead to this timing difference. If other things have been added into the program, then this could easily change the run time which would not only be accounting for the algorithm itself. It would have to account for the other operations and added information, along with the element increase.
        - An example of this could be a specific check or test within a program that were not accounted for within the asymptotic analysis. Also if the algorithm was implemented incorreclty this would also account for a slower time.
      3. Since asymptotic comaprisons are dependent on their environment, with this many elements there may not be proper allocation of memory, or due to the size it may create a greater inefficiency to the expected timing.
      - An example of this would be hardware that can run faster and has a greater memory capacity, with these qualities it will be able to run the algorithm faster.



Used Lecture 16: Introduction to Asymptotic Analysis
https://www.cs.cornell.edu/courses/cs312/2004fa/lectures/lecture16.htm

  I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.
