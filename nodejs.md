1. What is the event loop in Node.js, and how does it work?
Answer: The event loop is a core part of Node.js's asynchronous architecture. It allows Node.js to handle non-blocking I/O operations by offloading operations to the system kernel whenever possible. The event loop continuously checks the call stack and the callback queue, executing tasks as they become available.

2. Explain the difference between process.nextTick(), setImmediate(), and setTimeout().
Answer:

process.nextTick() schedules a callback to be invoked in the same phase of the event loop, before any I/O events.

setImmediate() schedules a callback to execute after the current poll phase completes.

setTimeout() schedules a callback after a minimum delay, but the actual execution depends on the event loop state.

3. How do you handle uncaught exceptions in Node.js?
Answer: Use the process.on('uncaughtException', callback) event to catch exceptions not handled elsewhere. However, it is generally better to handle errors using try-catch blocks and error events, as relying on this event can leave the process in an unstable state.

4. What is middleware in Express.js?
Answer: Middleware are functions that execute during the lifecycle of a request to the server. They can modify the request and response objects, end the request-response cycle, or call the next middleware in the stack.

5. How does Node.js handle child processes?
Answer: Node.js provides the child_process module to spawn child processes using functions like spawn, exec, and fork. These allow you to run shell commands, scripts, or other Node.js instances.

Advanced Topics
6. How do you manage authentication in a Node.js application?
Answer: Common approaches include using JWT (JSON Web Tokens) for stateless authentication, sessions with cookies, and integrating with Passport.js for various strategies. Token-based authentication is popular for APIs.

7. What is the difference between synchronous and asynchronous methods in Node.js?
Answer: Synchronous methods block the event loop until completion, preventing other code from executing. Asynchronous methods use callbacks, promises, or async/await to allow other operations to proceed while waiting for a task to finish.

8. How do you secure a Node.js application?
Answer:

Validate and sanitize user input.

Use HTTPS.

Implement proper authentication and authorization.

Avoid using deprecated or vulnerable packages.

Set HTTP security headers.

9. How do you connect Node.js to a MongoDB database?
Answer: Use the Mongoose library to define schemas and interact with MongoDB. Mongoose provides a schema-based solution to model application data and supports validation, middleware, and more.

10. How do you optimize the performance of a Node.js application?
Answer:
Use clustering to take advantage of multi-core CPUs.
Implement caching strategies.
Minimize synchronous code.
Monitor and profile the application to identify bottlenecks.

11. What is the difference between Laravel and Node.js in terms of scalability and real-time applications?
Answer: Node.js is event-driven and non-blocking, making it more scalable and better suited for real-time applications (e.g., chat, live updates). Laravel is synchronous and better for traditional web apps with complex features

**Intermediate & Advanced Questions**

1. What is an EventEmitter in Node.js?
Answer: The EventEmitter class is part of the events module and allows objects to emit named events. Listeners (callback functions) can be attached to these events and will be called synchronously whenever the event is emitted. This pattern is fundamental to Node.js's event-driven architecture.

2. Explain the concept of streams in Node.js.
Answer: Streams are objects that enable reading or writing data in chunks, rather than loading the entire data into memory. Node.js provides four types of streams: Readable, Writable, Duplex, and Transform. Streams are used for efficient handling of large files, network communications, and more.

3. What is the Buffer class in Node.js? Why is it needed?
Answer: The Buffer class provides a way to handle binary data directly in memory. Buffers are used because JavaScript strings only handle UTF-16 encoded data, but Node.js often needs to process binary streams (e.g., files, network packets). Buffers allow manipulation of raw binary data.

4. What is REPL in Node.js?
Answer: REPL stands for Read-Eval-Print Loop. It is an interactive shell that processes Node.js expressions, evaluates them, and prints the result. REPL is useful for experimenting, debugging, and testing snippets of code quickly.

5. What is the difference between fork() and spawn() methods in Node.js?
Answer: Both are used to create child processes. spawn() launches a new process with a given command, while fork() is a special case of spawn() that creates a new Node.js process and enables communication between parent and child via IPC (Inter-Process Communication) channels.

6. How do you handle CORS (Cross-Origin Resource Sharing) in Express.js?
Answer: CORS can be managed using the cors middleware package in Express.js. It allows you to specify which origins are permitted to access your resources, as well as allowed HTTP methods and headers.

7. What are the types of streams in Node.js, and when would you use each?
Answer:

Readable: For reading data (e.g., file streams).

Writable: For writing data (e.g., writing to a file).

Duplex: Both readable and writable (e.g., TCP sockets).

Transform: Modify or transform data as it is read or written (e.g., zlib compression).

8. How do you handle memory leaks in a Node.js application?
Answer: Identify leaks using profiling tools like Node.js built-in inspector, Chrome DevTools, or external tools like heapdump. Common strategies include monitoring heap usage, removing unused event listeners, and ensuring timers and callbacks are cleared when no longer needed.

9. What is the difference between callbacks and Promises in Node.js?
Answer: Callbacks are functions passed as arguments to handle asynchronous results, but can lead to "callback hell" if nested deeply. Promises provide a cleaner, more manageable way to handle async operations, supporting chaining and error handling via .then() and .catch().

10. How do you ensure scalability in a Node.js application?
Answer: Use clustering to take advantage of multi-core systems, implement load balancing (e.g., with Nginx), design stateless APIs for horizontal scaling, optimize code and database queries, and use caching strategies (like Redis).

11. How do you manage dependencies and security in Node.js?
Answer: Regularly audit dependencies using tools like npm audit or snyk, specify precise version ranges in package.json, and use package-lock.json to lock down versions. Keep dependencies updated and remove unused packages.

12. How would you handle file uploads in Node.js?
Answer: Use middleware like multer in Express.js to handle multipart/form-data, which is used for file uploads. Configure storage, file size limits, and validation as needed.

13. What is piping in Node.js?
Answer: Piping is a mechanism to connect the output of one stream to the input of another, allowing data to flow through multiple processing steps (e.g., reading a file, compressing it, and writing to disk) efficiently.

14. What is an error-first callback?
Answer: An error-first callback is a pattern where the first argument of the callback is reserved for an error object (if any), and subsequent arguments are for successful results. This allows for consistent error handling in async code.

15. How can you avoid callback hell?
Answer: Use Promises or async/await to flatten nested callbacks, modularize code into smaller functions, and leverage control flow libraries like async

16. How do you connect Node.js to a database like MongoDB?
Answer: Use libraries like Mongoose to define schemas and models, then connect to MongoDB using mongoose.connect(). Mongoose provides validation, middleware, and schema-based data modeling.

