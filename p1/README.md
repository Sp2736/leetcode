# Two Sum Problem – Learning Through Optimization

This problem is about returning the indices of the pairs of numbers from a vector, which when added, should give the desired sum which is there as input. There can be various ways of solving this problem, varying from the most beginner ones to the most expert ones.

I tried to solve this problem initially using the basic logic development as learned from C language, i.e. using nested loops and comparing each and every pair in the vector (or array).

Once the code was done, which would take no longer than 10 or 15 minutes if one is thorough with C language and logic, I shifted towards optimising my code. In order to learn new ways of looking at the problem, I started to explore the various approaches that could be made.

To be honest, I understood only 2 ways out of a list of various procedures, and one of them is present in the optimised code here.

It is not about directly searching and fetching the answers using the LLMs, but it is about using those powerful resources to learn and grasp newer approaches to the existing problems, which would help save time (in software). In order to start my LeetCode journey, I did the same. Must there come a time, when this shall not be required anymore!

---

## EXPLAINATION OF THE CODE

In the normal procedure, I simply used a nested for loop to check every umber with every other number in the vector (since same number was not to be considered, and there existed only a unique solution).

Even more so, once a particular index was considered for checking with other values, the next considered index was not to be compared with the previous index anymore, since [0,1] and [1,0] would both mean the same pair, and is logically 'trash' to do so.

Hence, the time complexity of the solution proposed was O(n^2), and the space complexity was O(1).

---

## OPTIMISED APPROACH

In the optimised version, the concept of Unordered HashMap STL of C++ was utilised, wherein the concept to be implemented was somehow similar to tail recursion: remembering the previous task.

The idea was to push every unique comparison as key (the number considered) and value (its index in vector) pairs into the unordered_map template.

One shall then look for that pair in the map, with every iteration in the vector, meaning that the entire vector would be iterated only once!

Hence the new time complexity of the problem got narrowed down to O(n). However, the space complexity was levelled up to O(n).

This one logical optimisation changed the way I view different problems (such as arrays, strings, etc. other stuff) completely, and probably much more to come.
