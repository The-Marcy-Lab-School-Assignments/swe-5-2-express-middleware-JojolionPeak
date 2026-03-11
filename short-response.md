# Short Response Questions

Answer each question below in your own words. Aim for 3–5 sentences per answer. Be specific — use the exact terms and concepts from the lesson.

Your responses will each be evaluated out of 6 points. You can earn 3 points for writing quality and 3 points for the accuracy and precision of the technical content per question.

---

## Question 1: Express vs `node:http`

Express is described as a framework that "wraps" `node:http`. What does that mean? Compare how you would handle a `GET /api/users` request in `node:http` versus in Express. What does Express do for you automatically that you had to write manually with `node:http`?

This means that Express is built upon `node:http`, and instead of replacing the functionality of node, it simply builds upon node's frameworks. Before, just using `node:http`, we had to **manually** set headers and write **if/else statements**, but with Express, we get more **properties and methods** with the request and response objects, making the server-side code much cleaner and quicker.

---

## Question 2: Endpoints, Controllers, and Middleware

What are **controllers** and **middleware** in Express? What are each responsible for and how do they work together to handle incoming requests?

**Controllers** are blocks of code that dictate _what the server should do based on the request being made_ to the server. **Middleware** are blocks of code that pauses the response from a request and can perform many actions, like _logging the requests being made_, before passing on the data from the request to either a _controller or another middleware_. They serve to guide the server on what the appropriate response is, and ensures the server is **working as intended**.

---

## Question 3: Query Strings and Route Parameters

How are **query strings** and **route parameters** similar? How are they different? In your answer, provide an example of when you would use each.

**Query strings** and **route parameters** both allow the user to get a response based on \*specific data that is inputted into the **URL\***, however, query strings are useful for _filtering or modifying_ the data they request, while route parameters are more useful for _getting a single resource's data_. Suppose we had a database full of information about books; I would use **query strings** for filtering books based on the inputted genre, and I would use **route parameters** for trying to find all the data on a single book.

---

## Question 4: Same-Origin Requests

For API fetch calls from a client-side application, explain the difference between fetching from endpoints with relative paths like `/api/quotes` and fetching from endpoints with a full URL like `https://dog.ceo/api/breeds/image/random`. Why do we not send a fetch using a url like `http://localhost:8080/api/quotes`?

We don't need to use the **absolute path** in a URL when the _origins of the client side code in the server are the same_. When the origins for the frontend code and the server code are the same device, the `https://localhost:8080` is assumed and doesn't need to be explicitly stated. However, when the client is requesting information from a server with a **different origin**, the prefix is necessary in the URL.
