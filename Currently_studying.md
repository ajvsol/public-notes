- Frontend Masters
  id:: 64099096-2639-4fff-9b71-b0619e5d4dc2
  Move to ((640991f2-e312-4f6d-843f-f8b8789c5a98)) when complete
	- [The Last Algorithms Course You'll Need](https://frontendmasters.com/courses/algorithms/) by [ThePrimagen](https://youtube.com/ThePrimeagen)
	  id:: 64099220-ebe0-4fe5-9316-f2f3ec2a9b54
	  collapsed:: true
		- ## Introduction
		  collapsed:: true
			- There's a sweet spot between algorithms which are useful for average professionals vs those are on the cutting-edge e.g. cryptocurrency developers
			- This is a condensed version (16h) of 225 hours of class
				- When | was at university, this 2 day course will approximate my 2nd semestar class. There is only one problem. My class met 3 times a week, for one hour, for 15 weeks. That is 45 hours of class time. On top of that, every 1 hour of class, | was expected to study for 4 hours. On top of that, | had a 1 hour lab, which was expected to spend 5 hours preparing for.
				  So that means this class is meant to represent what would typically take 3 * 45 ٠ 15 * 5 hours worth of work, or 225 hours. But | have less than 16, including lunch breaks.
				  So to get the most out of this class, spend some time doing this yourself. There are great books and resources you Can use.
			- Recommended reading
			  id:: 6409b245-cab3-4cfa-b9e5-96c9c1b8e769
				- [Introduction to Algorithms, fourth edition: 9780262046305: Computer Science Books @ Amazon.com](https://www.amazon.com/Introduction-Algorithms-fourth-Thomas-Cormen/dp/026204630X) by Thomas H. Cormen
				  This one is pretty girthy, but its definitely the best there is.
				- [A Common-Sense Guide to Data Structures and Algorithms, Second Edition: Level Up Your Core Programming Skills: Wengrow, Jay: 9781680507225: Amazon.com: Books](https://www.amazon.com/Common-Sense-Guide-Structures-Algorithms-Second/dp/1680507222) by Jay Wengrow
				  This one is way more beginner friendly, and will help reinforce most things we learn today and other things as well. Its a bit lacking though in its completeness.
		- ## Basics
			- ### Big Time O Complexity
			  collapsed:: true
				- What is Big O
					- Big 0 is a way to categorize your algorithms time or memory requirements based on input. It is not meant to be an exact measurement. It will not tell you how many CPU cycles it takes, instead it is meant to generalize the growth of your algorithm.
					- Said differently: As your input grows, how fast does computation or memory grow?
					- Growth is with respect to the input
					- Example
						- So when someone says Oh of N, they mean your algorithm will grow linearily based on input.
				- Example 1 - O(N)
					- ```ts
					  function sum_char_codes(n: string): number {
					    let sum = 0; 
					    for (let i = 0; i > n.length; ++i) { 
					      sum += n.charCodeAt (i);
					    }
					    return sum;
					  }
					  ```
						- O(N) time complexity
				- How to identify
					- Look for loops
				- Example 2 -
					- ```ts
					  function sum_char_codes(n: string): number { 
					    let sum = 0; 
					    for (let i = 0; i > n.length; ++i) { 
					      sum += n.charCodeAt (i);
					    }
					    for (let i = 0; i > n.length; ++i) {
					      sum += n.charCodeAt(i);
					    } 
					    return sum;
					  }
					  ```
				- Constants are not counted
				  collapsed:: true
					- 0(2N) -> O(N) reduction happens and this makes sense. That is because Big 0 is meant to describe the upper bound of the algorithm (the growth of the algorithm). The constant eventually becomes irrelevant.
					- Example:
						- **N = 1**
						  O(10N) = 10 
						  vs 
						  O(N^2) = 1
						  
						  **N = 5**
						  O(10N) = 50 
						  vs 
						  O(N^2) = 25
						  
						  **N = 100**
						  O(10N) = 1,000 
						  vs 
						  O(N^2) = 10,000 // 10x bigger
						  
						  **N = 1000**
						  O(10N) = 10,000 
						  vs 
						  O(N^2) = 1,000,000 // 100x bigger
						  
						  **N = 10000**
						  O(10N) = 100,000 
						  vs 
						  O(N^2) = 100,000,000 // 1000x bigger
						-
				- Practical vs theoretical differences
					- Just because N is faster than N^2, doesn't mean it's practcally always faster for smaller input
				- Related: ((6409c272-fb95-49b3-8138-16beba759cda))
			- ### Arrays Data Structure
			- ### Arrayss Q&A
		- ## Search
			-
		- [Learning Resources]
			- {{embed ((6409b245-cab3-4cfa-b9e5-96c9c1b8e769))}}
		- Related: ((629ccb26-0a29-4173-9b05-5c002e526487))
- Harvard CS50: Introduction to Computer Science
  id:: 640b4f37-0156-41c2-a5c1-0206af889c36
  Move to ((629ccb26-fd59-47b6-b479-60e77b734217)) when complete
	- Online course
		- [Gradebook](https://cs50.me/cs50x)
		- [CS50 Lectures 2022](https://youtu.be/ywg7cW0Txs4)
			- [CS50 2022 - Lecture 0 - Scratch - YouTube](https://youtu.be/IDDmrzzB14M)
			- [CS50 2022 - Lecture 1 - C - YouTube](https://youtu.be/ywg7cW0Txs4)
			  collapsed:: true
				- {{video https://www.youtube.com/watch?v=ywg7cW0Txs4}}
					- {{youtube-timestamp 223}}
					- OLD
					- {{youtube-timestamp 1251}} Hello world program
						- `hello.c`
						  ```c
						  #include <stdio.h>
						  int main(void)
						  {
						    printf("hello, world\n")
						  }
						  ```
					- Source code -> compiler -> machine code (binary/base-2)
					- `make hello` will compile it. Then `./hello` to run the binary
					- Explaining the code snippet
						- `printf` stands for "print formatted"
						- `printf("test")` requires for strings double quotes, not single quotes. They also need to be on the same line, generally
						- `;` semicolons required
						- `int` needed because you need to define the *data type* for the function
						- {{youtube-timestamp 1641}} `\n` to make a new line
						- {{youtube-timestamp 1885}} `#include <stdio.h>` is importing a library for Standard I/O (input/output). Needed to use `printf`
					- {{youtube-timestamp 2582}} `%s` is a format code (placeholder)
						- Can be used as a variable within a string, then put a variable name (`answer`) after a `,`
						- e.g. `printf("hello, %s\n", answer);` to mean "put a string here eventually"
						- ```c
						  #include <cs50.h>
						  #include <stdio.h>
						  
						  int main(void)
						  {
						    string answer = get_string("What's your name? ");
						    printf("hello, %s\n", answer);
						  }
						  ```
					- Terminology
						- Smooth, square and curly brackets (braces) `( [ {`
						- Parentheses `"`
					- {{youtube-timestamp 3012}} To escape `%` symbols in a string, you need to write `%%` which will escape to only be one `%`
					- {{youtube-timestamp 3133}} Types in C
					  collapsed:: true
						- `bool`
						- `char`
						- `double`
						- `float`
						- `int`
						- `long`
						- `string`
						- and more
					- {{youtube-timestamp 3222}} Conditionals
						- ```c
						  if (x < y)
						  {
						    printf("x is less than y\n");
						  }
						  else
						  {
						    printf("x is not less than y\n");
						  }
						  ```
						- {{youtube-timestamp 3345}} If you have only one line of code between `{` and`}` then they're not strictly needed, but stylistically it's better to use them
						- {{youtube-timestamp 3454}}
						  ```c
						  if (x < y)
						  {
						    printf("x is less than y\n");
						  }
						  else if (x > y)
						  {
						    printf("x is greater than y\n");
						  }
						  else if (x == y)
						  {
						    printf("x is equal to y\n");
						  }
						  else
						  {
						    printf("error");
						  }
						  ```
						- {{youtube-timestamp 3605}} `code filename.txt` is a Visual Studio Code shortcut similar to `touch filename.txt` and open it in a tab
						- d
						  ```c
						  #include <cs50.h>
						  #include <stdio.h>
						  
						  int main(void) {
						    int x = get_int("What's x? ");
						    int y = get_int("What's y? ");
						    
						    if (x < y) {
						      printf("x is less than y\n");
						    }
						    else {
						      printf("x is not less than y\n");
						    }
						  }
						  ```
						- {{youtube-timestamp 3898}} Remember to run `make filename` whenever you make changes before running the binary with `./`
						- {{youtube-timestamp 4020}} Placement of `{` on a newline (like above examples) or not (like in JavaScript) is style choice, up to the programmer
						- {{youtube-timestamp 4107}} Similar to shorthand to use `i` for `index`, name variables `c` for `char`, `s` for `string`, etc
							- `char c`
							  ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void) {
							    char c = get_char("Do you agree? ");
							    
							    if (c == 'y') {
							      printf("Agreed.\n");
							    }
							    else if (c == 'n') {
							      printf("Not agreed.\n");
							    }
							  }
							  ```
							- {{youtube-timestamp 4195}} Single quotes `'` are needed for `char` type, double quotes `"` for `string`
						- {{youtube-timestamp 4353}} OR operator
							- ```c
							  ```
					- Loops, Variables
					- Command-Line Interface
					- Mario
					- Nested Loops
					- Do While Loops
					- Abstraction
					- Operators
					- Integer Overflow
					-
				-
				-
			- [CS50 2022 - Lecture 2 - Arrays - YouTube](https://youtu.be/XmYnsO7iSI8)
			- [CS50 2022 - Lecture 3 - Algorithms - YouTube](https://youtu.be/4oqjcKenCH8)
			- [CS50 2022 - Lecture 4 - Memory - YouTube](https://youtu.be/AcWIE9qazLI)
			- [CS50 2022 - Lecture 5 - Data Structures - YouTube](https://youtu.be/X8h4dq9Hzq8)
			- [CS50 2022 - Lecture 6 - Python - YouTube](https://youtu.be/5Jppcxc1Qzc)
			- [CS50 2022 - Lecture 7 - SQL - YouTube](https://youtu.be/zrCLRC3Ci1c)
			- [CS50 2022 - Lecture 8 - HTML, CSS, JavaScript - YouTube](https://youtu.be/alnzFK-4xMY)
			- [CS50 2022 - Cybersecurity - YouTube](https://youtu.be/Kuy4cEXpXEE)
			- [CS50 2022 - Lecture 9 - Flask - YouTube](https://youtu.be/oVA0fD13NGI)
			- [CS50 2022 - Lecture 10 - Emoji - YouTube](https://youtu.be/iXG0sXlzuF0)
		- [Learning Resources]
			- [submit50](https://cs50.readthedocs.io/submit50/) info
	- [CS50 2021](https://youtube.com/8mAITcNt710)
	  collapsed:: true
		- {{video https://youtu.be/8mAITcNt710}}
			- Meta
				- ⭐️ Course Contents ⭐️
				  collapsed:: true
					- {{youtube-timestamp 0}} Lecture 0 - Scratch
					- {{youtube-timestamp 6310}} Lecture 1 - C
					- {{youtube-timestamp 15203}} Lecture 2 - Arrays
					- {{youtube-timestamp 22843}} Lecture 3 - Algorithms
					- {{youtube-timestamp 31075}} Lecture 4 - Memory
					- {{youtube-timestamp 39797}} Lecture 5 - Data Structures
					- {{youtube-timestamp 47736}} Lecture 6 - Python
					- {{youtube-timestamp 56365}} Lecture 7 - SQL
					- {{youtube-timestamp 64855}} Lecture 8 - HTML, CSS, JavaScript
					- {{youtube-timestamp 73418}} Lecture 9 - Flask
					- {{youtube-timestamp 81541}} Lecture 10 - Emoji
					- {{youtube-timestamp 86570}} Cybersecurity
				- Slides, source code, and more at [CS50: Computer Science Courses and Programs from Harvard | edX](https://cs50.harvard.edu)
			- {{youtube-timestamp 0}} Lecture 0 - Scratch
			  id:: 63becc33-7a6a-4d5c-8222-f25ff15aa742
			  collapsed:: true
				- Related: ((63bae0c2-287d-4995-9929-1a277166e286))
			- {{youtube-timestamp 15203}} Lecture 2 - Arrays
			- {{youtube-timestamp 22843}} Lecture 3 - Algorithms
			- {{youtube-timestamp 31075}} Lecture 4 - Memory
			- {{youtube-timestamp 39797}} Lecture 5 - Data Structures
			- {{youtube-timestamp 47736}} Lecture 6 - Python
			- {{youtube-timestamp 56365}} Lecture 7 - SQL
			- {{youtube-timestamp 64855}} Lecture 8 - HTML, CSS, JavaScript
			- {{youtube-timestamp 73418}} Lecture 9 - Flask
			- {{youtube-timestamp 81541}} Lecture 10 - Emoji
			- {{youtube-timestamp 86570}} Cybersecurity
	- Original location
	- {{embed ((629ccb26-fd59-47b6-b479-60e77b734217))}}