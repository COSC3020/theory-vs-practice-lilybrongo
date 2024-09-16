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

      1. Asymptotic comparisons can be misleading because dependent on the size of the array, the cases may differ. 
      (Graphs from lecture show that the longer the run time allows for more change to occur)

      2. Asymptotic comparisons can be misleading because they can also depend on implementation. This means that the expected "best case" may not be the best. Since asymptotic comaprisons are considered to be loose bound, this can lead to a misleading representation of the effectivness of the implementation. 

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

      1. Timing of inserting elements, along with creating a balanced tree may not have been accounted for
      2. The implementation of the code could also lead to this timing difference. If other things have been added into the program, then this could easily change the run time which would not only be accounting for the algorithm itself. It would have to account for the other operations and added information, along with the element increase. 
      3. Since asymptotic comaprisons are dependent on their environment, with this many elements there may not be proper allocation of memory, or due to the size it may create a greater inefficiency to the expected timing. 