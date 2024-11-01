# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

To verify the algorithm without access the source code, we can test different sizes and characteristics of the data array.

1. To test the different sizes of the data, for example, doubling the array size each time, starting with a small size, then increase to a larger one.

2. To test the characteristics of the data, for example, using already sorted array, reverse sorted array, same elements array.

To analysis the run time complexity, since the source code is not provided, the time complexity cannnot be estimated as usual. We can use a timer to masure how long it takes to sort the array, then plot the results, with x be the list size, y be the time. If the graph shows a linear relationship between the size and time, it proves X is correct, otherwise, it is not correct.

Theoretically, X could not be correct, becuase the comparsion based sorting algorithm should have a minimum time complexity $O(nlogn)$. This is because in comparsion-based sorting algorithm, each comparsion for between two elements can only have two outputs, first is greater than second or second is greater than first. Based on that, a decision tree can be used to represent this processe, with each node represent a comparsion. For sorting n elements, there are n! possible orderings, so the leaves of the tree is $n!$, and the number of comparsions in the worst case is the depth of the tree, which is at least $log(n!)$, using Stirling's approximation, $log(n!)=nlogn$

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.” --Doris Yan