
# Project Title

A brief description of what this project does and who it's for

# JavaScript_Interview_Question

## JavaScript Interview Questions

1. **[What are the different data types in JavaScript?](#q1-what-are-the-different-data-types-in-javascript)**
2. **[What is the difference between `var`, `let`, and `const`?](#q2-what-is-the-difference-between-var-let-and-const)**
3. **[What are primitive vs non-primitive types?](#q3-what-are-primitive-vs-non-primitive-types)**
4. **[What is hoisting in JavaScript?](#q4-what-is-hoisting-in-JavaScript)**  
5. **[What is the difference between regular functions and arrow functions?](#q5-what-is-the-difference-between-regular-functions-and-arrow-functions)**
6. **[What is a closure? How does it work?](#q6-what-is-a-closure-how-does-it-work)**
7. **[What is the difference between call(), apply(), and bind() in JavaScript?](#q7-what-is-the-difference-between-call-apply-and-bind-in-javascript)**
8. **[What is IIFE (Immediately Invoked Function Expression)?](#q8-what-is-iife-immediately-invoked-function-expression)**
9. **[How to create objects in JavaScript?](#q9-how-to-create-objects-in-javascript)**
10. **[What is the difference between == and ===?](#q10-what-is-the-difference-between--and-)**
11. **[What are JavaScript array methods like map(), filter(), reduce(), find(), etc.?](#q11-what-are-JavaScript-array-methods-like-map-filter-reduce-find-etc)**
12. **[What are callbacks? How do they work?](#q12-what-are-callbacks-How-do-they-work)**
13. **[What are Promises? How are they better than callbacks?](#q13-what-are-Promises-How-are-they-better-than-callbacks)**
14. **[What is async/await? How is it better than .then()?](#q14-what-is-asyncawait-how-is-it-better-than-then)**
15. **[What is the Event Loop in JavaScript?](#q15-what-is-the-event-loop-in-javascript)**
16. **[Explain microtask vs macrotask queue.](#q16-explain-microtask-vs-macrotask-queue)**
17. **[What are setTimeout, setInterval, and clearTimeout?](#q17-what-are-settimeout-setinterval-and-cleartimeout)**
18. **[What is callback hell and how do you avoid it?](#q18-what-is-callback-hell-and-how-do-you-avoid-it)**
19. **[What is the DOM? How do you manipulate it with JS?](#q19-what-is-the-dom-how-do-you-manipulate-it-with-js)**
20. **[What are event bubbling and event capturing?](#q20-what-are-event-bubbling-and-event-capturing)**
21. **[What are localStorage, sessionStorage, and cookies?](#q21-what-are-localstorage-sessionstorage-and-cookies)**
22. **[What is the `this` keyword and how does it behave in different contexts?](#q22-what-is-the-this-keyword-and-how-does-it-behave-in-different-contexts)**
23. **[What is destructuring in JavaScript (arrays/objects)?](#q23-what-is-destructuring-in-javascript-arraysobjects)**
24. **[What is middleware in Express.js? How does it work?](q24-what-is-middleware-in-expressjs-how-does-it-work)**
25. **[Explain how you implemented JWT-based authentication in your project.](#q25-explain-how-you-implemented-jwt-based-authentication-in-your-project)**
26. **[ Difference between process.nextTick(), setImmediate(), and setTimeout()?](#q26-difference-between-processnexttick-setimmediate-and-settimeout)**
27. **[How do you structure a Node.js project?](#q27-how-do-you-structure-a-nodejs-project)**
28. **[How do you handle errors in Express?](#q28-how-do-you-handle-errors-in-express)**
29. **[How do you define a model using Mongoose?](#q29-how-do-you-define-a-model-using-mongoose)**
30. **[Explain MongoDB aggregation pipeline stages.](#q30-explain-mongodb-aggregation-pipeline-stages)**
31. **[How do you secure a Node.js backend application?](#q31-how-do-you-secure-a-nodejs-backend-application)**
32. **[How do you deploy a Node.js app?](#q32-how-do-you-deploy-a-nodejs-app)**
33. **[What are streams in Node.js?](#q33-what-are-streams-in-nodejs)**
34. **[How does the Node.js event loop work?](#q34-how-does-the-nodejs-event-loop-work)**
35. **[How do you test your APIs?](#q35-how-do-you-test-your-apis)**
36. **[How would you scale a Node.js app for high traffic?](#q36-how-would-you-scale-a-nodejs-app-for-high-traffic)**
37. **[What is Mongoose? Why do we use it in Node.js projects?](#q37-what-is-mongoose-why-do-we-use-it-in-nodejs-projects)**
38. **[How do you define a model in Mongoose? What are schema types and validations?](#q38-how-do-you-define-a-model-in-mongoose-what-are-schema-types-and-validations)**
39. **[What are some common Mongoose schema options?](#q39-what-are-some-common-mongoose-schema-options)**
40. **[How do you perform basic CRUD operations using Mongoose?](#q40-how-do-you-perform-basic-crud-operations-using-mongoose)**
41. **[What is the aggregation framework in MongoDB?](#q41-what-is-the-aggregation-framework-in-mongodb)**
42. **[How would you write an aggregation query to calculate total sales per product category?](#q42-how-would-you-write-an-aggregation-query-to-calculate-total-sales-per-product-category)**
43. **[Explain the $lookup stage in aggregation. How is it different from SQL joins?](#q43-explain-the-lookup-stage-in-aggregation-how-is-it-different-from-sql-joins)**
44. **[What’s the difference between $project and $addFields in MongoDB?](#q44-whats-the-difference-between-project-and-addfields-in-mongodb)**
45. **[How do you design relationships in MongoDB? When to embed vs. reference?](#q45-how-do-you-design-relationships-in-mongodb-when-to-embed-vs-reference)**
46. **[What are indexes in MongoDB? When should you use them?](#q46-what-are-indexes-in-mongodb-when-should-you-use-them)**
47. **[How would you optimize large MongoDB queries or aggregation pipelines?](#q47-how-would-you-optimize-large-mongodb-queries-or-aggregation-pipelines)**


# Questions and Answers

### Q1. What are the different data types in JavaScript?

JavaScript supports two broad categories of data types:

#### ✅ Primitive Data Types:
- **String**, **Number**, **Boolean**, **null**, **undefined**, **Symbol**, **BigInt**

#### ✅ Non-Primitive (Reference) Data Types:
- **Object**, **Array**, **Function**

```js
// Primitive types
let name = "John";     // String
let age = 30;          // Number
let isLoggedIn = true; // Boolean
let nothing = null;    // null
let notDefined;        // undefined

// Non-primitive types
let person = { name: "Alice", age: 25 }; // Object
let colors = ["red", "blue"];            // Array
let greet = function() { console.log("Hi"); }; // Function
```
- [Back to Top](#javascript-interview-questions)

### Q2. What is the difference between `var`, `let`, and `const`?
   - **`let`:** It allows the declaration of block-scoped variables. The variable can be reassigned within the same block.
   - **`const`:** It also declares block-scoped variables but is used for constants that cannot be reassigned.
   - **`var`:** It declares a variable globally or locally to the entire function, regardless of block scope. It can be reassigned.
   - Example:
        ```
        function testVar() {
           if (true) {
             var x = 1;
           }
           console.log(x); // 1 (var is function-scoped)
         }

         function testLet() {
           if (true) {
             let y = 2;
           }
           // console.log(y); // Error! y is block-scoped
         }

         const z = 3;
         // z = 4; // Error! Cannot re-assign const

        ```
   - [Back to Top](#javascript-interview-questions)

### Q3. What are primitive vs non-primitive types?

   - 📌 Primitive Types:

      Store actual value
      Immutable (cannot be changed)
      Examples: String, Number, Boolean, null, undefined, Symbol, BigInt

   - 📌 Non-Primitive Types:

      Store reference to value
      Mutable (can be changed)
      Examples: Object, Array, Function
    - Example:
        ```
        let a = "hello"; // primitive
      let b = { msg: "hi" }; // non-primitive
      
      let c = b;
      c.msg = "hello again";
      console.log(b.msg); // Output: "hello again"
        ```
   - [Back to Top](#javascript-interview-questions)

### Q4. What is hoisting in JavaScript?

Hoisting is JavaScript's behavior of moving variable and function declarations to the top of their scope during the compile phase.

- var is hoisted and initialized as undefined

- let and const are hoisted but not initialized

- Function declarations are hoisted completely (code + definition)

    - Example:
        ```
        console.log(a); // undefined
        var a = 5;

        console.log(b); // ReferenceError
        let b = 10;

        greet(); // "Hello"
        function greet() {
        console.log("Hello");
        }

        ```

   - [Back to Top](#javascript-interview-questions)

### Q5. What is the difference between regular functions and arrow functions?
📌 Regular Functions

- Have their own this context
- Can access arguments object
- Can be used as constructors
- Are hoisted

📌 Arrow Functions

- Don’t have their own this, they inherit it from their parent scope
- Don’t have arguments object
- Cannot be used as constructors
- Not hoisted

    - Example:
        ```
        // Regular function
        function sayHello() {
        console.log("Hello from regular function");
        }

        // Arrow function
        const sayHi = () => {
        console.log("Hello from arrow function");
        }

        // `this` behavior
        const person = {
        name: "Alice",
        regularFunc: function () {
            console.log(this.name); // Alice
        },
        arrowFunc: () => {
            console.log(this.name); // undefined
        }
        };

        person.regularFunc();
        person.arrowFunc();


        ```

   - [Back to Top](#javascript-interview-questions)

### Q6. What is a closure? How does it work?
   - A closure is a function that remembers the variables from its outer lexical scope, even after the outer function has completed execution.
   - This means a function can "close over" its surrounding scope and still access those variables later.

   - Example:
        ```
        function outer() {
            let count = 0;
            return function inner() {
                count++;
                console.log("Count:", count);
            };
        }

        const counter = outer();
        counter(); // Count: 1
        counter(); // Count: 2
        ```

- Here, inner() is a closure — it keeps access to count even after outer() has finished.
   - [Back to Top](#javascript-interview-questions)

### Q7. What is the difference between call(), apply(), and bind() in JavaScript?
   - call: Calls a function with a specified this and arguments provided individually.

   - apply: Similar to call, but arguments are provided as an array.

   - bind: Returns a new function, with this set, without invoking immediately.
   - Example:
        ```
        const person = {
        name: "Alice",
        greet: function(city) {
            console.log(`Hello, I'm ${this.name} from ${city}`);
        }
        };

        const anotherPerson = { name: "Bob" };

        person.greet.call(anotherPerson, "Mumbai"); // Hello, I'm Bob from Mumbai
        person.greet.apply(anotherPerson, ["Delhi"]); // Hello, I'm Bob from Delhi

        const boundGreet = person.greet.bind(anotherPerson, "Pune");
        boundGreet(); // Hello, I'm Bob from Pune

        ```
   - [Back to Top](#javascript-interview-questions)

### Q8. What is IIFE (Immediately Invoked Function Expression)?
   - An IIFE is a function that runs as soon as it is defined. It is often used to avoid polluting the global scope or to create private variables.
   - Example:
        ```
        (function () {
            let message = "This runs immediately!";
            console.log(message);
        })(); // Output: This runs immediately!

        ```
   - [Back to Top](#javascript-interview-questions)

### Q9. How to create objects in JavaScript?
   - There are several ways to create objects:
   ✅ Object Literal
   - Example:
     ```
            const person = { name: "Alice", age: 25 };

     ```
   ✅ Constructor Function
   - Example:
     ```
            function Person(name, age) {
                this.name = name;
                this.age = age;
            }
            const user = new Person("Bob", 30);

     ```
   ✅ Object.create()
  - Example:
     ```
            const proto = { greet: function() { console.log("Hello"); } };
            const obj = Object.create(proto);
            obj.greet(); // Hello
     ```
   ✅ Class Syntax (ES6)
   - Example:
     ```
            class Person {
                constructor(name, age) {
                    this.name = name;
                    this.age = age;
                }
            }
            const user = new Person("Charlie", 40);
     ```

   - [Back to Top](#javascript-interview-questions)
### q10. What is the difference between == and ===?
   - == (loose equality) compares two values for equality after converting both values to a common type (type coercion).

   - === (strict equality) checks for both value and type — no type conversion is performed.
   - Example:
     ```
           console.log(2 == "2");   // true  (string "2" is converted to number)
           console.log(2 === "2");  // false (types are different)
           console.log(null == undefined);  // true (special case)
           console.log(null === undefined); // false
     ```
   - [Back to Top](#javascript-interview-questions)

### Q11. What are JavaScript array methods like map(), filter(), reduce(), find(), etc.?
- map creates a new array by applying a function to each element.

- filter returns a new array with elements that pass a test function.

- reduce reduces the array to a single value by accumulating results.

- find returns the first element that satisfies a test function.
- Example:
     ```
        const arr = [1, 2, 3, 4, 5];

        // map
        const doubled = arr.map(x => x * 2); // [2, 4, 6, 8, 10]

        // filter
        const evens = arr.filter(x => x % 2 === 0); // [2, 4]

        // reduce
        const sum = arr.reduce((acc, curr) => acc + curr, 0); // 15

        // find
        const firstEven = arr.find(x => x % 2 === 0); // 2

     ```
- [Back to Top](#javascript-interview-questions)

### Q12. What are callbacks? How do they work?
   - A callback is a function passed as an argument to another function, to be executed after some operation completes (often asynchronously).
   - Example:
     ```
       function fetchData(callback) {
        setTimeout(() => {
            callback("Data loaded");
        }, 1000);
        }

        fetchData(function(result) {
            console.log(result); // "Data loaded" (after 1s)
        });
     ```
   - Callbacks are core to handling asynchronous tasks in JavaScript (timers, I/O, events, etc.).
   - [Back to Top](#javascript-interview-questions)

### Q13. What are Promises? How are they better than callbacks?

- A Promise is an object representing the eventual completion or failure of an asynchronous operation. Promises help you avoid deeply nested callbacks (callback hell) and provide better error handling.

✅ Benefits over callbacks:
- Avoids callback nesting (callback hell)
- Better error handling with .catch()
- Easier to compose multiple async tasks

- [Back to Top](#javascript-interview-questions)

### Q14. What is async/await? How is it better than .then()?
   - async/await is syntactic sugar over Promises in JavaScript. It makes asynchronous code look and behave like synchronous code, improving readability and maintainability.

   - **async:** Declares a function as asynchronous. It returns a promise.
   - **await:** Pauses the execution of an async function until the promise is resolved or rejected.

   - Example:
     ```
       // Using .then()
            fetch("https://api.example.com/data")
            .then(res => res.json())
            .then(data => console.log(data))
            .catch(err => console.error(err));

            // Using async/await
            async function getData() {
            try {
                const res = await fetch("https://api.example.com/data");
                const data = await res.json();
                console.log(data);
            } catch (err) {
                console.error(err);
            }
            }
            getData();
     ```

   ✅ Readability:
- Code written with async/await is often easier to read and write than chaining multiple .then() calls, especially for sequential asynchronous steps.

✅ Error Handling:
- You can use try/catch with async/await just like synchronous code.

- [Back to Top](#javascript-interview-questions)

### Q15. What is the Event Loop in JavaScript?
- The Event Loop is a mechanism in JavaScript that handles asynchronous operations like callbacks, promises, and events.

- JavaScript is single-threaded, but it uses the event loop to manage tasks asynchronously without blocking the main thread.
🌀 Flow:

- Executes code from the call stack.
- Sends async tasks to Web APIs (e.g., setTimeout, fetch).
- Once done, the callback gets queued in task queues (macro/micro).
- The event loop checks the call stack. If it's empty, it moves tasks from the queue to the call stack.

- [Back to Top](#javascript-interview-questions)

### Q16. Explain microtask vs macrotask queue.
   - Microtask queue: Used for tasks like resolved Promises and MutationObservers.
    - Executes after the current script but before any macrotask (like a timer or event).

- Macrotask queue: Used for timers (setTimeout, setInterval), UI events, I/O, etc.

**Execution Order:**
 After every synchronous code block, all microtasks are run, then the first macrotask is processed, then microtasks again, and so on.
- Example:
     ```
       console.log('Start');
        setTimeout(() => console.log('Macrotask'), 0); // macrotask
        Promise.resolve().then(() => console.log('Microtask')); // microtask
        console.log('End');

        // Output:
        // Start
        // End
        // Microtask
        // Macrotask

     ```
- [Back to Top](#javascript-interview-questions)

### Q17. What are setTimeout, setInterval, and clearTimeout?
   - setTimeout(fn, delay): Runs a function once after a delay (in ms).

- setInterval(fn, delay): Runs a function repeatedly with a fixed delay between runs.

- clearTimeout(id) / clearInterval(id): Stops an active scheduled timeout or interval, using the ID returned by setTimeout/setInterval.
   - Example:
     ```
       // setTimeout
        const timeoutId = setTimeout(() => {
        console.log("Runs once after 1 second");
        }, 1000);

        // setInterval
        const intervalId = setInterval(() => {
        console.log("Runs every 2 seconds");
        }, 2000);

        // clearInterval/clearTimeout
        clearTimeout(timeoutId);    // Cancels the scheduled timeout
        clearInterval(intervalId);  // Cancels the setInterval
     ```
- [Back to Top](#javascript-interview-questions)

### Q18. What is callback hell and how do you avoid it?
   - Callback Hell refers to nested callbacks that make code hard to read and maintain.
   - Example:
     ```
      // Callback Hell
        loginUser("user", () => {
        fetchProfile(() => {
            loadDashboard(() => {
            console.log("Dashboard loaded");
            });
        });
        });

     ```
- How to avoid callback hell?
    - Use Promises: Enables chaining and flattens the code.
    - Use async/await: Makes async code look synchronous.
    - Use named functions instead of inline.
   
- [Back to Top](#javascript-interview-questions)

### Q19. What is the DOM? How do you manipulate it with JS?

- The **DOM (Document Object Model)** is a programming interface that represents the structure of an HTML document as a tree of objects.
- JavaScript uses the DOM to dynamically access and manipulate elements, attributes, and styles on a web page.
- Example :
```
// Accessing an element
const heading = document.getElementById("title");

// Changing text content
heading.textContent = "Hello World";

// Changing styles
heading.style.color = "blue";

// Creating and appending elements
const newPara = document.createElement("p");
newPara.textContent = "I was added using JS!";
document.body.appendChild(newPara);
```
- [Back to Top](#javascript-interview-questions)

### Q20. What are event bubbling and event capturing?

- Event Bubbling: Events start from the innermost element and bubble up to its ancestors.

- Event Capturing (Trickling): Events are first captured by the outermost ancestor and propagated inward.

- [Back to Top](#javascript-interview-questions)

### Q21. What are localStorage, sessionStorage, and cookies?
- localStorage : Stores data in the browser with no expiration. Survives page reloads and browser restarts.

- sessionStorage : Stores data for the current session only. Data is cleared when the page or browser is closed.

- Cookies : Small data pieces sent to and from the server with every HTTP request, can have an expiration date, and are accessible from both client and optionally the server.
- Example:
     ```
     // localStorage
      localStorage.setItem("name", "John");
      console.log(localStorage.getItem("name"));
      
      // sessionStorage
      sessionStorage.setItem("temp", "123");
      
      // cookies
      document.cookie = "user=John; expires=Fri, 1 Aug 2025 12:00:00 UTC";
     ```
- [Back to Top](#javascript-interview-questions)

### Q22. What is the `this` keyword and how does it behave in different contexts?

- The this keyword refers to the execution context (the object that owns the current code). Its value depends on how a function is called:

   - Global context: In the browser, this refers to the window object. In strict mode or Node.js global scope, it's undefined.

   - Object method: this refers to the object before the dot.

   - Constructor: Inside a constructor function/class, this refers to the newly created instance.

   - Arrow functions: Do not have their own this; they inherit from the outer (lexical) context.

- [Back to Top](#javascript-interview-questions)

### Q23. What is destructuring in JavaScript (arrays/objects)?

- Destructuring is a syntax for extracting values from arrays or objects into distinct variables, making code cleaner and more concise.

- [Back to Top](#javascript-interview-questions)
  

### Q24. What is middleware in Express.js? How does it work?

- Middleware functions in Express are functions that run during the request-response cycle, between when a request comes in and a response is sent. Middleware has access to req, res, and next and is used for tasks like logging, parsing,  authentication, error handling, etc.

- Global middleware: Applied to all routes using app.use()
- Route middleware: Applied to specific routes or route groups
-  Example:
     ```
    app.use((req, res, next) => {
     console.log(`${req.method} ${req.url}`);
     next(); // Passes control to the next middleware
   });

     ```
- [Back to Top](#javascript-interview-questions)

### Q25. Explain how you implemented JWT-based authentication in your project.

- After user login or signup, the server issues a JWT (signed with a secret).

- The client includes the JWT in the Authorization header for each protected API request.

- On protected endpoints, you verify the JWT. If valid, allow access; if invalid, reject the request.
-  Example:
     ```
    const jwt = require('jsonwebtoken');

        // Generate token after login
        const token = jwt.sign({ userId: user._id }, 'your_jwt_secret', { expiresIn: '1h' });

        // Middleware to protect routes
        function authMiddleware(req, res, next) {
        const token = req.headers.authorization?.split(' ')[1];
        try {
            const decoded = jwt.verify(token, 'your_jwt_secret');
            req.user = decoded;
            next();
        } catch (err) {
            res.status(401).json({ error: 'Invalid token' });
        }
        }

     ```
- [Back to Top](#javascript-interview-questions)

### Q26.Difference between process.nextTick(), setImmediate(), and setTimeout()?
- process.nextTick(): Executes the callback immediately after the current operation, before any I/O or timer events (microtask, highest priority).

- setImmediate(): Executes the callback on the next iteration of the event loop, after any I/O events (macrotask).

- setTimeout(callback, 0): Similar timing to setImmediate but scheduled by the timer phase, may be delayed more.

   - Example:
     ```
        process.nextTick(() => console.log('nextTick'));
        setTimeout(() => console.log('setTimeout'), 0);
        setImmediate(() => console.log('setImmediate'));
        // Output: nextTick, then setTimeout/setImmediate (order may vary)
     ```
- [Back to Top](#javascript-interview-questions)

### Q27. How do you structure a Node.js project?
   - Separate code into logical folders: routes, controllers, models, middlewares, config

- Use environment variables for secrets (with dotenv)

- Each module/file exports what’s needed, keeps code maintainable
   - Example:
     ```
      /project-root
        /routes
            user.js
        /controllers
            userController.js
        /models
            User.js
        /middlewares
            auth.js
        app.js
        .env
        package.json

     ```
   
- [Back to Top](#javascript-interview-questions)

### Q28. How do you handle errors in Express?

- For synchronous errors, use try/catch in route handlers

- For async errors, use next(err) to pass them to error-handling middleware

- Create a centralized error handler that responds to the client and logs errors
- Example :
```
// Centralized error handler
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).json({ message: err.message });
});

```
- [Back to Top](#javascript-interview-questions)

### Q29. How do you define a model using Mongoose?

- Define a schema, then create a model with Mongoose:

- Example :
```
const mongoose = require('mongoose');
const userSchema = new mongoose.Schema({
  username: { type: String, required: true, unique: true },
  password: { type: String, required: true }
});
const User = mongoose.model('User', userSchema);

module.exports = User;


```

- [Back to Top](#javascript-interview-questions)

### Q30. Explain MongoDB aggregation pipeline stages.
- Aggregation pipelines process data through multiple stages.

- $match filters docs, $group aggregates, $lookup joins.

- Example:
     ```
     [
        { $match: { status: 'active' } },
        { $group: { _id: '$department', total: { $sum: 1 } } },
        { $lookup: {
            from: 'departments', 
            localField: '_id', 
            foreignField: 'name', 
            as: 'departmentDetails'
            } 
        }
    ]

     ```
- [Back to Top](#javascript-interview-questions)

### Q31. How do you secure a Node.js backend application?

- Use environment variables, don’t commit secrets
- Validate and sanitize all user input
- Use HTTPS
- Limit rate (express-rate-limit), helmet for HTTP headers
- Keep dependencies updated (npm audit)
- Use proper authentication & authorization
- Sanitize database queries (e.g., use parameterized queries)

- [Back to Top](#javascript-interview-questions)

### Q32. How do you deploy a Node.js app?

- [Back to Top](#javascript-interview-questions)
  

### Q33. What are streams in Node.js?

- Streams let you read, write, or transform data piece by piece, not all at once (efficient for big files, network, video/audio).

- Readable, Writable, Duplex, Transform streams support various types of data flow.
- Used for file I/O, HTTP requests/responses, real-time data.
-  Example:
     ```
    const fs = require('fs');
    const stream = fs.createReadStream('large.txt');
    stream.on('data', chunk => console.log('Received chunk', chunk));
    ```
- [Back to Top](#javascript-interview-questions)

### Q34.How does the Node.js event loop work?

- Node.js uses an event loop with phases:

    1. Timers: Executes setTimeout/setInterval callbacks

    2. Pending Callbacks: I/O callbacks deferred to the next loop

    3. Idle, Prepare: Internal use

    4. Poll: Retrieves new I/O events, executes I/O-related callbacks

    5. Check: Executes setImmediate callbacks

    6. Close Callbacks: Executes close events

 In between, microtasks like process.nextTick and resolved Promises execute..

- [Back to Top](#javascript-interview-questions)

### Q35. How do you test your APIs?

- Manual testing: Use Postman/Insomnia to send requests, check responses.

- Automated testing: Use Jest/Supertest for integration tests.
-  Example:
     ```
    const request = require('supertest');
    const app = require('./app');

    test('GET /users returns 200', async () => {
    await request(app)
        .get('/users')
        .expect(200);
    });

    ```

- [Back to Top](#javascript-interview-questions)


### Q36. How would you scale a Node.js app for high traffic?

- Clustering: Use Node.js cluster module/PM2 to use multiple CPU cores.

- Load balancer: Use Nginx, HAProxy, or a cloud LB to distribute requests across multiple Node.js instances/servers.

- Horizontal scaling: Deploy multiple instances, possibly on Kubernetes/Docker.

- Stateless app: Avoid in-memory sessions; use Redis or database for session store.

- Caching: Use Redis/memcached to cache results and reduce DB load.

- Monitor and auto-scale: Use tools (NewRelic, AWS CloudWatch) to monitor and auto-scale based on traffic
- [Back to Top](#javascript-interview-questions)

