## How many ways are there to permute the letters in the word MISSISSIPPI?

### Initial Reasoning

- There are 11 letters in the word MISSISSIPPI
- We treat each letter as distinct because of its position
- There are 11 positions to place the letters
- There are 11 ways to place any letter to the first position
- Once the first letter is placed in the first position, there are only 10 ways to place the second letter
- Applying the same logic, there are a total of 11! = 11 * 10 * ... \* 1 ways to permute the letters in the word MISSISSIPPI
- The result is equal to nearly 4 million ways!

### Correction

- **The mismatch**: I overcounted the result by over two orders of magnitude! I found out thanks to the fact the result for this problem is available online. I think the key issue here is the line of reasoning where I said: "We treat each letter as distinct". But actually on second thought, I don't think that's the issue if I treat every single letter as distinct, then there are indeed 11! ways to rearrange them. In other words, the first letter S is different from the second, the third and the last. However, if I reframe the question as: "How many ways are there to distinguishably permute the letters in the word MISSISSIPPI?", then the results derived earlier is an overcount.
- **How to fix**: So, if we want to find the number of distinguishable permutations, then we need to adjust our lines of reasoning:
  - First, the distinct letters in the word are: M, S, I, P
  - If we choose to place M first, then there are 11 spaces available to put M: 11!/10! = 11 ways to place M
  - Now, we have 10 spaces left
  - If we choose to place the 4 Ss in the remaining 10 spaces: 10!/6! (indistinguishable)

### References

1. https://www.youtube.com/watch?v=1CxB3OykYag
