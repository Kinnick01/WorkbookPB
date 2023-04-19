# Web Module Questions

### Functional patterns

#### What is a callback function?

A callback is a function passed as an argument to another function. This technique allows a function to call another function. A callback function can run after another function has finished.


#### What is ECMA script ? 
ECMAScript is a JavaScript standard intended to ensure the interoperability of web pages across different browsers.

### What is the difference between Javascript & ECMA script ?
JavaScript is a general-purpose scripting language that conforms to the ECMAScript specification. The ECMAScript specification is a blueprint for creating a scripting language. JavaScript is an implementation of that blueprint. On the whole, JavaScript implements the ECMAScript specification as described in ECMA-262.

#### What is the difference between `let` & `var` ?
The main difference between let and var is that scope of a variable defined with let is limited to the block in which it is declared while variable declared with var has the global scope. So we can say that var is rather a keyword which defines a variable globally regardless of block scope.

#### Write an example where using the `var` declaration instead of the `let` could create a hard to debug code.




#### Give a practical example where you would use the `reduce` function in javascript.
const topSix = [
    { name: "Nigeria", position: "1st", points: 43 },
    { name: "England", position: "2nd", points: 37 },
    { name: "USA", position: "3rd", points: 35 },
    { name: "South Africa", position: "4th", points: 30 },
    { name: "Brazil", position: "5th", points: 27 },
    { name: "Korea", position: "6th", points: 23 }
]
 
const totalPoints = topSix.reduce((acc, currTeam) => acc + currTeam.points, 0);
 
console.log(totalPoints) // Prints 195



#### Give a practical example where you would use the `map` function in javascript.
const mathScores = [39, 50, 45, 41, 50];
  
mathScores.map((currentValue, index, array) => {
    console.log('Current value:' + currentValue);
    console.log('Index:' + index);
    console.log('Array:' + array);
    return currentValue;
})



"Current value:39"
"Index:0"
"Array:39,50,45,41,50"
...
"Current value:50"
"Index:4"
"Array:39,50,45,41,50"


#### Give a practical example where you would use the `filter` function in javascript.
1. Remove Repeated Values;

const numbers = [3, 12, 54, 12, 4, 4, 3, 12, 16];
const filteredNumbers = numbers.filter((number, index) => numbers.indexOf(number) === index);
console.log(filteredNumbers); // [3, 12, 54, 4, 16]



### Web basics

#### What is a web server?
A web server is software and hardware that uses HTTP (Hypertext Transfer Protocol) and other protocols to respond to client requests made over the World Wide Web. The main job of a web server is to display website content through storing, processing and delivering webpages to users.

#### Explain the client-server architecture.
client-server architecture, architecture of a computer network in which many clients (remote processors) request and receive service from a centralized server (host computer). Client computers provide an interface to allow a computer user to request services of the server and to display the results the server returns.


#### What is the difference between synchronous and asynchronous execution?

Synchronous execution means the first task in a program must finish processing before moving on to executing the next task whereas asynchronous execution means a second task can begin executing in parallel, without waiting for an earlier task to finish.
#### What is `npm`? Why is it useful?
NPM is used to manage dependencies for packages. If you were to unpack a framework and use it outside NPM, you would have to do this every time you want to update the framework. NPM does this for you. You always know what version you're on, and you can limit a dependency to a specific major/minor/patch version.

#### What is the difference between the `depdendencies` & `devDependencies` in a `package.json` file ?
"dependencies" : Packages required by your application in production. "devDependencies" : Packages that are only needed for local development and testing.

#### What would be the impact of javascript `fetch` if it was not asyncronous ?
The code won't go forward until the fetch returns with the information
#### Wh benefits would bring to a developer to use the `Postman` application ?
you can test the backend server and test if the api's work 


#### List the parts of the URL.
A URL consists of five parts: the scheme, subdomain, top-level domain, second-level domain, and subdirectory.

#### What is query parameter?
Query parameters are a defined set of parameters attached to the end of a url. They are extensions of the URL that are used to help define specific content or actions based on the data being passed. To append query params to the end of a URL, a ‘?’ Is added followed immediately by a query parameter.
To add multiple parameters, an ‘&’ is added in between each. These can be created by any variation of object types or lengths such as String, Arrays and Numbers. The following is an example:


http://example.com/path?name=Branch&products=[Journeys,Email,Universal%20Ads]


#### What kind of HTTP status codes do you know?
Informational responses (100–199)
Successful responses (200–299)
Redirection messages (300–399)
Client error responses (400–499)
Server error responses (500–599)

200 OK
400 Bad Request
403 Forbidden
404 Not Found
500 Internal Server Error

