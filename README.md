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
10. **[What is the difference between == and ===?](#q10-what-is-the-difference-between-==-and-===)**
11. **[What are JavaScript array methods like map(), filter(), reduce(), find(), etc.?](#q11-what-are-JavaScript-array-methods-like-map-filter-reduce-find-etc)**
12. **[What are callbacks? How do they work?](#q12-what-are-callbacks-How-do-they-work)**
13. **[What are Promises? How are they better than callbacks?](#q13-what-are-Promises-How-are-they-better-than-callbacks)**
14. **[What is async/await? How is it better than .then()?](#q14-what-is-async-await-how-is-it-better-than-then)**
15. **[What is the Event Loop in JavaScript?](#q15-what-is-the-difference-between-==-and-===)**
16. **[Explain microtask vs macrotask queue.](#q16-what-are-JavaScript-array-methods-like-map-filter-reduce-find-etc)**
17. **[What are setTimeout, setInterval, and clearTimeout?](#q17-what-are-callbacks-How-do-they-work)**
18. **[What is callback hell and how do you avoid it?](#q18-what-are-Promises-How-are-they-better-than-callbacks)**


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

### Q19. What is the difference between SQL and NoSQL databases?
   **SQL Databases:**
- **Schema-based:** SQL databases use a predefined schema, which includes table structures, relationships, and data types.
- **Structured data:** They are ideal for handling structured data that follows a strict format.
- **Relational model:** These databases use tables to represent data, with relationships between tables maintained using foreign keys.
- **ACID compliance:** SQL databases are known for their support of ACID properties (Atomicity, Consistency, Isolation, Durability), which ensures data integrity.
- **Query language:** SQL databases use Structured Query Language (SQL) for querying and manipulating data.
- **Examples:** MySQL, PostgreSQL, Oracle, Microsoft SQL Server.

**NoSQL Databases:**
- **Flexible schema:** NoSQL databases do not require a predefined schema, allowing for flexibility in handling different data types and structures.
- **Unstructured data:** They are suitable for managing unstructured or semi-structured data, such as JSON or XML.
- **Various data models:** NoSQL databases offer different data models, including key-value stores, document stores, column-family stores, and graph databases.
- **Scalability:** NoSQL databases are often more scalable and can handle large amounts of data across distributed systems.
- **BASE properties:** Instead of ACID, NoSQL databases prioritize BASE properties (Basically Available, Soft state, Eventual consistency) for distributed systems.
- **Examples:** MongoDB, Cassandra, CouchDB, Redis, Neo4j.

In summary, SQL databases are suitable for structured data and require a predefined schema, whereas NoSQL databases offer flexibility in handling unstructured data and can be more scalable. The choice between SQL and NoSQL depends on the specific requirements of your application.
   - [Back to Top](#javascript-interview-questions)

### Q20. What are debouncing and throttling in JavaScript?

**Debouncing:**
Debouncing is a technique used to limit the execution of a function call. It delays the execution of the function until after a certain period of time has passed since the last function call. If the function is called again before the delay period is over, the timer resets and the function execution is postponed. This can be useful in scenarios such as handling input events, where you want to wait for the user to stop typing before processing their input.

**Throttling:**
Throttling is a technique used to limit the execution of an event handler function to a specific rate. It ensures that the function is executed at most once in a given period of time, even if the event occurs multiple times. This is beneficial in scenarios such as handling browser resizing or scrolling events, where continuous execution can cause performance issues.

By using debouncing and throttling, you can optimize your code for better performance and avoid unnecessary function calls.

   - [Back to Top](#javascript-interview-questions)

### Q21. Explain `call()`, `apply()`, and `bind()` methods in JavaScript.
   - In JavaScript, `call()`, `apply()`, and `bind()` are methods used to manipulate the context (the value of `this`) in which a function is executed.

   - **`call()` method:**
     - The `call()` method is used to invoke a function with a specific `this` value and arguments provided individually.

   - **`apply()` method:**
     - The `apply()` method is similar to `call()`, but it takes an array of arguments instead of listing them individually.

   - **`bind()` method:**
     - The `bind()` method creates a new function that, when called, has its `this` keyword set to a specific value, and returns a bound function.

   - [Back to Top](#javascript-interview-questions)

### Q22. What is Node.js? What are its advantages and disadvantages?

**Node.js** is an open-source, cross-platform JavaScript runtime environment that allows developers to build server-side and network applications using JavaScript. It is built on the V8 JavaScript engine developed by Google and is known for its event-driven, non-blocking I/O model, which makes it efficient and suitable for scalable applications.

**Advantages of Node.js:**
- **Asynchronous and Event-Driven:** Node.js is based on an asynchronous, non-blocking I/O model that makes it suitable for handling concurrent requests efficiently.
- **Single Language for Both Server and Client:** Since it uses JavaScript, developers can write both server-side and client-side code in the same language, making it easier to maintain and share code.
- **Large Ecosystem:** Node.js has a large ecosystem of packages and libraries available through npm (Node Package Manager), making it easier to find and integrate tools and modules.
- **Fast Performance:** Being built on the V8 engine, Node.js offers high-speed execution and performance.
- **Community Support:** Node.js has a large and active community, providing plenty of support, resources, and continuous improvements.

**Disadvantages of Node.js:**
- **Single-threaded:** While Node.js uses a non-blocking I/O model, it operates as a single-threaded environment, which can lead to performance issues when handling CPU-intensive tasks.
- **Callback Hell:** Due to its asynchronous nature, complex operations may lead to "callback hell," where callbacks are nested deeply, making code harder to read and maintain.
- **Not Suitable for Heavy Computation:** Node.js is not well-suited for heavy computation tasks as it may block the event loop, affecting application performance.
- **Immature Modules:** Some npm modules may not be well-maintained or fully reliable, so careful selection and testing are necessary.

Overall, Node.js is an excellent choice for building scalable and efficient web applications and APIs, particularly when handling many concurrent connections or dealing with real-time data. However, it may not be the best choice for CPU-intensive applications or scenarios requiring heavy computation.

- [Back to Top](#javascript-interview-questions)

### Q23. What are the core modules in Node.js?

**Common Node.js Core Modules:**
- **fs (File System):** The `fs` module allows you to interact with the file system, including reading, writing, and manipulating files and directories.

- **http and https:** These modules enable you to create HTTP and HTTPS servers and make requests. They provide methods to handle requests, responses, headers, and other HTTP features.

- **path:** The `path` module provides utilities for working with file and directory paths, such as joining, normalizing, and resolving paths.

- **url:** The `url` module allows you to parse and format URL strings, making it easier to work with URLs.

- **os (Operating System):** The `os` module provides information and utilities related to the operating system, such as user info, system uptime, and CPU details.

- **events:** The `events` module provides an EventEmitter class that allows you to handle and emit events in your application.

- **util:** The `util` module offers utility functions, including debugging, type-checking, and deprecation features.

- **stream:** The `stream` module provides tools to work with streams, such as readable and writable streams, allowing you to handle data in a continuous flow.

- **net:** The `net` module allows you to create network servers and clients for TCP and IPC (inter-process communication) connections.

- **crypto:** The `crypto` module provides cryptographic functions such as hashing, encryption, and decryption.

- **querystring:** The `querystring` module helps you parse and stringify query strings in URLs.

These are just a few examples of the core modules available in Node.js. There are many more modules that offer different functionalities and features. You can find a full list of core modules in the [Node.js documentation](https://nodejs.org/api/). Core modules are fundamental for building robust and efficient Node.js applications.

- [Back to Top](#javascript-interview-questions)
  

### Q24. How would you secure a Node.js server?

1. **Use HTTPS:** 
    - Always use HTTPS for secure communication between the server and clients. Obtain an SSL/TLS certificate and configure your server to use it.

2. **Input Validation:** 
    - Validate and sanitize user inputs to prevent injection attacks such as SQL injection and cross-site scripting (XSS). Use appropriate libraries or built-in functions for this purpose.

3. **Implement Authentication and Authorization:**
    - Use robust authentication methods such as OAuth, OpenID Connect, or token-based authentication (e.g., JWT) to verify users.
    - Implement proper authorization mechanisms to control access to resources.

4. **Secure Dependencies:**
    - Keep your dependencies up to date and use trustworthy packages from reputable sources. Use tools like `npm audit` to identify vulnerabilities in your dependencies.

5. **Limit Error Information:**
    - Avoid exposing detailed error messages to clients. Instead, log errors server-side and return generic messages to the client.

6. **Use Security Headers:**
    - Configure your server to use security headers like `Content-Security-Policy`, `X-Frame-Options`, `X-XSS-Protection`, and `Strict-Transport-Security`.

7. **Rate Limiting and Throttling:**
    - Implement rate limiting and throttling to prevent abuse and protect against DoS attacks.

8. **Secure Your Environment:**
    - Keep your Node.js server updated with the latest patches and security updates.
    - Use environment variables to store sensitive information such as API keys and database passwords.

9. **Use a Web Application Firewall (WAF):**
    - A WAF can provide an additional layer of security by filtering and monitoring HTTP traffic.

10. **Protect against CSRF:**
    - Use techniques such as CSRF tokens to protect against Cross-Site Request Forgery attacks.

11. **Monitor and Audit:**
    - Continuously monitor your application for security issues and conduct regular security audits.

12. **Secure File and Directory Permissions:**
    - Set appropriate file and directory permissions to restrict access to only the necessary users and processes.

13. **Limit Privilege:** 
    - Run your Node.js server with the least privilege required, avoiding running it as a root user.

Implementing these best practices will help you create a more secure Node.js server and reduce the risk of security vulnerabilities in your application. Let me know if there's anything else I can help you with!
- [Back to Top](#javascript-interview-questions)

### Q25. What are SQL joins?

In SQL, joins are used to combine rows from two or more tables based on a related column between them. This allows you to retrieve data from multiple tables in a single query, making it easier to analyze data and gain insights. Here are some common types of SQL joins:

1. **INNER JOIN:**
    - Retrieves rows that have matching values in both tables based on the specified join condition.
    - Example:
        ```sql
        SELECT columns
        FROM table1
        INNER JOIN table2 ON table1.column = table2.column;
        ```

2. **LEFT JOIN (LEFT OUTER JOIN):**
    - Retrieves all rows from the left table and matching rows from the right table. If there is no match, NULL values are returned for columns from the right table.
    - Example:
        ```sql
        SELECT columns
        FROM table1
        LEFT JOIN table2 ON table1.column = table2.column;
        ```

3. **RIGHT JOIN (RIGHT OUTER JOIN):**
    - Retrieves all rows from the right table and matching rows from the left table. If there is no match, NULL values are returned for columns from the left table.
    - Example:
        ```sql
        SELECT columns
        FROM table1
        RIGHT JOIN table2 ON table1.column = table2.column;
        ```

4. **FULL OUTER JOIN:**
    - Retrieves all rows from both tables, including rows with no matching values. If there is no match, NULL values are returned for columns from the non-matching table.
    - Example:
        ```sql
        SELECT columns
        FROM table1
        FULL OUTER JOIN table2 ON table1.column = table2.column;
        ```

5. **CROSS JOIN:**
    - Produces a Cartesian product of both tables, resulting in all possible combinations of rows from each table.
    - Example:
        ```sql
        SELECT columns
        FROM table1
        CROSS JOIN table2;
        ```

6. **SELF JOIN:**
    - Joins a table to itself, typically for hierarchical or related data within a single table.
    - Example:
        ```sql
        SELECT columns
        FROM table1 AS t1
        JOIN table1 AS t2 ON t1.column = t2.column;
        ```

Using joins, you can create complex queries to retrieve and combine data from multiple tables efficiently. Joins are essential for querying relational databases and are a fundamental aspect of SQL. Let me know if you have any other questions or if there's anything else I can help you with!
- [Back to Top](#javascript-interview-questions)



