# Guard-The-Wall

There're n sections in a line numbered from 1 to n.

There're q soliders, for i_th solider, he can guard from section L_i to R_i (1<=i<=q)

A section is guarded if at least one solider guard the section.

You can only hire q-2 soliders. 

You need to find the maximum number of sections that can be quarded by hiring q-2 soliders from q soliders.

# input

  First number t = number of testcase
  
  Each testcase contains two numbers n and q (3<=n,q<=5000).
  
  Following q lines, each line contains two integer L_i, R_i (1 <= L_i <= R_i <= n)
  
# output
  the maximum number of sections that can be guarded by hiring q-2 soliders.

# solution 
  1. calculate each section has how many guard
  2. enumerate if we take off one guard:
    a. -1 on the section that the gurad have
    b. for the section which only 1 guard do prefix fum
    c. enumerate the array to find the next guard we choose the remove will decrease the minimum section (checking on prefix sum can get O(1))