#### How does an HTTP Request look like? 

An HTTP client sends an HTTP request to a server in the form of a request message which includes following format: A Request-line. Zero or more header (General|Request|Entity) fields followed by CRLF. An empty line (i.e., a line with nothing preceding the CRLF) indicating the end of the header fields.

### What are the most relevant HTTP header fields?
General-header: These header fields have general applicability for both request and response messages.

Client Request-header: These header fields have applicability only for request messages.

Server Response-header: These header fields have applicability only for response messages.

Entity-header: These header fields define meta information about the entity-body or, if no body is present, about the resource identified by the request

#### How does an HTTP Response look like?

After receiving and interpreting a request message, a server responds with an HTTP response message: A Status-line. Zero or more header (General|Response|Entity) fields followed by CRLF. An empty line (i.e., a line with nothing preceding the CRLF) indicating the end of the header fields


### What are the most relevant HTTP header fields?





#### Why should you ignore the `node_modules` folder in `.gitignore` ?


The node_modules/ folder is the folder where all packages required by your JavaScript project are downloaded and installed. This folder is commonly excluded from a remote repository because it has a large size and you shouldn't add code that you didn't write to the repository.


### Rest API: Serve and Fetch

#### Why is it recommend for a developer to use the http methods `get`, `put`, `delete` ?
GET
The GET method requests transfer of a current selected representation for the target resource. GET is the primary mechanism of information retrieval


POST
The POST method requests that the target resource process the representation enclosed in the request according to the resource’s own specific semantics.


PUT
The PUT method requests that the state of the target resource be created or replaced with the state defined by the representation enclosed in the request message payload.



DELETE
The DELETE method requests that the origin server remove the association between the target resource and its current functionality.



#### How does a `POST` request look like when it is made from a web browser (on the front end written) ?



#### What is an API?
Application Programming Interface, which is a software intermediary that allows two applications to talk to each other. 
#### What is REST API?
A REST API (also known as RESTful API) is an application programming interface (API or web API) that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services. REST stands for representational state transfer and was created by computer scientist Roy Fielding
#### What is JSON and how do we use it?
JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax. It is commonly used for transmitting data in web applications (e.g., sending some data from the server to the client, so it can be displayed on a web page, or vice versa).
#### What is API versioning ?
API versioning is the practice of transparently managing changes to your API. 


Managing an API boils down to defining and evolving data contracts and dealing with breaking changes. The most effective way to evolve your API without breaking changes is to follow effective API change management principles.
#### Give 3 examples of HTTP response status codes ? Explain what each number means.

### Advanced JavaScript

#### How does the `ternary operator` looks like in javascript?

something1 ? (if somthing1 is true): if something1 is false
#### How to import a function from another module in JavaScript?
import Function from "../Function.js"
#### What is a shallow copy on an object?

A shallow copy of an object is a copy whose properties share the same references (point to the same underlying values) as those of the source object from which the copy was made.

#### What is a callback function?

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

## Tell some examples of its usage.
function greeting(name) {
  alert(`Hello, ${name}`);
}

function processUserInput(callback) {
  const name = prompt("Please enter your name.");
  callback(name);
}

processUserInput(greeting);

#### What is object destructuring in javascript?
Destructuring is a JavaScript expression that allows us to extract data from arrays, objects, and maps and set them into new, distinct variables.

const user = {
  givenname: "adam"
surname: "kraus
}


console.log(user.givenname)  //awaited log (adam)
#### What is array destructuring in javascript?

#### What is the spread operator in `js` ?
The JavaScript spread operator ( ... ) allows us to quickly copy all or part of an existing array or object into another array or object.

#### What are the differences between the `arrow` function and the regular `function`?
Regular functions created using function declarations or expressions are constructible and callable. Since regular functions are constructible, they can be called using the new keyword. However, the arrow functions are only callable and not constructible, i.e arrow functions can never be used as constructor functions.

1. Syntax
2. Arguments binding
3. Use of this keyword
4. Using new keyword
5. No duplicate named parameters
Arrow functions can never have duplicate named parameters, whether in strict or non-strict mode.

#### What is the `import` keyword used for?
The import keyword is used to import a package, class or interface.
#### What is the `required` used for?
1) require()
In NodeJS, require() is a built-in function to include external modules that exist in separate files. require() statement basically reads a JavaScript file, executes it, and then proceeds to return the export object. require() statement not only allows to add built-in core NodeJS modules but also community-based and local modules.


