Download Link: https://assignmentchef.com/product/solved-csce314-homework-1-programming-in-haskell
<br>
Below, the exercise problems are from the Haskell Textbook: “Programming in Haskell, 2nd Ed.” by Graham Hutton. Some problems are modified (with additional requirements) by the instructor. Please read textbook Chapters 1 thru 6 and the problem statements carefully. Keep the name and type of each function exactly the same as given in the problem statement and the skeleton code.

<strong>Problem 1. </strong>Put your full name, UIN, and <em>acknowledgements of any help received </em>in the head comment in your .hs file.

<strong>Problem 2. </strong> The <em>n</em>-th Lucas number <em>`<sub>n </sub></em>is recursively defined as follows: <em>`</em><sub>0 </sub>= 2 and <em>`</em><sub>1 </sub>= 1 and <em>`<sub>n </sub></em>= <em>`<sub>n</sub></em><sub>−1</sub>+<em>`<sub>n</sub></em><sub>−2 </sub>for <em>n</em>≥ 2. Write a <em>recursive </em>function lucas that computes the <em>n</em>-th Lucas number. lucas :: Int -&gt; Int

<strong>Problem 3. </strong> Chapter 1, Exercise 4 (modified).

Study the definition of the function qsort given in the text carefully, and try it out with an integer list, for example, [3,2,3,1,4]. You will notice that it sorts a list of elements in an ascending order.

3.1 (5 points) Write a recursive function qsort1 that sorts a list of elements in a <em>descending </em>order.

<h1>qsort1 :: Ord a =&gt; [a] -&gt; [a]</h1>

3.2 (10 points) Write your answer for this question in a block comment following the definition of function qsort1. Suppose that qsort1 is invoked with the input [3,2,3,1,4]. How many times is qsort1 called recursively (i.e., without counting the first invocation of qsort1 [3,2,3,1,4])? Explain step-by-step, in particular, at each level of recursive call, what are the values of x, smaller, and larger? [Hint: Think using a binary tree structure.]

<strong>Problem 4. </strong>Chapter 5, Exercise 9 (modified).

The scalar product function should be able to take not only two lists of the same length <em>n </em>but also those of <em>different </em>lengths.

4.1 Using the list comprehension with the zip prelude function, write the scalar product function.

<h1>scalarproduct :: [Int] -&gt; [Int] -&gt; Int</h1>

4.2 Explain carefully step-by-step the working of your scalarproduct function when it is invoked as follows.

<h1>*Main&gt; scalarproduct [1,2,3] [4..]</h1>

<strong>Problem 5. </strong>() Chapter 6, Exercise 7.

Like in the previous problem, the merge function should be able to take two sorted lists of different lengths as well as those of the same length.

<h1>merge :: Ord a =&gt; [a] -&gt; [a] -&gt; [a]</h1>

<strong>Problem 6. </strong>Chapter 6, Exercise 8.

Defining function halve is required (hint: use splitAt prelude function).

<h1>(8 points) msort :: Ord a =&gt; [a] -&gt; [a] (7 points) halve :: [a] -&gt; ([a], [a])</h1>

<strong>Problem 7. </strong>Write a recursive function isElem that returns True if a given value is an element of a list or False otherwise.

<h1>isElem :: Eq a =&gt; a -&gt; [a] -&gt; Bool</h1>

Sets are the most fundamental discrete structure on which all other discrete structures are built. In the following problem (and continuing in the next homework set), we are going to implement mathematical sets and their operations using Haskell lists.

A set is an <em>unordered </em>collection of elements (objects) without duplicates, whereas a list is an <em>ordered </em>collection of elements in which multiplicity of the same element is allowed. We define Set as a <em>type synonym </em>for lists as follows: type Set a = [a]

Even though the two types – Set a and [a] – are the same to the Haskell compiler, they communicate to the programmer that values of the former are <em>sets </em>and those of the latter are lists.

<strong>Problem 8. </strong>Write a recursive function that constructs a set from a list. Constructing a set from a list simply means removing all duplicate values. Use isElem from the previous problem in the definition of toSet.

<h1>toSet :: Eq a =&gt; [a] -&gt; Set a</h1>

<strong>Skeleton code and modes of running your code: </strong>The file hw1-skeleton.hs contains “stubs” for all the functions you are going to implement and placeholders for your explanations. The Haskell function bodies are initially undefined, a special Haskell value that has all possible types (thus, the skeleton file at least compiles).

In the skeleton file you find a test suite that test-evaluates the functions. Initially, all tests fail, until you provide correct implementation for the Haskell function. The tests are written using the HUnit library. Feel free to add more tests to the test suite.

The skeleton code can be loaded to the interpreter (&gt; ghci hw1-skeleton.hs). In the interpreter mode, you can test individual functions one at a time while you are implementing them. Evaluating the function main (by &gt; main in the interpreter mode) runs all of the tests in the test suite.

Alternatively, you can compile the code and execute it in the terminal mode:

<h1>&gt; ghc hw1-skeleton.hs and then</h1>

&gt; ./hw1-skeleton which has the same effect as when you do &gt; main in the interpreter mode.