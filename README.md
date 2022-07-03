# Trapping-rain-Water
Maximum Index
Medium Accuracy: 42.72% Submissions: 71161 Points: 4

Given an array A[] of N positive integers. The task is to find the maximum of j - i subjected to the constraint of A[i] < A[j] and i < j.
 

Example 1:

Input:
N = 2
A[] = {1, 10}
Output:
1
Explanation:
A[0]<A[1] so (j-i) is 1-0 = 1.

Example 2:

Input:
N = 9
A[] = {34, 8, 10, 3, 2, 80, 30, 33, 1}
Output:
6
Explanation:
In the given array A[1] < A[7]
satisfying the required 
condition(A[i] < A[j]) thus giving 
the maximum difference of j - i 
which is 6(7-1).

 

Your Task:
The task is to complete the function maxIndexDiff() which finds and returns maximum index difference. Printing the output will be handled by driver code. Return -1 in case no such index is found.

Expected Time Complexity: O(N)
Expected Auxiliary Space: O(N)






int maxIndexDiff(int A[], int N) 
    { 
        int c=0;
       int i=0;
       int j=N-1;
       while(i<=j)
       {
           if(A[i]<=A[j])
           {
           c=max(c,j-i);
           i++;
           j=N-1;
           }
           else
           {
               j--;
           }
       }
       return c;
    }