#### What are template literals?
Template literals are literals delimited with backtick ( ` ) characters, allowing for multi-line strings, for string interpolation with embedded expressions, and for special constructs called tagged templates.

### Testing basics

#### What is code coverage? 

Code coverage is the percentage of code which is covered by automated tests.
### Why is it used?
Code coverage is a metric that can help you understand how much of your source is tested.
#### What is a test case? What is an assertion? Give examples!

A test case is a set of actions performed on a system to determine if it satisfies software requirements and functions correctly.

An assertion is a statement in programming languages that enables you to test your assumptions about your program.
GET http://localhost:8080/employees

###

POST http://localhost:8080/employees
Content-Type: application/json

{
    "name": "Robert Downey Jr",
    "position": "sidekick",
    "level": "SENIOR"
}

###

DELETE http://localhost:8080/employees/6332c84da41fd3425a2ae66e


###

PATCH http://localhost:8080/employees/6332c84ea41fd3425a2ae670
Content-Type: application/json

{
    "level": "expert"
}

#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
Unit Testing Best Practices 
1. Write Readable, Simple Tests
2. Write Deterministic Tests
3. Test One Scenario Per Test
4. Unit Tests Should Be Automated
5. Write Isolated Tests
6. Avoid Test Interdependence
7. Avoid Active API Calls
8. Combine Unit and Integration Testing
9. Ensure Unit Tests are Repeatable and Scalable
10. Test for Security Issues as Part of Your Unit Tests



#### What is arrange/act/assert pattern?
The idea is to develop a unit test by following these 3 simple steps: Arrange – setup the testing objects and prepare the prerequisites for your test. Act – perform the actual work of the test. Assert – verify the result.
#### How do you test asynchronous code with `jest` ?
Instead of putting the test in a function with an empty argument, use a single argument called done . Jest will wait until the done callback is called before finishing the test.

#### What is `setup` & `teardown` in jest ?
Often while writing tests you have some setup work that needs to happen before tests run, and you have some finishing work that needs to happen after tests run. Jest provides helper functions to handle this.


For that it has two important methods, setUp() and tearDown() . setUp() — This method is called before the invocation of each test method in the given class. tearDown() — This method is called after the invocation of each test method in given class
#### Give an example when you would use in `jest` the `toBe` & `toEqual` assertions.
Use .toBe to compare primitive values or to check referential identity of object instances. It calls Object.is to compare values, which is even better for testing than === strict equality operator.


Use .toEqual to compare recursively all properties of object instances (also known as "deep" equality). It calls Object.is to compare primitive values, which is even better for testing than === strict equality operator.

### React basics

#### What benefits does it bring for a developer to use `components` (opposed of writing all the code in a single file) ?
For designers and developers, the primary benefit of components lies in their reusability. Each component represents an element that can be reused throughout a site (often with minor customizations based on some input). That means you can design and build it once and use it everywhere.
#### What is the difference between Element and Component?

React Element does not have any methods, making it light and faster to render than components.
Element	                                                    Component
A React element is an object representation of a DOM node.	A component encapsulates a DOM tree.
Elements are immutable i,e once created cannot be changed.	The state in a component is mutable.



#### How do you pass values between components in `react`?
With props


#### What is `key` prop?
React's key prop gives you the ability to control component instances.
Key prop helps React identify which items have changed, are added, or are removed.

const List = () => {
    const listItems = ['Item 1', 'Item 2', 'Item 3'];

    return (
        <ul>
            {listItems.map((item, index)) => <li key={index}>{item}</li>}
        </ul>
    );
}
#### How does a child component pass data to it's parent component ?
Pass a function as a prop to the Child component. Call the function in the Child component and pass the data as arguments. Access the data in the function in the Parent .
#### Write the code to create in JSX an HTML DIV element that has the innerText the contents of the variable `let name = 'Andrew'`
let name = "andrew"

function App() {
  return (
    <div className="App">
      <div>{name}</div>
    </div>
  );
}

export default App;
#### Write the code to create in JSX an unordered list from the array `let names = ["Mathew", "John", "Maverik"]`

function App() {
  return (
    <div className="App">
      <ul>
  {names.map(element => <li>{element}</li>)}
</ul>
      
      <div>{name}</div>
    </div>
  );
}
#### Write the code to set the background color red of a div in JSX.
.app{
  background-color: red
}
### Testing react

#### What are unit tests, integration tests? What is the major difference between these two?
- `Unit testing is a software development process in which the smallest testable parts of an application, called units, are individually and independently scrutinized for proper operation`
- `Integration testing -- also known as integration and testing (I&T) -- is a type of software testing in which the different units, modules or components of a software application are tested as a combined entity.`
- `Unit Testing, accessibility of code is required, as it tests the written code, while for Integration Testing, access to code is not required, since it tests the interactions and interfaces between modules.`
#### What is unit testing?
- ``
#### What does `mocking` mean from a testing perspective ? Give an example when you would use it.
- `Mocking is a process used in unit testing when the unit being tested has external dependencies. The purpose of mocking is to isolate and focus on the code being tested and not on the behavior or state of external dependencies.`
- ``
#### How do you test that function was called `at least` 2 times using `jest` ?
- ``
#### Name 4 benefits a developer gets from writing tests.
-``
### React patterns

#### What is the difference between Real DOM and Virtual DOM?
- `Manipulating DOM is slow, but manipulating Virtual DOM is fast as nothing gets drawn on the screen. So each time there is a change in the state of our application, the virtual DOM gets updated first instead of the real DOM`
#### When adding an item to an array, why is it necessary to pass a new array to the `useState` hook ?
- `useState create queues for React core to update the state object of a React component. So the process to update React state is asynchronous for performance reasons. That's why changes don't feel immediate.`
#### Describe what techniques or tools you use to debug a react app.
- `browser inspector`
- `console`
#### What is the difference between a react `class` component & a `functional` component ?
- ` The class component is a regular ES6 class that extends the React component library to create a stateful component. In contrast, functional components with hooks can be used to build stateful or presentational components.`
#### Name 3 lifecycle states in a react `functional` component.
- `A React component undergoes three phases in its lifecycle: mounting, updating, and unmounting. The mounting phase is when a new component is created and inserted into the DOM or, in other words, when the life of a component begins. This can only happen once, and is often called “initial render.”`
#### What is conditional rendering in `react` ? Give an example.
- `In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application. Conditional rendering in React works the same way conditions work in JavaScript`
- `Example:`
```
function Goal(props) {
  const isGoal = props.isGoal;
  return (
    <>
      { isGoal ? <MadeGoal/> : <MissedGoal/> }
    </>
  );
}
```
#### Write the code that prints to the console `component destroyed` when the component it is part of is removed from the DOM tree.
- ``
#### Why is there an infinite loop in this code
```function App() {
  const [count, setCount] = useState(0); //initial value of this 
  useEffect(() => {
    setCount((count) => count + 1); //increment this Hook
  }); //no dependency array.
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```
- `useEffect should have an empty array as a dependency so it only renders once when the page loads`
#### Why is there an infinite loop in this code
```
  async function App() {
  const [count, setCount] = useState("");
  setCount(count + 1);
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```
- `useState always rerenders the page and count is +1 as was in the previous render`

### Mongo & mongoose

#### What is a database schema ?
- `A schema is a JSON object that defines the the structure and contents of your data`
#### Why is the `id` unique in a database ?
- `A unique index ensures that the indexed fields do not store duplicate values; i.e. enforces uniqueness for the indexed fields. By default, MongoDB creates a unique index on the _id field during the creation of a collection.`
#### What are the advatanges & disadvatages of using `lean()` function in a mongo query ?
- `The lean option tells Mongoose to skip hydrating the result documents. This makes queries faster and less memory intensive, but the result documents are plain old JavaScript objects (POJOs), not Mongoose documents. In this tutorial, you'll learn more about the tradeoffs of using lean().`
#### Write the code to store the object `{name: "Andrew", age: 10}` to a mongo database. You can ignore the part of connection parameters.
```
...
User.create(
    { name: "Andrew", age: 10}
  );
  ...
  ```
#### Write the code to delete from a mongo database all employees that are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.
```
...
User.deleteMany({ age: {$gt 18} });
...
```
#### Write the code to display in the console from a mongo database the employees who are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.

```
...
console.log(User.find({age: {$gt 18} }));
...

```
#### Write the code to update from a mongo database the employees with name='John' and set the new age to 8. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.

```
Users.updateMany({ name: John }, { $set: { age: 8 } })

```


### Authentication (cookies + google)

#### How to properly store passwords?
#### What is encryption and decryption?
#### What is hashing?
#### What is OAuth2?
#### What is the difference between encryption and hashing? When would you use which?
#### How/where would you store sensitive data (like db password, API key, ...) of your application?
#### What would you use a session for?
#### What would you use a cookie for?

### Mern stack

#### What does `MERN` stand for in the context of web development ?
Mongo
Express
React
Node
#### What is routing in the context of a `react` app ?
Routing is a process in which a user is directed to different pages based on their action or request.

#### What is routing in the context of an `express` app ?
Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on). Each route can have one or more handler functions, which are executed when the route is matched.
#### What is `CORS` policy ?
Cross-origin resource sharing is a mechanism that allows restricted resources on a web page to be requested from another domain outside the domain from which the first resource was served.
#### What advantages does a developer have for using `bootstrap` or `material ui` ?
its easy as 1-2-3