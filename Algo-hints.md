# Leetcode/Algo Questions

### XOR property:
* 0 ^ 5 = 5
* Only works during continued operation
* 5 ^ 5 = 0
* Helps in finding duplicates
* int carry1 = a&b; carry1 << 1 to add to the sum1
* int sum1 = a^b;
* 
* a ^ b gives plain sum (without carry)
* a & b gives set bits (or pseudo carry)
    * Shift bits by << 1 
    * Use the shifted carry to add to plain sum
    * Continue until the carry becomes zero
https://www.geeksforgeeks.org/top-algorithms-and-data-structures-for-competitive-programming/#algo1
Valid BST 
use MIN, MAX at every recursion. min, max changes based on whether traversing left or right. LeetCode failed for some dumb test cases.
#### LRU Cache
Doubly Linked List + HashMap —> O(1) get&put
#### Merge k sorted Lists
* Heaps
* Merge 2 lists —> Merge 2 Merge 2 —> Merge 4 Merge 4 —> … reverse binary division approach
* Merge Sort 2 lists
    * Keep two ptrs. Move each of them based on comparison
Max Path Sum Binary Tree
* Consider max of left/right sum
* Consider sum of existing subtree
* Store Max in a separate class to retain pointer
Edit Distance
* Dynamic Programming. 
Longest Consecutive Sequence
* Store initial array in map
* return f(n) + f(n-1)
* No memoization reqd
Longest Parentheses
* Use stack, Pop if you see ‘)’. 
RegExMatching . & *
* Recursion
BurstBalloons
 k is the last balloon to be burst in the range i,j
Try all possible k's in the range i,j
 len can vary from 1 --> N. Traverse every i,j in all the length
 i,j can range from 0,1 0,2 1,2 3,4 ... 0,n
O(N^3) time O(N^2) space
Longest Palindrome
- O(N^2) Dynamic Programming. p[i][i] = true or false. loop over for all lengths
- Manachers’ Problem is O(N). https://articles.leetcode.com/longest-palindromic-substring-part-ii/ Involves padding & stuff
Delete middle of linked list with access to only to that node
- Copy paste values from the next node
Head of Loop in a Linked List
- Run two pointers 1x & 2x. Once they meet. Run one ptr from head. One from the meting pt both at 1x. Meeting point is the head of the loop
Towers of Hanoi
- Recursion. Move top 3 —> Buffer, Move left over to destination. Swap Buffer & destination in the next loop
Knight Movement
- Store all possible moves in delta +2,+1 -2,+1
Exam Room
- Store the occupied indices in a TreeSet
Three Sum == 0
- Sort the input arr
- For every element find the matching elements whose sum = -curr . Ignore duplicates
## Two Pointer Problems
### MinWindowSubstring
- Keep a count of matches 
- Begin End Ptr
- Create a map of T. counter = T.size
- For every end char. Decrease map(char)
- Increase the counter if map(char)>=0
- When counter == 0 check minLen
  - Once minLen updated, move Begin ptr
  - Begin Ptr movement needs to be adjusted
  - Increase Map(begin) 
  - If >0 then Decrease counter
## Graph
