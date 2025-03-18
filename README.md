## Commit 1 Reflection
The handle_connection method processes incoming HTTP requests from a browser. The method reads the request line by line using BufReader, collecting and printing the request details to understand how browsers communicate with a server. This helped me see the raw HTTP request structure, making it easier to handle different types of requests in future improvements.

## Commit 2 Reflection
In this milestone, the handle_connection method is modified to return an HTML response, allowing the browser to render a simple webpage. I learned how to read an HTML file in Rust and format an HTTP response properly, including setting the status line and content length. This helped me understand how web servers send responses and the importance of properly structuring HTTP headers.
![Commit 2 screen capture](/assets/images/commit2.png)

