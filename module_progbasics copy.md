# Programming Basics questions

## Computer science

### Data structures

#### *What is the purpose of the array (list in some programming languages) data structure? Name some methods of it!*
Arrays are lists that **store data in JavaScript**. <br>
They are created with brackets **"[]"**. <br>
Each item inside of an array is at a numbered position, or **index, starting at 0**. <br>
Variables that contain **arrays can be declared with let** or **const**. <br>
Arrays **mutated inside of a function will keep that change even outside the function**. <br>
We can **access one item in an array** using its index, with syntax like: **myArray[0]**. <br>
We can also **change an item in an array** using its index, with syntax **like myArray[0] = 'new string'** <br>
Arrays **can be nested inside other arrays**. <br>
To **access elements in nested arrays** chain indices using bracket notation: **myArray[0][2]** <br>
They have a **length property**, which allows you to see how many items are in an array : **myArray.length()** . <br>
They have their own **methods, including .push() and .pop()**, (and many more) which **add and remove items from an array**. <br>
* **myArray.reverse()** -> reverses the order of the elements of an array in place
* **myArray.slice(2,4)** -> extracts a section of the calling array and returns a new array (in this case the first element of myArray will be the third element and the fifth element won't show) and many [more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
.slice
.concat
.push
.pop

#### What are the differences between a list/array and a set?
The main difference between List and Set is that List allows duplicates while Set doesn't allow duplicates. List is an ordered collection it maintains the insertion order, which means upon displaying the list content it will display the elements in the same order in which they got inserted into the list.

#### What are the purpose and some methods of a dictionary/map data structure (simple data objects in JavaScript)?
A dictionary is a general-purpose data structure for storing a group of objects. A dictionary has a set of keys and each key has a single associated value. When presented with a key, the dictionary will return the associated value.

### Algorithms

#### Write a method (or pseudocode) that generates the Fibonacci sequence.
const fibonacci = n => {
  let a = 0, b = 1, c = n;
  
  for(let i = 2; i <= n; i++) {
    c = a + b;
    a = b;
    b = c;
  }
  
  return c;
};
#### How do you find a max value in a list/array if you can’t use any built-in functions or methods?
<script>
  
    // Array of numbers where the maximum
    // and minimum are to be found
    const array = [-1, 2, -5, 8, 16];
  
    // Setting a number of the given array as
    // value of max and min we choose 0th index
    // element as atleast one element should be
    // present in the given array
  
    let max = array[0], min = array[0];
    for (let i = 0; i < array.length; i++) {
  
        // If we get any element in array greater
        // than max, max takes value of that
        // larger number
        if (array[i] > max) { max = array[i]; }
  
        // If we get any element in array smaller
        // than min, min takes value of that
        // smaller number
        if (array[i] < min) { min = array[i]; }
    }
    console.log("max = " + max);
    console.log("min = " + min);
</script>


#### How do you find the average of values in a list/array if you can’t use any built-in functions or methods?
I sum all the values together and didvide them by the amount of values in the array.

#### What do we call an in-place sort?
sort() The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

#### Explain an algorithm which sorts a list!
Image result for Explain an algorithm which sorts a list! javascript
Sorting can be referred to as arranging files in some particular order. The arrangement performed can be based on the value of each file present. That particular order can be in either an ascending or descending fashion. Sorting algorithms are instructions given to a computer to arrange elements in a particular order.

### Programming paradigms - procedural

#### Explain the characteristics of the procedural programming paradigm.
The characteristics of procedural programming are: Procedural programming follows a top-down approach. The program is divided into blocks of codes called functions, where each function performs a specific task. Procedural programs model real-world processes as 'procedures' operating on 'data'.

#### What is the call stack?
A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

#### What is "stack overflow"?
A stack overflow is an undesirable condition in which a particular computer program tries to use more memory space than the call stack has available. In programming, the call stack is a buffer that stores requests that need to be handled.

#### What are the main parts of a function?
A function has three parts, a set of inputs, a set of outputs, and a rule that relates the elements of the set of inputs to the elements of the set of outputs in such a way that each input is assigned exactly one output.

#### What is the difference between parameters and arguments?
The values that are declared within a function when the function is called are known as an argument. Whereas, the variables that are defined when the function is declared are known as a parameter.

### Programming languages - JavaScript

#### What does it mean that a type is immutable? Tell examples.
Mutable is something you can change. Immutable is just the opposite of that. So, mutability is the ability to change over time. Immutability means something is unchanging over time.

like a const value and a let/var value

#### What does it mean that an object is mutable? Tell examples.
Mutable is a type of variable that can be changed. In JavaScript, only objects and arrays are mutable, not primitive values. (You can make a variable name point to a new value, but the previous value is still held in memory. Hence the need for garbage collection.)

What is an example of a mutable object?
The objects in which you can change the fields and states after the object is created are known as Mutable objects. Example: java. util. Date, StringBuilder, and etc.

#### What is a conditional expression?
The conditional (ternary) operator is the only JavaScript operator that takes three operands: a condition followed by a question mark ( ? ), then an expression to execute if the condition is truthy followed by a colon ( : ), and finally the expression to execute if the condition is falsy.

#### What are different types of arguments?

Rest, default, and destructured parameters.

#### What is variable shadowing?
Shadowing: when a variable is declared in a certain scope having the same name defined on its outer scope and when we call the variable from the inner scope, the value assigned to the variable in the inner scope is the value that will be stored in the variable in the memory space

#### What can happen if you try to delete/add an item from/to a array, while you are iterating over it?
ha torlok egy elemt akkor annak a  helyer elkdezme beirni a a torolt helytol az osszes indexet
#### If you need to access the iterator variable after a for loop, how would you do it?
i="
for (i =0)
"${i}"
#### What type of elements can a list contain?
strings, integers
#### What can the + operator be used for?
++	Increment operator. Increase operand value by one
#### What is string formatting?
String formatting is also known as String interpolation. It is the process of inserting a custom string or variable in predefined text. custom_string = "String formatting" print(${custom_string} is a powerful technique") String formatting is a powerful technique.
#### Name 4 iterable types.
string
array
object

#### Does the order of the function definitions matter? Why?
Yes.
 why exactly does JavaScript function order matter? Well, function order matters a huge amount when a variety of functions exist inside multiple scopes of a program. For a JavaScript program to perform correctly, functions in the inner scope must be able to access functions in the outer scope.
#### What is spread/rest syntax for?
Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element
#### What does a destructuring assignment mean?
The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.
#### What happens when you try to assign the result of a function which has no return statement to a variable?
If no return value is specified, JavaScript will return undefined .

## Software engineering

### Debugging

#### What techniques can you use while debugging a program?
Debugging strategies
Incremental and bottom-up program development. ...
Instrument program to log information. ...
Instrument program with assertions. ...
Use debuggers. ...
Backtracking. ...
Binary search. ...
Problem simplification. ...
A scientific method: form hypotheses.

#### What does step over, step into and step out mean when using the debugger?
Step Into

A method is about to be invoked, and you want to debug into the code of that method, so the next step is to go into that method and continue debugging step-by-step.

Step Over

A method is about to be invoked, but you're not interested in debugging this particular invocation, so you want the debugger to execute that method completely as one entire step.

Step Return

You're done debugging this method step-by-step, and you just want the debugger to run the entire method until it returns as one entire step.

Resume

You want the debugger to resume "normal" execution instead of step-by-step

Line Breakpoint

You don't care how it got there, but if execution reaches a particular line of code, you want the debugger to temporarily pause execution there so you can decide what to do.

Eclipse has other advanced debugging features, but these are the basic fundamentals.


#### How can you start to debug a program from a certain line using the debugger?
To start your app with the debugger attached, press F11 (Debug > Step Into). F11 is the Step Into command and advances the app execution one statement at a time. When you start the app with F11, the debugger breaks on the first statement that gets executed.

### Version control

#### What are the advantages of using a version control system?
A version control system helps track every little change made to an existing code base, with details like who made the changes, when it was made, what the changes are, etc. So, it also helps to roll back code, merge codes developed by several programmers, and check out code.

#### What is the difference between the working directory, the staging area and the repository in git?
The working area is where files that are not handled by git. These files are also referred to as "untracked files." Staging area is files that are going to be a part of the next commit, which lets git know what changes in the file are going to occur for the next commit.
#### What are remote repositories in git?
A remote in Git is a common repository that all team members use to exchange their changes. In most cases, such a remote repository is stored on a code hosting service like GitHub or on an internal server. In contrast to a local repository, a remote typically does not provide a file tree of the project's current state
#### Why does a merge conflict occur?
Often, merge conflicts happen when people make different changes to the same line of the same file, or when one person edits a file and another person deletes the same file. You must resolve all merge conflicts before you can merge a pull request on GitHub.
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
 git add  git commit git push
#### What does it mean atomic commits and descriptive commit messages?
Atomic:
In the field of computer science, an atomic commit is an operation that applies a set of distinct changes as a single operation. If the changes are applied, then the atomic commit is said to have succeeded.

descriptive:
The guideline of a descriptive commit message is you should at least know what were you working with just by reading the commit message. The convention is usually using imperative sentences, and present tense. For example: change aspect ratio for company profile video.
#### What’s the difference between Git and GitHub?
Git is a version control system that lets you manage and keep track of your source code history. GitHub is a cloud-based hosting service that lets you manage Git repositories. If you have open-source projects that use Git, then GitHub is designed to help you better manage them.

## Software design

### Clean code

#### What does clean code mean?
Clean code is code that is easy to understand and easy to change.
#### What steps do we usually do during a clean code refactoring?
Applying the Red-Green-Refactor method, developers break refactoring down into three distinct steps:
Stop and consider what needs to be developed. [RED]
Get the development to pass basic testing. [GREEN]
Implement improvements. [REFACTOR]

### Error handling

#### What is error/exception handling?
What is exception handling. Exception handling is one of the powerful JavaScript features to handle errors and maintain a regular JavaScript code/program flow. An exception is an object with an explanation of what went amiss. Also, it discovers where the problem occurred

error handling:

Error handling handles the runtime errors in the JavaScript. try is the keyword creates the try block. Here the code that can cause exception is under the wrap under this block. The catch is the keyword creates the catch block
#### What are the basics of exception handling in JavaScript?

A try-catch-finally statement is a code or program that handles exceptions.
The try clause runs the code that generates exceptions.
The catch clause catches exceptions that are thrown.
A finally clause always gets executed.
The throw statement generates exceptions.

#### In which case should we catch an exception? Why?
tortenik egy olyan kivetel amit helyben nem tudunk megoldani es kesobb oldjuk meg es ott le is kezeljuk
#### What can/should we do with an exception in the `catch` block?
solve it 


#### What does the `finally` statement do in a `try-catch` block in JavaScript?
a finally mindig lefut 

a sima catach nem feltetlen fut le