# HW2 Questions
## UMBC CMSC 671 fall 2021

Please answer the following questions using the git [markdown syntax](https://guides.github.com/features/mastering-markdown/).  You should view this file on your repo on GitHub after pushing it to make sure it looks the way you want.  You can also use a browser extension (like [this one](https://chrome.google.com/webstore/detail/markdown-preview-plus/febilkbfcbhebfnokafefeacimjdckgl) for Chrome) to view your local file.

### (1) Describe in words the heuristic you used for the steps cost and explain why it is admissable

We used the A* algorithm. The goal state is achieved by replacing one word at a time closer to the goal node and the heuristic is the estimate of cost of shortest path from node to a goal.

### (2) Describe in words the heuristic you used for the scrabble cost and explain why it is admissable

For Scrabble cost, each letter that is replaced in the word (using A* Algorithm) contains a cost. Therefore, the cost is based on the sum of the total letter replacement cost to achieve the goal state. 

### (3) Describe in words the heuristic you used for the frequency cost and explain why it is admissable

For frequency, the cost is calculated on how frequently the word is used. If the replaced word is rare, then the cost is more. The measure of how rare the word is found in the dictionary.

### (4) Given an intiial word W1 and goal words W2, if there is a shortest path with N steps from W1 to W2, will there also be a shortest path of N steps from W2 to W1?  Explain why or why not.

 Yes. Because consider the initial words W1 - cat and W2 - dog. The shortest path for this is cat -> cot -> cog -> dog with cost 3. 
 Now again consider W1 - dog and W2 - cat (Interchanged). The shortest path computed is dog -> cog -> cot -> cat with cost 3.

### (5) Using the steps cost, what is the longest path for a pair of three- and four-letter words you can find?

The longest path using steps cost found for a pair of 3 letter word is - ('ask','why') because - The cost is 5.
DC(ask,why,steps) cost:5; time: 2.690; solution:ask ass ahs aha wha why

The longest path using steps cost found for a pair of 4 letter word is - ('icky','murk') because - The cost is 9.
DC(icky,murk,steps) cost:9; time: 31.860; solution:icky inky inks inns ions mons mans mars mark murk
