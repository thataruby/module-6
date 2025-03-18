## Commit 1 Reflection
The handle_connection method processes incoming HTTP requests from a browser. The method reads the request line by line using BufReader, collecting and printing the request details to understand how browsers communicate with a server. This helped me see the raw HTTP request structure, making it easier to handle different types of requests in future improvements.

## Commit 2 Reflection
In this milestone, the handle_connection method is modified to return an HTML response, allowing the browser to render a simple webpage. I learned how to read an HTML file in Rust and format an HTTP response properly, including setting the status line and content length. This helped me understand how web servers send responses and the importance of properly structuring HTTP headers.
![Commit 2 screen capture](/assets/images/commit2.png)

## Commit 3 Reflection
In this milestone, I learned how to handle different types of HTTP requests by checking the request line and returning either the requested HTML page or a 404 error. The refactoring step was important because it reduced repetition in the code by separating the response status and filename logic, making it easier to update or extend in the future.
![Commit 3 screen capture](/assets/images/commit3.png)

## Commit 4 Reflection
This milestone showed how a single-threaded server struggles when handling multiple requests, especially when one request takes a long time to process. Since the server processes requests sequentially, any slow response (like the /sleep request) blocks other incoming requests, causing delays for all users.

## Commit 5 Reflection
In this milestone, the server was improved by implementing ThreadPool, which now allows it to handle multiple requests concurrently instead of processing them one by one. This prevents slow requests (like /sleep) from blocking the entire server, making it more efficient. The ThreadPool has a set number of worker threads that take turns handling requests, making the server run more smoothly even under hevaly load.