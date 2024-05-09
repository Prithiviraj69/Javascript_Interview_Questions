# JavaScript_Interview_Question

## JavaScript Interview Questions
1. **[What is JavaScript?](#q1-what-is-javascript)**
2. **[Explain the difference between `let`, `const`, and `var` in JavaScript.](#q2-explain-the-difference-between-let-const-and-var-in-javascript)**
3. **[What is the DOM in JavaScript?](#q3-what-is-the-dom-in-javascript)**
4. **[Explain the concept of closures in JavaScript.](#q4-explain-the-concept-of-closures-in-javascript)**
5. **[How does prototypal inheritance differ from classical inheritance?](#q5-how-does-prototypal-inheritance-work-in-javascript)**
6. **[What is asynchronous programming in JavaScript?](#q6-what-is-asynchronous-programming-in-javascript)**
7. **[Explain the difference between `==` and `===` in JavaScript.](#q7-explain-the-difference-between-and-in-javascript)**
8. **[What are Arrow functions in JavaScript?](#q8-what-are-arrow-functions-in-javascript)**
9. **[What is the significance of the `this` keyword in JavaScript?](#q9-what-is-the-significance-of-the-this-keyword-in-javascript)**
10. **[Explain the callback, promises, async/await in JavaScript.](#q10-explain-the-callback-promises-async-await-in-javascript)**
11. **[What is the purpose of the `setTimeout` function in JavaScript?](#q11-what-is-the-purpose-of-the-settimeout-function-in-javascript)**
12. **[How can you handle errors in JavaScript?](#q12-how-can-you-handle-errors-in-javascript)**
13. **[Explain the concept of Promises in JavaScript.](#q13-explain-the-concept-of-promises-in-javascript)**
14. **[What is the difference between `null` and `undefined` in JavaScript?](#q14-what-is-the-difference-between-null-and-undefined-in-javascript)**
15. **[How can you achieve inheritance in JavaScript?](#q15-how-can-you-achieve-inheritance-in-javascript)**
16. **[Explain the concept of hoisting in JavaScript.](#q16-explain-the-concept-of-hoisting-in-javascript)**
17. **[What is the role of the `document.write()` method?](#q17-what-is-the-role-of-the-documentwrite-method)**
18. **[How does the `localStorage` differ from `sessionStorage` in JavaScript?](#q18-how-does-the-localstorage-differ-from-sessionstorage-in-javascript)**
19. **[What is the purpose of the `JSON.stringify()` method?](#q19-what-is-the-purpose-of-the-jsonstringify-method)**
20. **[Explain the concept of the same-origin policy in JavaScript.](#q20-explain-the-concept-of-the-same-origin-policy-in-javascript)**
21. **[Explain `call()`, `apply()`, and `bind()` methods in JavaScript.](#q21-explain-call-apply-and-bind-methods-in-javascript)**

# Questions and Answers

### Q1. What is JavaScript?
   - JavaScript is a versatile programming language primarily known for its role in web development.
   - It is a high-level, interpreted scripting language that allows developers to add dynamic and interactive elements to websites.
   - [Back to Top](#javascript-interview-questions)

### Q2. Explain the difference between `let`, `const`, and `var` in JavaScript. 
   - **`let`:** It allows the declaration of block-scoped variables. The variable can be reassigned within the same block.
   - **`const`:** It also declares block-scoped variables but is used for constants that cannot be reassigned.
   - **`var`:** It declares a variable globally or locally to the entire function, regardless of block scope. It can be reassigned.
   - [Back to Top](#javascript-interview-questions)

### Q3. What is the DOM in JavaScript?
   - The DOM (Document Object Model) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content dynamically.
   - The DOM represents the document as a tree of nodes, where each node corresponds to part of the page (e.g., elements, attributes, text).
   - [Back to Top](#javascript-interview-questions)

### Q4. Explain the concept of closures in JavaScript.
   - A closure is a function along with its lexical environment (the environment in which the function was declared). It allows a function to access variables from its outer function even after that function has finished execution.
   - Closures are useful for maintaining state, creating private variables, and implementing data encapsulation.
   - [Back to Top](#javascript-interview-questions)

### Q5. How does prototypal inheritance work in JavaScript?
   - JavaScript uses prototypal inheritance, where objects can inherit properties and methods from other objects.
   - Each object has an internal property called `[[Prototype]]`, and when a property is not found in an object, JavaScript looks for it in the object's prototype, creating a chain.
   - In classical inheritance, classes are immutable, may or may not support multiple inheritance, and may contain interfaces, final classes, and abstract classes. In contrast, prototypes are much more flexible in the sense that they may be mutable or immutable. The object
may inherit from multiple prototypes, and only contains objects.
   - [Back to Top](#javascript-interview-questions)

### Q6. What is asynchronous programming in JavaScript?
   - Asynchronous programming in JavaScript allows code to run without waiting for long-running tasks to finish.
   - It is achieved using callbacks, promises, and async/await. Callbacks are functions passed as arguments to be executed later.
   - [Back to Top](#javascript-interview-questions)

### Q7. Explain the difference between `==` and `===` in JavaScript. 
   - **`==`:** It performs type coercion, allowing different types to be considered equal. For example, `"5" == 5` is true.
   - **`===`:** It strictly checks for equality without type coercion. `"5" === 5` is false.
   - [Back to Top](#javascript-interview-questions)

### Q8. What are Arrow functions in JavaScript?
   - Arrow function {()=>} is concise way of writing JavaScript functions in shorter way. They make our code more structured and readable.
   - Arrow functions are anonymous functions i.e. functions without a name but they are often assigned to any variable. They are also called Lambda Functions.
   - [Back to Top](#javascript-interview-questions)

### Q9. What is the significance of the `this` keyword in JavaScript?
   - The `this` keyword refers to the object it belongs to. In a function, `this` refers to the global object (window in a browser).
   - In methods, `this` refers to the object that owns the method. Arrow functions don't have their own `this` but inherit it from the enclosing scope.
   - [Back to Top](#javascript-interview-questions)

### Q10. Explain the callback, promises, async/await in JavaScript.
   - **Callback** :
   - When you nest a function inside another function as an argument, that's called a callback.
   - When doing a complex task, we break that task down into smaller steps. To help us establish a relationship between these steps according to time (optional) and order, we use callbacks.
   - **Promises** :
   - Promises were invented to solve the problem of callback hell and to better handle our tasks.
   - promise has three states:
     1. Pending: This is the initial stage. Nothing happens here. Think of it like this, your customer is taking their time giving you an order. But they haven't ordered anything yet.
     2. Resolved: This means that your customer has received their food and is happy.
     3. Rejected: This means that your customer didn't receive their order and left the restaurant.
   - **Aysnc** :
   - The Async function simply allows us to write promises-based code as if it were synchronous and it checks that we are not breaking the execution thread.
   - Async functions will always return a value. It makes sure that a promise is returned and if it is not returned then JavaScript automatically wraps it in a promise which is resolved with its value.
   - **Await** :
   - Await is used to wait for the promise. It could be used within the async block only.It makes the code wait until the promise returns a result. 

   - [Back to Top](#javascript-interview-questions)

### Q11. What is the purpose of the `setTimeout` function in JavaScript?
   - The `setTimeout` function is used to delay the execution of a function or a piece of code for a specified amount of time (in milliseconds).
   - It's commonly used to create delays in animations, execute code after a certain interval, or simulate asynchronous behavior.
   - [Back to Top](#javascript-interview-questions)

### Q12. How can you handle errors in JavaScript?
   - Errors in JavaScript can be handled using `try`, `catch`, `finally` blocks.
   - The `try` block contains the code to be executed, and if an error occurs, it jumps to the `catch` block.
   - The `finally` block is executed regardless of whether an error occurred or not.
   - [Back to Top](#javascript-interview-questions)

### Q13. Explain the concept of Promises in JavaScript.
   - Promises are objects representing the eventual completion or failure of an asynchronous operation.
   - They have states: `pending`, `fulfilled`, and `rejected`. Promises simplify asynchronous code and make it more readable.
   - [Back to Top](#javascript-interview-questions)

### Q14. What is the difference between `null` and `undefined` in JavaScript?
   - **`null`:** It represents the intentional absence of any object value. It must be assigned.
   - **`undefined`:** It represents an uninitialized or unassigned value. Variables that are not assigned a value are `undefined`.
   - [Back to Top](#javascript-interview-questions)

### Q15. How can you achieve inheritance in JavaScript?
   - Inheritance in JavaScript is achieved through prototype chaining. Objects can inherit properties and methods from other objects by setting their prototype.
   - The `Object.create()` method is commonly used to create an object with a specific prototype.
   - [Back to Top](#javascript-interview-questions)

### Q16. Explain the concept of hoisting in JavaScript.
   - Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase.
   - Variables declared with `var` are hoisted and initialized with `undefined`. Function declarations are fully hoisted.
   - [Back to Top](#javascript-interview-questions)

### Q17. What is the role of the `document.write()` method?
   - The `document.write()` method is used to write HTML expressions or JavaScript code to a document.
   - It is typically used for testing and dynamically generating content, but it can cause issues with the document structure if used after the page has loaded.
   - [Back to Top](#javascript-interview-questions)

### Q18. How does the `localStorage` differ from `sessionStorage` in JavaScript?
   - **`localStorage`:** Data stored in `localStorage` persists even after the browser is closed. It has no expiration time.
   - **`sessionStorage`:** Data stored in `sessionStorage` is limited to the duration of the page session. It is cleared when the page session ends.
   - [Back to Top](#javascript-interview-questions)

### Q19. What is the purpose of the `JSON.stringify()` method?
   - The `JSON.stringify()` method converts a JavaScript object or value to a JSON string.
   - It is commonly used to send data to a server or to store data in a format that can be easily transmitted between different platforms.
   - [Back to Top](#javascript-interview-questions)

### Q20. Explain the concept of the same-origin policy in JavaScript.
   - The same-origin policy is a security measure that restricts a web page from making requests to a different domain than the one that served the web page.
   - It prevents malicious scripts from making requests on behalf of the user without their consent.
   - [Back to Top](#javascript-interview-questions)

### Q21. Explain `call()`, `apply()`, and `bind()` methods in JavaScript.
   - In JavaScript, `call()`, `apply()`, and `bind()` are methods used to manipulate the context (the value of `this`) in which a function is executed.

   - **`call()` method:**
     - The `call()` method is used to invoke a function with a specific `this` value and arguments provided individually.
     - Example:
       ```javascript
       function greet(name) {
           console.log(`Hello, ${name}!`);
       }

       greet.call(null, 'John');
       ```

   - **`apply()` method:**
     - The `apply()` method is similar to `call()`, but it takes an array of arguments instead of listing them individually.
     - Example:
       ```javascript
       function greet(name) {
           console.log(`Hello, ${name}!`);
       }

       greet.apply(null, ['John']);
       ```

   - **`bind()` method:**
     - The `bind()` method creates a new function that, when called, has its `this` keyword set to a specific value, and returns a bound function.
     - Example:
       ```javascript
       function greet(name) {
           console.log(`Hello, ${name}!`);
       }

       const boundGreet = greet.bind(null, 'John');
       boundGreet();
       ```

   - [Back to Top](#javascript-interview-questions)


