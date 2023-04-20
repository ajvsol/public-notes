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
			- [Unit tests used by Check50](https://github.com/cs50/problems)
			- [submit50 — CS50 Docs](https://cs50.readthedocs.io/submit50/)
		- [CS50 Lectures 2022](https://youtu.be/ywg7cW0Txs4)
			- [CS50 2022 - Lecture 0 - Scratch - YouTube](https://youtu.be/IDDmrzzB14M)
			  Computer Science. Computational Thinking. Problem Solving: Inputs, Outputs. Representation: Unary, Binary, Decimal, ASCII, Unicode, RGB. Abstraction. Algorithms. Running Times. Pseudocode. Scratch: Functions, Arguments, Return Values; Variables; Boolean Expressions, Conditionals; Loops; Events; Threads.
			- [CS50 2022 - Lecture 1 - C - YouTube](https://youtu.be/ywg7cW0Txs4)
			  collapsed:: true
			  C. Source Code. Machine Code. Compiler. Correctness, Design, Style. Visual Studio Code. Syntax Highlighting. Escape Sequences. Header Files. Libraries. Manual Pages. Types. Conditionals. Variables. Loops. Linux. Graphical User Interface (GUI). Command-Line Interface (CLI). Constants. Comments. Pseudocode. Operators. Integer Overflow. Floating-Point Imprecision.
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
						- `bool`
						- `char`
						- `double`
						- `float`
						- `int`
						- `long`
						- `string`
						- and more
					- ### {{youtube-timestamp 3222}} Conditionals
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
						- Most important commands to learn
							- `cd` = Change Directory
							- `cp` = Copy
							- `ls` = List
							- `mkdir` = Make Directory
							- `mv` = Move (also renames)
							- `rm` = Remove
							- `rmdir` = Remove Directory
					- ### {{youtube-timestamp 6339}} Nested Loops and Mario
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
			  Preprocessing. Compiling. Assembling. Linking. Debugging. Arrays. Strings. Command-Line Arguments. Cryptography.
				- {{video https://youtu.be/XmYnsO7iSI8}}
					- ### {{youtube-timestamp 376}} Compiling in ((640c8362-cdc6-44a3-b991-a338f1d05b5a))
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
								- Changes everything to assembly code
								- Example assembly code for our C code
								  collapsed:: true
									- ![image.png](../assets/image_1678709069073_0.png)
							- {{youtube-timestamp 1689}} Assembling
								- Converts Assembly to binary (base-2/machine code)
							- {{youtube-timestamp 1724}} Linking
								- Combines the machine code for your code with the machine code for all your imports
						- {{youtube-timestamp 2240}} Decompiling is possible but you lose variable and function names, it becomes very hard to read. Probably better off just writing it from scratch
					- ### {{youtube-timestamp 2302}} Debugging
						- {{youtube-timestamp 2549}} `printf` is the simplest form of debugging (equivalent to `console.log`)
						- {{youtube-timestamp 2752}} Debugger
						  collapsed:: true
							- Breakpoints can be added in normal Visual Studio Code view by clicking in the gutter. Execute file as normal `./hello`
							- {{youtube-timestamp 2968}} Step-over - it'll step over functions like `printf`. Step-into would show each line of code beign executed in `printf`
							- The highlighted line hasn't yet been executed
							- {{youtube-timestamp 3434}} Step-into instead of step-over when you need to lock inside what a called function is doing
						- {{youtube-timestamp 3625}} Rubber duck debugging
						  collapsed:: true
							- Out loud talk through your issue
							-
					- ### {{youtube-timestamp 3904}} Arrays
						- {{youtube-timestamp 3904}} Each data structure takes up differing amounts of memory
							- `bool` = 1 byte (8 bits)
							- `int` = 4 bytes (32 bits)
							- `long` = 8 bytes (64 bits)
							- `float` = 4
							- `double` = 8
							- `char` = 1
							- `string` = ? bytes
						- {{youtube-timestamp 4176}} Arithmetic example
							- ```c
							  int main(void) {
							    int score1 = 72;
							    int score2 = 73;
							    int score3 = 33;
							    
							    printf("Average: %i\n", (score1 + score2 + score3) / 3)
							  }
							  ```
						- {{youtube-timestamp 4331}} Can't swap out `%i` for %f` unless you change another part of code
							- A) Make at least one of the existing numbers a `float` e.g. change `3` to `3.0`
							- B) Typecast instead e.g. `3` becomes `(float) 3`
						- {{youtube-timestamp 4530}} `int scores[3]` creates an array with space for `3` integers
						- `scores[0] = 72` inserts `72` as the first item of the array
						- {{youtube-timestamp 4633}} Replacing int variables with an integer array
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void) {
							    int scores[3]
							    scores[0] = get_int("Score: ");
							    scores[1] = get_int("Score: ");
							    scores[2] = get_int("Score: ");
							    
							    printf("Average: %i\n", (scores[0] + scores[1] + scores[2]) / 3)
							  }
							  ```
						- {{youtube-timestamp 4962}} How to write that a function takes an array of integers. `array` is just the var name, it's the `int ___[]` that defines it as an int array
						  ```c
						  float average(int array[]);
						  ```
						- {{youtube-timestamp 5127}} You want to set the array length and loop length to a var so you only have to change the number from one place (it's not a "magic number" you have to edit in multiple places)
							- ```c
							  const int N = 4; 
							  
							  float average(int array[]);
							  
							  int main(void) { 
							    int scores[N]; 
							    for (int i = 0; i<N; i++) { 
							      scores[i] = get_int("Score: "); 
							    }
							  }
							  ```
						- {{youtube-timestamp 5239}}
							- ```c
							  float average(int array[]) {
							    int sum = 0;
							    for (int i = 0; i < N; i++) {
							      sum += array[i];
							    }
							    return sum / (float) N;
							  }
							  ```
						- {{youtube-timestamp 5609}} You can't find out the length of an array after initialising it
					- ### {{youtube-timestamp 5704}} Strings
						- {{youtube-timestamp 5777}} A string is an array of characters, which is why you can access individual characters via bracket notation
						- {{youtube-timestamp 5866}} At the end of each string is a "sentinel value"/delimiter which is `0` char to separate the string from others. Similarly int arrays have a hidden `0` char at the end, which allows computers to know when the array ends. AKA `null`
						- {{youtube-timestamp 6058}} How to do multiple variables in a `printf`
						  ```c
						  int main(void) { 
						    char c1 = "H";
						    char c2 = "I"; 
						    char c3 = '!';
						    
						    printf ("%c %c %c\n", c1, c2, c3);
						  }
						  ```
						- {{youtube-timestamp 6231}} Similar example but for string
							- ```c
							  int main(void) {
							    string s = "HI!";
							    // or %c is valid. Strings are arrays of chars but also be expressed as int
							    printf("%i %i %i\n", s[0], s[1], s[2]);
							  }
							  ```
						- {{youtube-timestamp 6318}} Each string is just an array of chars
							- ```c
							  int main(void) {
							    string s = "HI!";
							    string t = "BYE!";
							  
							    printf("%s\n", s);
							    printf("%s\n", t);
							  }
							  ```
							- Each square being a byte:
							  ![image.png](../assets/image_1678795894869_0.png)
						- {{youtube-timestamp 6428}} How to initialise an array of strings in ((640c8362-cdc6-44a3-b991-a338f1d05b5a)) (`arrayType varName[arrayLength]`)
							- ```c
							  int main(void) {
							    // arrayType varName[arrayLength]
							    string words[2];
							    
							    words[0] = "HI!";
							    words[1] = "BYE!";
							  
							    printf("%s\n", words[0]);
							    printf("%s\n", words[1]);
							    // returns: HI!
							    // BYE!
							  }
							  ```
						- {{youtube-timestamp 6467}} You can access each character in an array of strings by using double bracket notation
							- ```c
							  int main(void) {
							    // Initalise with a length of 2
							    string words[2];
							    
							    words[0] = "HI!";
							    words[1] = "BYE!";
							  
							    printf("%c%c%c\n", words[0][0], words[0][1], words[0][2]);
							    printf("%c%c%c\n", words[1][0], words[1][1], words[1][2], words[1][3]);
							    // returns: HI!
							    // BYE!
							  }
							  ```
						- {{youtube-timestamp 6562}} There's no double `\0` to end an array of strings, it's just one `\0` for the last array item. This is why you can't figure out the length of an array once it's initialised, but you can for a `string`. Strings are special and end with `0`, whereas arrays don't have a special delimiter
							- ![image.png](../assets/image_1678795691630_0.png)
						- {{youtube-timestamp 6652}} How to get the length of a string using a while loop in ((640c8362-cdc6-44a3-b991-a338f1d05b5a))
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void) {
							    string name = get_string("What's your name? ");
							    
							    int n = 0;
							    while (name[n] != '\0') {
							      n++
							    }
							    printf("%i\n", n);
							  }
							  ```
						- {{youtube-timestamp 6788}} There's a library for `string` functions in ((640c8362-cdc6-44a3-b991-a338f1d05b5a)) called [`string.h`](https://manual.cs50.io/#string.h)
						- {{youtube-timestamp 6809}} `strlen` is the function in `string.h` to get string length
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  #include <string.h>
							  
							  int main(void) {
							    string name = get_string("What's your name? ");
							    int n = strlen(name);
							    printf("%i\n", n);
							  }
							  ```
						- {{youtube-timestamp 6878}} [`ctype.h`](https://manual.cs50.io/#ctype.h) library - for data types in C
							- The difference between a lowercase letter and it's uppercase version is always 32 in ASCII
							- ASCII chart
								- ![image.png](../assets/image_1678811769692_0.png)
							- Make uppercase.c
								- ```c
								  #include <cs50.h>
								  #include <stdio.h>
								  #include <ctype.h>
								  
								  int main(void) {
								    string s = get_string("Before: ");
								    printf("After: ");
								    for (int i = 0; i < strlen(s); i++) {
								      // Loop through each character, check if it's a letter
								      if (s[i] >= 'a' && s[i] <= 'z') {
								        // Convert it to uppercase by reducing it by 32 - see ASCII chart
								        printf("%c", s[i] - 32);
								      } else {
								        printf("%c", s[i]);
								      }
								    }
								    printf("\n");
								  }
								  ```
							- {{youtube-timestamp 7208}} Version using the library `ctype` - using the `strlen` function
								- ```c
								  #include <cs50.h>
								  #include <stdio.h>
								  #include <ctype.h>
								  
								  int main(void) {
								    string s = get_string("Before: ");
								    printf("After: ");
								    for (int i = 0; i < strlen(s); i++) {
								        printf("%c", toupper(s[i]));
								    }
								    printf("\n");
								  }
								  ```
							- {{youtube-timestamp 7379}} The loop checking for the length of `s` each time is inefficient, wastes CPU cycles **(important)**
								- ```c
								  // Before
								  for (int i = 0; i < strlen(s); i++)
								    
								  // After
								  for (int i = 0, n = strlen(s); i < n; i++)
								  ```
					- ### Command-Line Arguments
						- {{youtube-timestamp 7549}} `void` in `int main(void)` means it takes no CLI arguments
						- {{youtube-timestamp 7627}} `argc` = argument count, `argv` = argument value? the strings you enter as CL arguments
						  collapsed:: true
							- ```c
							  int main(int argc, string argv[]) { 
							    string name = get_string("What's your name? "); 
							    printf("hello, %s\n", name);
							  }
							  ```
						- {{youtube-timestamp 7704}} How to make a basic CL argument in your program
						  collapsed:: true
							- ```c
							  int main(int argc, string argv[]) { 
							    printf("hello, %s\n", argv[1]);
							  }
							  
							  // Running this via `./greet David`
							  // Returns: `hello, David`
							  ```
						- {{youtube-timestamp 7731}} `argv[0]` is always the name of the expression used to execute the program e.g. `./greet` here
						- {{youtube-timestamp 7786}} and `argc` = `2` (length), because you've entered 1 expression and 1 argument i.e. `./greet` and `name`
						- {{youtube-timestamp 7866}} Nowadays there's two official ways to define a main function:
						  collapsed:: true
							- ```c
							  // No CLI arguments
							  int main(void)
							    
							  // Yes CLI arguments
							  int main(int argc, string argv[])
							  ```
					- ### {{youtube-timestamp 8046}} Exit Status
					  collapsed:: true
						- 404 = not found
						- HTTP error code
						- {{youtube-timestamp 8141}} `int` means it'll return an integer, `0` by default (success)
						  collapsed:: true
							- ```c
							  int main(void)
							  ```
						- {{youtube-timestamp 8247}} `echo $?` can be run after executing a program (e.g. `./status` for `1` or `./status David` for `0`) to show the exit status of a program (showing what it returns)
						  id:: 642437fb-baa6-4c18-a3d1-596ecbccb6c4
						  collapsed:: true
							- ```c
							  int main(int argc, string argv[]) {
							    if (arge != 2) { 
							      printf("Missing command-line argument\n"); 
							      return 1;
							    }
							    else { 
							      printf("hello, %s\n", argv([1]);
							      return 0;
							    }
							  }
							  ```
					- ### {{youtube-timestamp 8379}} Cryptography
					  collapsed:: true
						- Transforming plaintext and key > via cipher (algorithm) > to ciphertext
						-
			- [CS50 2022 - Lecture 3 - Algorithms - YouTube](https://youtu.be/4oqjcKenCH8)
			  collapsed:: true
			  Searching: Linear Search, Binary Search. Sorting: Bubble Sort, Selection Sort, Merge Sort. Asymptotic Notation: *O* , Ω, Θ. Recursion.
				- {{video https://youtu.be/4oqjcKenCH8}}
					- ### {{youtube-timestamp 72}} Algorithms
					- ### {{youtube-timestamp 469}} Linear Search
						- Just starting at one end of the array and checking each sequentially
						- ```
						  For i from 0 to 26-1
						  	If 50 is behind doors[i]
						  		Return true
						  Return false
						  ```
					- ### {{youtube-timestamp 732}} Binary Search
						- Pre-requisite: the array has to be sorted
						- {{youtube-timestamp 856}} Keep looking in the middle of the selection of the array, then make a new subsection using the left or right half
						- ```
						  If no doors left
						  	Return false
						  If 50 is behind doors[middle]
						  	Return true
						  Else if 50 < doors[middle]
						  	Search left half
						  Else if 50 > doors[middle]
						  	Search right half
						  ```
						- {{youtube-timestamp 954}}
							- ```c
							  If no doors left
							  	Return false
							  If 50 is behind doors[middle]
							  	Return true
							  Else if 50 < doors[middle]
							  	Search doors[0] through doors[middle - 1]
							  Else if 50 > doors[middle]
							  	Search doors[middle + 1] through doors[length - 1]
							  ```
					- ### Running Time
						- {{youtube-timestamp 1286}} Big O notation
							- ![image.png](../assets/image_1680528039104_0.png)
						- {{youtube-timestamp 1308}} O(n/2) is irrelevant because it's the same shape
							- ![image.png](../assets/image_1680528122163_0.png)
						- {{youtube-timestamp 1351}} Upper-bound, how long an algorithm might take in worst case scenario (slowest at top):
						  id:: 643a7163-086b-4ebe-8f88-d1ed28f62336
							- O(*n*²)
							  id:: 642ad30b-9fff-4cba-ac25-bb3dd0262cee
							  Selection sort
							- O(*n* log *n*)
							- O(*n*)
							  id:: 642ad322-cf6c-4360-9e3e-a4e24f264d56
							  Linear search
							- O(log *n*)
							  id:: 642ad32c-4d27-468c-b0c5-d9f5e5eca51c
							  Binary search
							- O(1)
							  Finite number of steps, can even be say 999 steps
						- {{youtube-timestamp 1432}} Linear search is ((642ad322-cf6c-4360-9e3e-a4e24f264d56)) whereas binary search is ((642ad32c-4d27-468c-b0c5-d9f5e5eca51c))
						- {{youtube-timestamp 1521}} Ω (omega) describes lower-bound of an algorithm (how fast it might be if it gets lucky first time)
						  id:: 643a7163-c0d5-4f5f-a110-81ab4d4005b0
							- Ω(*n*²)
							  id:: 643a7163-5a80-4690-b11f-70282d809ee5
							  Selection sort
							- Ω(*n* log *n*)
							- Ω(*n*)
							  id:: 643a7163-9507-4130-9c35-0f5fd422c7b2
							  Bubble sort
							- Ω(log *n*)
							- Ω(1)
							  Linear search or binary search might get lucky and get it on first check
						- {{youtube-timestamp 1656}} Θ (theta) can be used if an algorithm has identical Big *O* and Ω values
							- Θ(*n*²)
							  id:: 643a7163-0b32-48c8-aca8-89f2a30c7ef9
							- Θ(*n* log *n*)
							- Θ(*n*)
								- e.g. counting all students in a room
							- Θ(log *n*)
							- Θ(1)
					- ### search.c
					  collapsed:: true
						- {{youtube-timestamp 1796}} Can use curley brackets when initialising an array to get the compiler to allocate you that much memory for the array
						  collapsed:: true
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void)
							  {
							    int numbers[] = {20, 500, 10, 5, 100, 1, 50};
							  }
							  ```
								- Alternatively:
								  ```c
								  int numbers[7];
								  numbers[0] = 20;
								  numbers[1] = 500; 
								  // etc
								  ```
						- {{youtube-timestamp 1891}} Example linear search
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void)
							  {
							    
							    int numbers[] = {20, 500, 10, 5, 100, 1, 50};
							    
							    int n = get_int("Number: ");
							    // Linear search
							    for (int i = 0; i < 7; i++)
							    {
							      if (numbers[i] == n)
							      {
							        printf("Found\n");
							        return 0;
							      }
							    }
							    printf("Not found\n");
							    return 1;
							  }
							  ```
						- {{youtube-timestamp 2049}} [`strcmp`](https://manual.cs50.io/3/strcmp) is needed to compare strings inside arrays
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  
							  int main(void)
							  {
							    string strings[] = {"battleship", "boot", "cannon", "iron", "thimble", "top hat"};
							    
							    string s = get_string("String: ");
							    // Linear search
							    for (int i = 0; i < 7; i++)
							    {
							      // The line `if (strings[i] == s)` wouldn't work because strings are arrays of chars?
							      // Instead use strcmp:
							      if (strcmp(strings[i], s) == 0)
							      {
							        printf("Found\n");
							        return 0;
							      }
							    }
							    printf("Not found\n");
							    return 1;
							  }
							  ```
						- {{youtube-timestamp 2261}} Segmentation fault error occurs when you touched memory you shouldn't have e.g. looped too many times
						- {{youtube-timestamp 2490}} related: ((642437fb-baa6-4c18-a3d1-596ecbccb6c4))
						- {{youtube-timestamp 2577}} Storing both names and numbers for a phonebook
							- `phonebook.c`
							  ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  #include <string.h>
							  
							  int main(void)
							  {
							    string names[] = {"Carter", "David"};
							    string numbers[] = {"+1-617-495-1000", "+1-949-468-2750"};
							    
							    string name = get_string("Name: ");
							    for (int i = 0; i < 2; i++)
							    {
							      if (strcmp(names[i], name) == 0)
							      {
							        printf("Found %s\n", numbers[i]);
							        return 0;
							      }
							    }
							    printf("Not found\n");
							    return 1;
							  }
							  ```
						- {{youtube-timestamp 2818}} Cons of the previous design:
							- Difficult to update the phonebook if it scales to much more users
							- Not built to ensure the order of arrays stays the same
					- ### structs
						- {{youtube-timestamp 2941}} Arrays are one type of data structure, but we can invent our own using primitives like string and int
						- {{youtube-timestamp 3023}} How to create a struct - example
							- ```c
							  typedef struct // Create own definition + the type of it is a 'structure'
							  {
							    string name;
							    string number;
							  }
							  person; // Name of type that you're creating
							  ```
						- {{youtube-timestamp 3090}} Integrating a struct by refactoring the previous example - uses dot notation
							- ```c
							  #include <cs50.h>
							  #include <stdio.h>
							  #include <string.h>
							  
							  typedef struct 
							  {
							    string name;
							    string number;
							  }
							  person;
							  
							  int main(void)
							  {
							    person people[2];
							    
							    people[0].name = "Carter";
							    people[0].number = "+1-617-495-1000";
							    
							    people[1].name = "David";
							    people[1].number = "+1-622-413-1001";
							   
							    string name = get_string("Name: ");
							    for (int i = 0; i < 2; i++)
							    {
							      if (strcmp(people[i].name, name) == 0)
							      {
							        printf("Found %s\n", people[i].number);
							        return 0;
							      }
							    }
							    printf("Not found\n");
							    return 1;
							  }
							  ```
					- ## {{youtube-timestamp 3532}} Sorting
						- e.g. sort the numbers into ascending order (initially `72541603`)
						- ### {{youtube-timestamp 3776}} Selection Sort
							- {{youtube-timestamp 3808}} Analyses the entire list to find the smallest number, then swaps that number with the number at position `0`
							- {{youtube-timestamp 3992}} Pseudocode version:
								- ```c
								  For i from 0 to n-1
								    Find smallest number between numbers[i] and numbers[n-1]
								    Swap smallest number with numbers[i]
								  ```
						- ### {{youtube-timestamp 4033}} Bubble Sort
							- {{youtube-timestamp 4076}} Just compares one number with the next number
							- {{youtube-timestamp 4160}} Largest numbers "bubble" their way to the top
							- {{youtube-timestamp 4218}} To confirm when to stop, do another full loop and when there's no swaps then stop
						- ### {{youtube-timestamp 4276}} Comparing Algorithms
							- {{youtube-timestamp 4356}} To calculate efficiency of algorithms vs each other, count how many comparisons took place
							- {{youtube-timestamp 4473}} Algorithm efficiency of selection sort = *n*(*n* - 1)/2 **->** (*n²* - 1)/2 **->** *n²*/2 - *n*/2
								- i.e. `(n - 1) + (n - 2) + (n - 3) + ... + 1`
								- Because to get the first smallest number is `(n - 1)`
								- To get the second smallest number is `(n - 2)`
								- etc
							- {{youtube-timestamp 4485}} It's basically ((642ad30b-9fff-4cba-ac25-bb3dd0262cee)) (you get to ignore that it gets divided by 2 and subtract a number, because when *n* is really large it doesn't really matter)
								- Related: ((643a7163-086b-4ebe-8f88-d1ed28f62336))
							- {{youtube-timestamp 4574}} Selection sort is ((643a7163-5a80-4690-b11f-70282d809ee5)), so because it's also ((642ad30b-9fff-4cba-ac25-bb3dd0262cee)) that makes it ((643a7163-0b32-48c8-aca8-89f2a30c7ef9))
								- Related: ((643a7163-c0d5-4f5f-a110-81ab4d4005b0))
							- {{youtube-timestamp 4709}} Bubble sort is ((642ad30b-9fff-4cba-ac25-bb3dd0262cee)) and ((643a7163-9507-4130-9c35-0f5fd422c7b2))
						- ((642437fb-c486-462e-9f9c-e508fcfda137))
					- ### {{youtube-timestamp 5246}} Recursion
						- Recursion is the ability of a function to call itself
						- {{youtube-timestamp 5555}} Pyramid example - print bricks in a pyramid shape
							- ```c#
							  #include <cs59.h>
							  #include <stdio.h>
							  
							  void draw(int n);
							  
							  int main(void) 
							  { 
							    int height = get_int("Height: "); 
							    draw(height); 
							  }
							  
							  void draw(int n)
							  {
							    for (int i = 0; i < n; i++)
							    {
							      for (int j = 0; j < i + 1; j++) 
							      {
							        printf("#");
							      }
							      printf("\n");
							    }
							  }
							  ```
						- {{youtube-timestamp 5715}} How to do the previous example recursively
							- ```c#
							  #include <cs59.h>
							  #include <stdio.h>
							  
							  void draw(int n);
							  
							  int main(void) 
							  { 
							    draw(1);
							  }
							  
							  void draw(int n)
							  {
							    // Base case
							    if (n <= 0) 
							    {
							      return;
							    }
							    
							    draw(n + 1);
							    
							    for (int i = 0; i < n; i++)
							    {
							      printf("#");
							    }
							    printf("\n");
							  }
							  ```
						- {{youtube-timestamp 6060}} Base classes can be used to exit a recursive program at the appropriate time
							- Example in previous example
								- ```c#
								  if (n <= 0) 
								  {
								    return;
								  }
								  ```
					- ### {{youtube-timestamp 6280}} Merge Sort
					  id:: 642437fb-c486-462e-9f9c-e508fcfda137
						- Depends on recursion
						- Pseudocode
							- ```
							  If only one number
							  	Quit
							  Else
							    Sort left half of numbers
							    Sort right half of numbers
							    Merge sorted halves
							  ```
						- {{youtube-timestamp 6544}} You keep looking at the left half, of the left half, of the left half until you end up with 2 numbers. Then compare and sort those.
						- {{youtube-timestamp 6662}} Then sort the next pair -> then the merge stage involves comparing the first numbers of each half, and each digit after that
						-
					- Asymptotic Notation: *O* , Ω, Θ.
			- [CS50 2022 - Lecture 4 - Memory - YouTube](https://youtu.be/AcWIE9qazLI)
			  Pointers. Segmentation Faults. Dynamic Memory Allocation. Stack. Heap. Buffer Overflow. File I/O. Images.
			- [CS50 2022 - Lecture 5 - Data Structures - YouTube](https://youtu.be/X8h4dq9Hzq8)
			  Abstract Data Types. Queues, Stacks. Linked Lists. Trees, Binary Search Trees. Hash Tables. Tries.
			- [CS50 2022 - Lecture 6 - Python - YouTube](https://youtu.be/5Jppcxc1Qzc)
			  Python: Functions, Arguments, Return Values; Variables; Boolean Expressions, Conditionals; Loops. Modules, Packages.
			- [CS50 2022 - Lecture 7 - SQL - YouTube](https://youtu.be/zrCLRC3Ci1c)
			  SQL: Tables; Types; Statements; Constraints; Indexes; Keywords, Functions; Transactions. Race Conditionals. SQL Injection Attacks
			- [CS50 2022 - Lecture 8 - HTML, CSS, JavaScript - YouTube](https://youtu.be/alnzFK-4xMY)
			  Internet: Routers; TCP/IP; DNS. HTTP: URLs, GET, POST. HTML: Tags; Attributes. Servers. CSS: Properties; Selectors. Frameworks. JavaScript: Variables; Conditionals; Loops. Events.
			- [CS50 2022 - Cybersecurity - YouTube](https://youtu.be/Kuy4cEXpXEE)
			- [CS50 2022 - Lecture 9 - Flask - YouTube](https://youtu.be/oVA0fD13NGI)
			  Flask. Route. Decorators. Requests, Responses. Sessions. Cookies.
			- [CS50 2022 - Lecture 10 - Emoji - YouTube](https://youtu.be/iXG0sXlzuF0)
			  Precision. Unicode: Emoji, Code Points, ZWJ.
		- [Learning Resources]
			- Recommended books
				- Hacker’s Delight, Second Edition
				  Henry S. Warren Jr.
				  Pearson Education, 2013
				  ISBN 0-321-84268-5
				- How Computers Work, Tenth Edition
				  Ron White
				  Que Publishing, 2014
				  ISBN 0-7897-4984-X
				- Programming in C, Fourth Edition
				  Stephen G. Kochan
				  Pearson Education, 2015
				  ISBN 0-321-77641-0
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