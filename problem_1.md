
     
## The Library with less wait 
In the lecture about searching, we talked about how different data structure such as array, linked list, and tree can be used to different searching algorithm. There are two categories, random-search vs popularity search. These refer to the different pattern of search activities. In this task, we'll be implementing a popularity-based search data structure called "LRU" cache, or "Least Recently Used" cache. 

### Task 1.1 

Watch [this Google Talk video](https://youtu.be/OwKj-wgXteo?si=vVIJV50gW75pBUYo&t=2528). It has a great explanation about the concept and real-life examples of "Least Recently Used" scenarios. For this task, write in a block of comment in [this file](https://github.com/a-teaching-goose/2024-summer-342-hw-3/blob/main/src/problem_1/LRU.hpp) listing at least 3 but no more than 7 things you learnt from the video.

### Task 1.2

Implement the LRU data structure [here](https://github.com/a-teaching-goose/2024-summer-342-hw-3/blob/main/src/problem_1/LRU.hpp) following the TODOs.

Here's a diagram of what this LRU looks like:

<img width="50%" alt="image" src="https://github.com/user-attachments/assets/1a7e35f5-2798-4145-a8ed-52faa90d5222">

### Task 1.3 

After the homework is assigned, a bug was found. It starts with a logic error in this [unit test for library](https://github.com/a-teaching-goose/2024-summer-342-hw-3/blob/main/test/problem_1/unit_test_library.cpp#L12). A line is missing, and it will cause the test to fail even if the code is correct. Fix this by adding the missing line with a comment explaining what's the issue and why the fix.

In addition, [this function](https://github.com/a-teaching-goose/2024-summer-342-hw-3/blob/main/src/problem_1/library.cpp#L7) in library class also has logic error. It can be fixed by adding one line of code. Please make the fix and add a comment explaining it.

### LRU Library

Once the LRU code is finished, read [this](https://github.com/a-teaching-goose/2024-summer-342-hw-3/blob/main/test/problem_1/unit_test_library.cpp) test where your LRU is used in an real-life example of a library. In this library, there's multiple floors to store books, and the higher the floor, the longer it takes to retrieve the book. To help speed up the retrieve time by observing the fact that popular books are usually borrowed closely in time, there's a book shelf at the front desk to keep those recently returned book. This book shelf has limited capacity, so if it's full, the least recently used book will be put back to a shelf in its floor based on the book name. Here's a diagram:

Once your LRU code is done, the library test will pass too. All your work is in the LRU file. Nothing to write in the library file but it'd be full to read and see how it works.
