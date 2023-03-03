- Related: [[JavaScript]] : ((6341c12f-21ed-489f-bb16-1734abd32b1f))
- Meta
- Takeaways
- TEMPLATE
  collapsed:: true
	- My solution
		- ```javascript
		  ```
	- Best practice
		- ```javascript
		  ```
- Completed solutions
- [Learning Resources]
	- [Grind 75](https://www.techinterviewhandbook.org/grind75) (v2 of ((64bcadf7-2fb0-4d59-89a7-7b565d18560b)) )
	  collapsed:: true
		- *Array*
			- *Easy*
				- [Two Sum](https://leetcode.com/problems/two-sum/description)
				  id:: 0e542595-2f6d-4864-9ff5-9f953ccd7a29
				  collapsed:: true
					- My solution
						- ```javascript
						  /**
						   * @param {number[]} nums
						   * @param {number} target
						   * @return {number[]}
						   */
						  var twoSum = function(nums, target) {
						      for (let i = 0; i < nums.length; i++) {
						          for (let j = i + 1; j < nums.length; j++) {
						              if (nums[i] + nums[j] === target) {
						                  return [i, j]
						              }
						          }
						      }
						  };
						  ```
					- Best practice - [Solutions](https://leetcode.com/problems/two-sum/solutions/127810/two-sum/)
						- Approach 1: Brute Force
						  collapsed:: true
							- Cons
								- Succeeds the first test cases, but fails the ones where they use huge integers
							- ```javascript
							  var twoSum = function(nums, target) {
							      for (let j = 0; j < nums.length; j++) {
							          for (let i = j + 1; i < nums.length; i++) {
							              console.log(`j: ${j} and i: ${i} and target: ${target}`)
							              if (nums[j] === target - nums[i]) {
							                  return [j, i]
							              }
							          }
							      }
							      return null
							  };
							  ```
						- Approach 2: Two-pass Hash Table
							- ```javascript
							  var twoSum = function(nums, target) {
							      // create a new Map
							      let map = new Map();
							      // loop over the nums
							      for (let i = 0; i < nums.length; i++) {
							        // store the complement between current num and the target
							  	  // if target 10, and num[i] = 6 there is only ONE number that we can add to 6 to make it 10. 
							          // That is the number 4. We call it the complement because it complements 6 to hit the target 10.
							          // EG if target = 10 and nums[i] = 6....  10 - 6 = complement = 4
							          let complement = target - nums[i];
							          // What we are going to do is check if the complement exists in the hashmap.
							          // If the map already contains the complement we will return an array with the index of the complieent. And current index.
							          // When calling map.get(complement) in the return, this will return the VALUE at that key 
							          if (map.has(complement)) {
							             return [map.get(complement), i];
							          } else {
							            // Since the complement does not exist as a key in the map.
							            // We store the key num[i], and index as the value for that key.
							            map.set(nums[i] , i)
							          }
							      }
							      // If there is no complement we will return an empty array. 
							  return [];
							  };
							  ```
								- ((63904f3d-96c1-429e-af8b-4a46b1bf89c5))
								- ((63904f3d-6b67-461e-bf92-5f55bc24fa36))
							- ```javascript
							  var twoSum = function(nums, target) {
							      let map = new Map();
							      for(let i = 0; i < nums.length; i ++) {
							          if(map.has(target - nums[i])) {
							              return [map.get(target - nums[i]), i];
							          } else {
							              map.set(nums[i], i);
							          }
							      }
							  	return [];
							  };
							  ```
							- One-pass Hash Table
							  ```javascript
							  var twoSum = function(nums, target) {
							      const indices = new Map();
							      for (let index = 0; index < nums.length; index++) {
							          const complement = target - nums[index];
							          if (indices.has(complement)) {
							              return [indices.get(complement), index]
							          }
							          indices.set(nums[index], index)
							      }
							  };
							  ```
				- [Best Time to Buy and Sell Stock ](https://leetcode.com/problems/best-time-to-buy-and-sell-stock)
				  collapsed:: true
					- My solution
						- ```javascript
						  ```
					- Best practice
						- ```javascript
						  ```
				- [Contains Duplicate](https://leetcode.com/problems/contains-duplicate)
				  id:: 63f3d7d0-a1ab-4f21-8ce8-fa4ae7aed53d
				- [Majority Element](https://leetcode.com/problems/majority-element)
			- *Medium*
				- [Insert Interval](https://leetcode.com/problems/insert-interval)
				- [3Sum](https://leetcode.com/problems/3sum)
				- [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self)
				- [Combination Sum](https://leetcode.com/problems/combination-sum)
				- [Merge Intervals](https://leetcode.com/problems/merge-intervals)
				- [Sort Colors](https://leetcode.com/problems/sort-colors)
				- [Container With Most Water](https://leetcode.com/problems/container-with-most-water)
		- *String*
		  collapsed:: true
			- *Easy*
				- [Valid Palindrome](https://leetcode.com/problems/valid-palindrome)
				- [Valid Anagram](https://leetcode.com/problems/valid-anagram)
				- [Longest Palindrome](https://leetcode.com/problems/longest-palindrome)
			- *Medium*
				- [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters)
				- [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring)
				- [String to Integer (atoi)](https://leetcode.com/problems/string-to-integer-atoi)
				- [Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string)
			- *Hard*
				- [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring)
		- *Matrix - Medium*
		  collapsed:: true
			- [Spiral Matrix](https://leetcode.com/problems/spiral-matrix)
		- *Graph*
		  collapsed:: true
			- *Easy*
				- [Flood Fill](https://leetcode.com/problems/flood-fill)
			- *Medium*
				- [01 Matrix](https://leetcode.com/problems/01-matrix)
				- [Clone Graph](https://leetcode.com/problems/clone-graph)
				- [Course Schedule](https://leetcode.com/problems/course-schedule)
				- [Number of Islands](https://leetcode.com/problems/number-of-islands)
				- [Rotting Oranges](https://leetcode.com/problems/rotting-oranges)
				- [Accounts Merge](https://leetcode.com/problems/accounts-merge)
				- [Word Search](https://leetcode.com/problems/word-search)
				- [Minimum Height Trees](https://leetcode.com/problems/minimum-height-trees)
			- *Hard*
				- [Word Ladder](https://leetcode.com/problems/word-ladder)
		- *Binary - Easy*
		  collapsed:: true
			- [Add Binary](https://leetcode.com/problems/add-binary)
		- *Binary Search*
		  collapsed:: true
			- *Easy*
				- [Binary Search](https://leetcode.com/problems/binary-search)
				- [First Bad Version](https://leetcode.com/problems/first-bad-version)
			- *Medium*
				- [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array)
				- [Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store)
			- *Hard*
				- [Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling)
		- *Binary Search Tree*
		  collapsed:: true
			- *Easy*
				- [Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree)
			- *Medium*
				- [Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree)
				- [Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst)
		- *Binary Tree*
		  collapsed:: true
			- *Easy*
				- [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree)
				- [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree)
				- [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree)
				- [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree)
			- *Medium*
				- [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal)
				- [Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree)
				- [Binary Tree Right Side View](https://leetcode.com/problems/binary-tree-right-side-view)
				- [Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal)
			- *Hard*
				- [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree)
		- *Hash Table - Easy*
		  collapsed:: true
			- [Ransom Note](https://leetcode.com/problems/ransom-note)
		- *Recursion - Medium*
		  collapsed:: true
			- [Permutations](https://leetcode.com/problems/permutations)
			- [Subsets](https://leetcode.com/problems/subsets)
			- [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number)
		- *Linked List*
		  collapsed:: true
			- *Easy*
				- [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists)
				- [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle)
				- [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list)
				- [Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list)
			- *Medium*
				- [LRU Cache](https://leetcode.com/problems/lru-cache)
		- *Stack*
		  collapsed:: true
			- *Easy*
				- [Valid Parentheses](https://leetcode.com/problems/valid-parentheses)
				- [Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks)
			- *Medium*
				- [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation)
				- [Min Stack](https://leetcode.com/problems/min-stack)
			- *Hard*
				- [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water)
				- [Basic Calculator](https://leetcode.com/problems/basic-calculator)
				- [Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram)
		- *Heap*
		  collapsed:: true
			- *Medium*
				- [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin)
				- [Task Scheduler](https://leetcode.com/problems/task-scheduler)
			- *Hard*
				- [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream)
				- [Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists)
		- *Trie - Medium*
		  collapsed:: true
			- [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree)
			- [Word Break](https://leetcode.com/problems/word-break)
		- *Dynamic Programming*
		  collapsed:: true
			- *Easy*
				- [Climbing Stairs](https://leetcode.com/problems/climbing-stairs)
			- *Medium*
				- [Maximum Subarray](https://leetcode.com/problems/maximum-subarray)
				- [Coin Change](https://leetcode.com/problems/coin-change)
				- [Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum)
				- [Unique Paths](https://leetcode.com/problems/unique-paths)
	- Blind 75
	  id:: 64bcadf7-2fb0-4d59-89a7-7b565d18560b
	  collapsed:: true
		- [Best practice questions by the author of Blind 75 | Tech Interview Handbook](https://www.techinterviewhandbook.org/best-practice-questions/)
		- [LeetCode 75 - Study Plan - LeetCode](https://leetcode.com/study-plan/leetcode-75/)
		- [Blind 75 Leetcode problems : Detailed Video Solutions](https://takeuforward.org/interviews/blind-75-leetcode-problems-detailed-video-solutions/)
		- [Blind 75](https://leetcode.com/discuss/general-discussion/460599/blind-75-leetcode-questions)
		  collapsed:: true
			- ### Array
			- [Two Sum](https://leetcode.com/problems/two-sum/)
			- [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
			- [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
			- [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
			- [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
			- [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
			- [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
			- [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
			- [3 Sum](https://leetcode.com/problems/3sum/)
			- [Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
			  
			  ---
			- ### Binary
			- [Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/)
			- [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/)
			- [Counting Bits](https://leetcode.com/problems/counting-bits/)
			- [Missing Number](https://leetcode.com/problems/missing-number/)
			- [Reverse Bits](https://leetcode.com/problems/reverse-bits/)
			  
			  ---
			- ### Dynamic Programming
			- [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)
			- [Coin Change](https://leetcode.com/problems/coin-change/)
			- [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
			- [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
			- [Word Break Problem](https://leetcode.com/problems/word-break/)
			- [Combination Sum](https://leetcode.com/problems/combination-sum-iv/)
			- [House Robber](https://leetcode.com/problems/house-robber/)
			- [House Robber II](https://leetcode.com/problems/house-robber-ii/)
			- [Decode Ways](https://leetcode.com/problems/decode-ways/)
			- [Unique Paths](https://leetcode.com/problems/unique-paths/)
			- [Jump Game](https://leetcode.com/problems/jump-game/)
			  
			  ---
			- ### Graph
			- [Clone Graph](https://leetcode.com/problems/clone-graph/)
			- [Course Schedule](https://leetcode.com/problems/course-schedule/)
			- [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/)
			- [Number of Islands](https://leetcode.com/problems/number-of-islands/)
			- [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
			- [Alien Dictionary (Leetcode Premium)](https://leetcode.com/problems/alien-dictionary/)
			- [Graph Valid Tree (Leetcode Premium)](https://leetcode.com/problems/graph-valid-tree/)
			- [Number of Connected Components in an Undirected Graph (Leetcode Premium)](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
			  
			  ---
			- ### Interval
			- [Insert Interval](https://leetcode.com/problems/insert-interval/)
			- [Merge Intervals](https://leetcode.com/problems/merge-intervals/)
			- [Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
			- [Meeting Rooms (Leetcode Premium)](https://leetcode.com/problems/meeting-rooms/)
			- [Meeting Rooms II (Leetcode Premium)](https://leetcode.com/problems/meeting-rooms-ii/)
			  
			  ---
			- ### Linked List
			- [Reverse a Linked List](https://leetcode.com/problems/reverse-linked-list/)
			- [Detect Cycle in a Linked List](https://leetcode.com/problems/linked-list-cycle/)
			- [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
			- [Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
			- [Remove Nth Node From End Of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
			- [Reorder List](https://leetcode.com/problems/reorder-list/)
			  
			  ---
			- ### Matrix
			- [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)
			- [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
			- [Rotate Image](https://leetcode.com/problems/rotate-image/)
			- [Word Search](https://leetcode.com/problems/word-search/)
			  
			  ---
			- ### String
			- [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
			- [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
			- [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
			- [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
			- [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
			- [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
			- [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
			- [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
			- [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)
			- [Encode and Decode Strings (Leetcode Premium)](https://leetcode.com/problems/encode-and-decode-strings/)
			  
			  ---
			- ### Tree
			- [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
			- [Same Tree](https://leetcode.com/problems/same-tree/)
			- [Invert/Flip Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
			- [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
			- [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
			- [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)
			- [Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/)
			- [Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)
			- [Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/)
			- [Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst/)
			- [Lowest Common Ancestor of BST](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)
			- [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)
			- [Add and Search Word](https://leetcode.com/problems/add-and-search-word-data-structure-design/)
			- [Word Search II](https://leetcode.com/problems/word-search-ii/)
			  
			  ---
			- ### Heap
			- [Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
			- [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
			- [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/)
	- [LeetCode - Top Interview Questions - Easy Collection](https://leetcode.com/explore/featured/card/top-interview-questions-easy/)
	  collapsed:: true
		- *Array*
			- [Remove Duplicates from Sorted Array](https://leetcode.com/explore/featured/card/top-interview-questions-easy/92/array/727/)
			  collapsed:: true
				- My solution
					- ```javascript
					  var removeDuplicates = function(nums) {
					      
					      nums.forEach((el, ind) => {
					          if (nums.indexOf(el) !== nums.lastIndexOf(el)) {
					              nums.splice(el, 1)
					          }
					      })
					      console.log(`nums:`, nums)
					      return nums.length
					  };
					  ```
				- Best practice
					- ```javascript
					  var removeDuplicates = function (nums) {
					      var i = 0;
					      nums.forEach(el => {
					          if (el !== nums[i]) {
					              nums[++i] = el;
					          }
					      });
					      return nums.length && i + 1;
					  };
					  ```
						- Explanation 1
							- ```javascript
							  var removeDuplicates = function (nums) {
							      var i = 0;
							      nums.forEach(function (elem) { // iterate over each element of the nums array
							          if (elem !== nums[i]) { // if elem is not the same as the previous element
							              nums[++i] = elem; // add elem to the array and then increment i to point to the next index after setting elem
							          }
							      });
							      return nums.length && i + 1;  // if nums is empty, return 0, otherwise return i + 1
							  };
							  ```
						- Explanation 2
							- ((635eb08f-9a44-4545-88c0-b7064e94f590)) because the algorithm has to be done in-place - no creation of additional arrays
							- `i` was incremented for every new unique element
							- `return nums.length && i + 1`
								- The expression `nums.length && i + 1` in this function returns the length of the modified array if it is not empty (has at least one element) and `i + 1` otherwise.
								- The `&&` operator in JavaScript is known as the logical AND operator. It returns the first operand if it is falsy, and the second operand otherwise. In this case, `nums.length` is the first operand and `i + 1` is the second operand. If `nums.length` is 0 (which is a falsy value), the expression returns 0, indicating that the array is empty. Otherwise, if `nums.length` is not 0, the expression returns `i + 1`, which is the length of the modified array with duplicates removed.
								- This way, if the input array is empty, the function will return 0, and if there are any elements in the array, it will return the length of the modified array.
					- ```javascript
					  var removeDuplicates = function(nums) {
					      let pointer = 0;    
					      for (let i = 0; i < nums.length; i++) {
					          if (nums[i] !== nums[i+1]) {
					              nums[pointer] = nums[i];
					              pointer++;
					          }
					      }
					      return pointer;
					  };
					  ```
			- [Best Time to Buy and Sell Stock II](https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/564/)
			  collapsed:: true
				- My solution
					- ```javascript
					  var maxProfit = function(prices) {
					      let profit = 0
					      let prev
					      prices.reduce((acc, val, ind, arr) => {
					        // reduce starts with index 1 unlike other methods, so first need to set value of `prev` as otherwise the 0th index item is unassigned
					          if (!prev) {
					              prev = arr[ind-1]
					          }
					        // if next item is higher value than previous, then the profit is the difference
					          if (val > prev) {
					              profit += val - prev
					          }
					          prev = val // set `prev` to the current value
					      })
					          
					      return profit 
					  };
					  ```
						- Note: not using `acc` here. Probably should be swapped for `profit`
						- Similar "Implementation based on O(1) aux space"
							- ```javascript
							  var maxProfit = function(prices) {
							      let profitFromPriceGain = 0;
							      for( let i = 0 ; i < prices.length-1 ; i++ ){
							          if( prices[i] < prices[i+1] ){
							              profitFromPriceGain += (prices[i+1] - prices[i]);
							          }
							      }
							      return profitFromPriceGain;
							  }
							  ```
						- ((6350374d-3846-414b-a27e-7d32b86eec86))
				- Best practice
					- [O(n) sol by DP + state machine. Bottom-up DP + iteration](https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/564/discuss/803206/PythonJSJavaGoC++-O(n)-by-DP-Greedy-+-Visualization)
						- ```javascript
						  var maxProfit = function(prices) {
						      // It is impossible to sell stock on first day, set -infinity as initial value for curHold
						      let [curHold, curNotHold] = [-Infinity, 0];
						      
						      for(const stockPrice of prices){
						          let [prevHold, prevNotHold] = [curHold, curNotHold];
						          // either keep hold, or buy in stock today at stock price
						          curHold = Math.max(prevHold, prevNotHold - stockPrice );
						          // either keep not-hold, or sell out stock today at stock price
						          curNotHold = Math.max(prevNotHold, prevHold + stockPrice );
						      }
						      // Max profit must come from notHold state finally.
						      return curNotHold; 
						  };
						  ```
			- [Rotate Array](https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/646/)
			  collapsed:: true
				- My solution
					- ```javascript
					  var rotate = function(nums, k) {
					  	k = k % nums.length
					      nums.unshift(...nums.splice(-k));
					  };
					  ```
					- Wrong solution
						- Doesn't work if `k` > `nums.length`
							- ```javascript
							  var rotate = function(nums, k) {
							  	nums.unshift(...nums.splice(nums.length - k))
							  };
							  ```
						- Using immutable method not mutable
							- ```javascript
							  /**
							   * @param {number[]} nums
							   * @param {number} k
							   * @return {void} Do not return anything, modify nums in-place instead.
							   */
							  var rotate = function(nums, k) {
							      let arr1 = nums.slice(nums.length - k) 
							      console.log(`arr1:`, arr1)
							      let arr2 = nums.slice(0, nums.length - k)
							      console.log(`arr2:`, arr2)
							      return [...arr1, ...arr2]
							  };
							  ```
				- Best practice
					- ```javascript
					  var rotate = function (nums, k) {
					    for (let i = nums.length - 1; i >= 0; i--) {
					      nums[i + k] = nums[i];
					    }
					  
					    for (let j = k - 1; j >= 0; j--) {
					      nums[j] = nums.pop();
					    }
					  
					    // Time comlexity = O(a + b)
					  };
					  ```
						- Explanation 1
						  collapsed:: true
							- ```javascript
							  var rotate = function (nums, k) {
							    // i.e. nums = [1, 2, 3, 4, 5, 6, 7],  k = 3
							    for (let i = nums.length - 1; i >= 0; i--) {
							      nums[i + k] = nums[i];
							      // i = 6,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[6 + 3] = nums[6]
							      // nums[9] = 7              nums = [1, 2, 3, 4, 5, 6, 7, , , 7]
							  
							      // i = 5,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[5 + 3] = nums[5]
							      // nums[8] = 6              nums = [1, 2, 3, 4, 5, 6, 7, , 6, 7]
							  
							      // i = 4,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[4 + 3] = nums[4]
							      // nums[7] = 5              nums = [1, 2, 3, 4, 5, 6, 7, 5, 6, 7]
							  
							      // i = 3,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[3 + 3] = nums[3]
							      // nums[6] = 4              nums = [1, 2, 3, 4, 5, 6, 4, 5, 6, 7]
							  
							      // i = 2,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[2 + 3] = nums[2]
							      // nums[5] = 3              nums = [1, 2, 3, 4, 5, 3, 4, 5, 6, 7]
							  
							      // i = 1,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[1 + 3] = nums[1]
							      // nums[4] = 2              nums = [1, 2, 3, 4, 2, 3, 4, 5, 6, 7]
							  
							      // i = 0,  k = 3
							      // nums[i + k] = nums[i]
							      // nums[0 + 3] = nums[0]
							      // nums[3] = 1              nums = [1, 2, 3, 1, 2, 3, 4, 5, 6, 7]
							    }
							  
							    for (let j = k - 1; j >= 0; j--) {
							      // nums = [1, 2, 3, 1, 2, 3, 4, 5, 6, 7]
							      nums[j] = nums.pop();
							  
							      // j = 2
							      // nums[j] = nums.pop()
							      // nums[2] = 7               nums = [1, 2, 7, 1, 2, 3, 4, 5, 6]
							  
							      // j = 1
							      // nums[j] = nums.pop()
							      // nums[1] = 6               nums = [1, 6, 7, 1, 2, 3, 4, 5]
							  
							      // j = 0
							      // nums[j] = nums.pop()
							      // nums[0] = 5               nums = [5, 6, 7, 1, 2, 3, 4]
							    }
							  
							    // nums = [5, 6, 7, 1, 2, 3, 4]
							  
							    // Time comlexity = O(a + b)
							  };
							  ```
					- ```javascript
					  var rotate = function (nums, k) {
					      const len = nums.length
					      k = (k % len)
					      
					      let end = nums.splice(len - k)
					  
					      nums.splice(0,0,...end)
					  };
					  ```
			- ((63f3d7d0-a1ab-4f21-8ce8-fa4ae7aed53d))
			- ((0e542595-2f6d-4864-9ff5-9f953ccd7a29))
		- *Strings*
		- Linked List
		- Trees
		- Sorting and Searching
		- Dynamic Programming
		- Design
		- Math
		- Others
	- [Study cheatsheet from Grind 75 site](https://www.techinterviewhandbook.org/algorithms/study-cheatsheet/)
		-