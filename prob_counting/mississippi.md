## How many ways are there to permute the letters in the word MISSISSIPPI?

### Initial Reasoning

- There are 11 letters in the word MISSISSIPPI
- We treat each letter as distinct because of its position
- There are 11 positions to place the letters
- There are 11 ways to place any letter to the first position
- Once the first letter is placed in the first position, there are only 10 ways to place the second letter
- Applying the same logic, there are a total of 11! = 11 _ 10 _ ... \* 1 ways to permute the letters in the word MISSISSIPPI
- The result is equal to nearly 4 million ways!

### Correction

- **The mismatch**: I overcounted the result by over two orders of magnitude! I found out thanks to the fact the result for this problem is available online. I think the key issue here is the line of reasoning where I said: "We treat each letter as distinct". But actually on second thought, I don't think that's the issue if I treat every single letter as distinct, then there are indeed 11! ways to rearrange them. In other words, the first letter S is different from the second, the third and the last. However, if I reframe the question as: "How many ways are there to distinguishably permute the letters in the word MISSISSIPPI?", then the results derived earlier is an overcount.
- **How to fix**: So, if we want to find the number of distinguishable permutations, then we need to adjust our lines of reasoning:
  - First, the distinct letters in the word are: M, S, I, P
  - If we choose to place M first, then there are 11 spaces available to put M: 11!/10! = 11 ways to place M
  - Now, we have 10 spaces left
  - If we choose to place the 4 Ss in the remaining 10 spaces: 10!/6! (indistinguishable). However, this total count consists of duplicates. As a result, we need to divide the total by 4! to get the distinguishable count. Why? Because given any 4 spaces, there are 4 (place the first S) _ 3 (place the second S) _ 2 (place the third S) \* 1 (place the last S) = 4! which means the counts to place 4 Ss are duplicated 4! times.
  - Therefore, there are 10!/6!4! ways to place the 4 Ss distinguishably
  - Now we have 6 spaces left
  - If we choose to place the 4 Is in the reamining 6 spaces, we have: 6!/2!4! (ways)
  - Now we have 2 spaces left, which means there is only 1 way to place the 2 Ps
  - **Final Result: 11 * (10!/6!4!) * (6!/2!4!) \* 1 = 34650**

### References

1. https://www.youtube.com/watch?v=1CxB3OykYag
