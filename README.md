# DSARoadmap_DAY1-2

Day 1 & 2 Progress:

Method to find the time complexity (Big O notation) of any algorithm: 

1. Drop the non-dominant terms.
       - do not consider the time complexity of terms that are very minute or not depending on N when compared to the terms depending on N. 
       - only take the terms with higher N order.
2. Drop the constant terms.
       - If you have time complexity as Tn = K1 + K2*n, drop K1 as it is non-dominant and also drop K2 as it is a constant term.
3. Break the code into fragments.
       - Consider the code snippet: 
   
              // loop 1

              for (i=0; i<n; i++)
              {
                 k = k + i;
              }

              // loop 2 

              for(i=0; i<n; i++)
              {
                 k = k - i;
              }
           
      - Here the time complexity would be (n*k1) + (n*k2) => n * (k1 + k2) => time complexity is O(n), as we eliminated the constants k1 and k2.

4. For nested loops, consider the code: 
       ```
       for(i=0; i<n; i++)
       {      
              for(j=0; j<n; j++)
              {
                     k = k + 1; 
              }
        }
       ```
       - Here the time complexity would be O(n^2).
5. 

