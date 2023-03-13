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
		- Meta
			- [Gradebook](https://cs50.me/cs50x)
			- [Visual Studio Code for CS50 — CS50 Docs](https://cs50.readthedocs.io/code/) Docs on their web editor
			- [Sign in to GitHub · GitHub](https://submit.cs50.io/users/ajvsol) submission site
		- [CS50 Lectures 2022](https://youtu.be/ywg7cW0Txs4)
			- [CS50 2022 - Lecture 0 - Scratch - YouTube](https://youtu.be/IDDmrzzB14M)
			- [CS50 2022 - Lecture 1 - C - YouTube](https://youtu.be/ywg7cW0Txs4)
			  collapsed:: true
				- {{video https://www.youtube.com/watch?v=ywg7cW0Txs4}}
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
					- ### {{youtube-timestamp 2582}} Format Codes
						- `%s` is a format code (placeholder)
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
					- {{youtube-timestamp 3133}} Types in ((640c8362-cdc6-44a3-b991-a338f1d05b5a))
					  collapsed:: true
						- `bool`
						- `char`
						- `double`
						- `float`
						- `int`
						- `long`
						- `string`
						- and more
					- ### {{youtube-timestamp 3222}} Conditionals
					  collapsed:: true
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
						- {{youtube-timestamp 4353}} OR operator `||`
						  collapsed:: true
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void) {
							    char c = get_char("Do you agree? ");
							    
							    if (c == 'y' || c == 'Y') {
							      printf("Agreed.\n");
							    }
							    else if (c == 'n' || c == 'N') {
							      printf("Not agreed.\n");
							    }
							  }
							  ```
					- ### {{youtube-timestamp 4552}} Loops, Variables
					  collapsed:: true
						- {{youtube-timestamp 4608}} ((640c8362-cdc6-44a3-b991-a338f1d05b5a)) convention is 4 spaces for indentation
						- {{youtube-timestamp 4781}} Syntactic sugar when shorter ways of writing common expressions
						- {{youtube-timestamp 4820}} `counter = counter + 1` == `counter += 1` == `counter++`
						- {{youtube-timestamp 4901}} While loop
						  collapsed:: true
							- ```c
							  int i = 0;
							  while (i < 3) {
							    printf("meow\n");
							    i--
							  }
							  ```
							- {{youtube-timestamp 5207}} Canonical way is starting `i = 0`
							- ```c
							  #include <stdio.h>
							  
							  int main(void) {
							    int i = 0;
							    while (i < 30) {
							      printf("meow\n");
							      i++
							    }
							  }
							  ```
						- {{youtube-timestamp 5326}} For loop
							- ```c
							  for (int i = 0; i < 3; i++) {
							    printf("meow\n");
							  }
							  ```
						- {{youtube-timestamp 5630}} Forever while loop
							- `while (true)` or `while (1)`
							- Need to also `#include <stdloop.h>`
					- ### {{youtube-timestamp 5808}} Command-Line Interface
					  collapsed:: true
						- Most important commands to learn
							- `cd` = Change Directory
							- `cp` = Copy
							- `ls` = List
							- `mkdir` = Make Directory
							- `mv` = Move (also renames)
							- `rm` = Remove
							- `rmdir` = Remove Directory
					- ### {{youtube-timestamp 6339}} Nested Loops and Mario
					  collapsed:: true
						- Making a 3x3 grid
						  ```c
						  #include <stdio.h>
						  
						  int main(void) {
						    for (int i = 0; i < 4; i++) {
						      for (int j = 0; j < 3; j++) {
						        printf("#");
						      }
						      printf("\n");
						    }
						  }
						  ```
						- {{youtube-timestamp 6907}} `const` e.g. `const int n = 5`
					- ### {{youtube-timestamp 7249}} Do While Loops
					  collapsed:: true
						- ```c
						  #include <stdio.h>
						  
						  int main(void) {
						    int n;
						    do {
						      n = get_int("Size: ");
						    } while (n < 1);
						    
						    for (int i = 0; i < 4; i++) {
						      for (int j = 0; j < 3; j++) {
						        printf("#");
						      }
						      printf("\n");
						    }
						  }
						  ```
					- {{youtube-timestamp 7452}} `//` for comments
					- ### {{youtube-timestamp 7579}} Abstraction
					  collapsed:: true
						- ```c
						  #include <stdio.h>
						  
						  int main(void) {
						    // Get size of grid
						    int n = get_size();
						    
						    // Print grid of tickets
						    print_grid(n)
						  }
						  
						  int get_size(void) {
						    int n;
						    do {
						      n = get_int("Size: ");
						    } while (n < 1);
						    return n;
						  }
						  
						  void print_grid(int size) {
						    for (int i = @; i < size; i++) {
						      for (int j = 0; j < size; j++) {
						      	printf ("#");
						      }
						      print("\n");
						    }
						  }
						  ```
							- ```c
							  void print_grid(int size)
							  ```
								- `int size` because similar to TypeScript, parameters need a type annotation
								- `void` because the function returns no type (`void`)
						- {{youtube-timestamp 7837}} Teasing (related to hoisting?)
							- Cleaner solution rather than having to move functions to the top of the file
							- Copy the first line of code from the function and end it with a semi-colon
							  ```c
							  #include <stdio.h>
							  
							  // Teasing
							  int get_size(void);
							  void print_grid(int size);
							  
							  int main(void) {
							    // Get size of grid
							    int n = get_size();
							    
							    // Print grid of tickets
							    print_grid(n)
							  }
							  
							  int get_size(void) {
							    int n;
							    do {
							      n = get_int("Size: ");
							    } while (n < 1);
							    return n;
							  }
							  
							  void print_grid(int size) {
							    for (int i = @; i < size; i++) {
							      for (int j = 0; j < size; j++) {
							      	printf ("#");
							      }
							      print("\n");
							    }
							  }
							  ```
					- ### {{youtube-timestamp 8175}} Integer Overflow
						- In 32-bit you can only go ~2 billion positive or negative. Integer overflow is when you try to represent an integer outside this range
						- Instead of `int` you can use `long` which allows for bigger numbers
					- Truncation
						- {{youtube-timestamp 8288}} Other format codes
							- `%c` = char
							- `%f` == `float` == floating point values (has decimals)
							- `%li` = long integer (64-bit)
							- `%s` = string
							- `%i` = integer (32-bit)
						- {{youtube-timestamp 8453}} `int` and `long` don't have support for decimals
						- {{youtube-timestamp 8525}} Type casting
							- `(float)` has to be added infront of the variables
							  ```c
							  int main(void) {
							    long x = get_long("x: ");
							    long y = get_long("y: ");
							    
							    float z = (float) x / (float) y; 
							    printf("%f\n", z);
							  }
							  ```
					- {{youtube-timestamp 8604}} Floating-point imprecision
						- `printf("%.20f\n", z);` = added `.20`to show 20 decimal places for the `%f`
						- {{youtube-timestamp 8726}} How to prevent
							- `double` = 2x as many bits as `float` (32 -> 64)
					- [Learning Resources]
						- ((64024e3f-a15d-4a78-a629-6d530a318a64))
				-
				-
			- [CS50 2022 - Lecture 2 - Arrays - YouTube](https://youtu.be/XmYnsO7iSI8)
			  collapsed:: true
				- {{video https://youtu.be/XmYnsO7iSI8}}
					- ### {{youtube-timestamp 376}} Compiling
						- {{youtube-timestamp 442}} `make` isn't a compiler, it automates one. It utilises `clang` as the compiler
						- {{youtube-timestamp 501}} `clang hello` instead of `make hello` produces an `a.out` file (assembler output). To make it use the same filename, instead do `clang -o hello hello.c`
							- `-o hello` = name the output file as `hello`
						- {{youtube-timestamp 930}} Our file from last week won't compile as-is using `clang`
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void) { 
							    string name = get_string("What's your name? "); 
							    printf("hello, %s\n", name);
							  }
							  ```
						- {{youtube-timestamp 950}} Need to run with `clang -o hello hello.c -lcs50` so that `clang` knows where the third-party imported library is located. `stdio` on the other hand is first-party, built-into C
						- {{youtube-timestamp 1181}} There's really 4 steps in compiling:
							- {{youtube-timestamp 1216}} Preprocessing
							  collapsed:: true
								- Converts everything to proper C code by adding in the imports
								- The libraries we included before are actually stored in `/usr/include`
								- The `include`s get transformed
								  ```c
								  // #include <cs50.h>
								  string get_string(string prompt);
								  // #include <stdio.h>
								  int printf(string format, ...);
								  ```
									- `...` = any number of variables
									-
							- {{youtube-timestamp 1534}} Compiling
							  collapsed:: true
								- Changes everything to assembly code
								- Example assembly code for our C code
								  collapsed:: true
									- ![image.png](../assets/image_1678709069073_0.png)
							- {{youtube-timestamp 1689}} Assembling
							  collapsed:: true
								- Converts Assembly to binary (base-2/machine code)
							- {{youtube-timestamp 1724}} Linking
							  collapsed:: true
								- Combines the machine code for your code with the machine code for all your imports
						- {{youtube-timestamp 2240}} Decompiling is possible but you lose variable and function names, it becomes very hard to read. Probably better off just writing it from scratch
					- ### {{youtube-timestamp 2302}} Debugging
						- {{youtube-timestamp 2549}} `printf` is the simplest form of debugging (equivalent to `console.log`)
						- {{youtube-timestamp 2752}} Debugger
							- Breakpoints can be added in normal Visual Studio Code view by clicking in the gutter. Execute file as normal `./hello`
							- {{youtube-timestamp 2968}} Step-over - it'll step over functions like `printf`. Step-into would show each line of code beign executed in `printf`
							- The highlighted line hasn't yet been executed
							- {{youtube-timestamp 3434}} Step-into instead of step-over when you need to lock inside what a called function is doing
						- {{youtube-timestamp 3625}} Rubber duck debugging
							- Out loud talk through your issue
							-
					- ### Arrays
					- ### Strings
					- ### Command-Line Arguments
					- ### Exit Status
					- ### Cryptography
					-
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