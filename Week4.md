# Week 4

### Weekly Aims:
1. Learn to explain the basics of how the HTTP protocol works.
2. Learn to send GET and POST HTTP requests with parameters using a graphical interface.
3. Learn to test-drive Sinatra routes which interact with database-backed classes.
4. Use HTML forms to make the browser send GET and POST requests.
5. Learn to use Discovery debugging for a web application.
6. Learn to deploy an application using Render.

---
### Weekly Objectives:
1. Explain how HTTP requests and responses work at a high level
2. Write integration tests for a web application
3. Implement web routes using a lightweight web framework
4. Follow a debugging process for a web application
5. Deploy a web application using a light cloud service such as Render

---
### Evidence

#### Main Project - Twitter Clone
[Link here](https://github.com/forreya/twitter-clone). Skills practiced & challenges faced:
1. Developed a small Twitter clone that will allow the users to post messages to a public stream.
2. Integrated a database using the `pg` gem and Repository classes
3. Used Sinatra, RSpec, HTML and ERB views to make dynamic webpages such as the **tweets** page or the **log-in** page.
4. Saved all user & tweet information in a database, with keys that allow the system to link tweets to the *original poster*.

#### 1. Understand how the HTTP protocol works.

_HTTP (Hypertext Transfer Protocol) is a client-server communication protocol used for transmitting data over the internet. It's the foundation of data communication for the World Wide Web._

The basics of HTTP communication:

1. A client, such as a web browser, sends an HTTP request to a server.
2. The server receives the request and returns an HTTP response.
3. The client receives the response and displays the data to the user.

HTTP is a stateless protocol, which means that the server does not store information about the client between requests. This makes HTTP scalable and easy to implement, but it also means that additional technologies, such as cookies and sessions, are needed to maintain state between requests.

#### 2. Send GET and POST HTTP requests with parameters using a graphical interface.

_Througout this week, I learned to use `Postman`, which is a client like [curl](https://curl.se/), but with a graphical interface, which is a bit easier to use and configure._

**I worked on this aim through the following project:**

A [music library database web app](https://github.com/forreya/web-applications/tree/main/music_library_database_app), that applies CRUD repository methods, integrating the main App file to the database and displaying the information & messages to the user through HTTP pages. Postman was used to test the web server responses, given a specific HTTP request.

#### 3. Test-drive Sinatra routes which interact with database-backed classes.

**Projects & Challenges:**
1. Test-drove a simple route POST /sort-names which receives a list of names (as a comma-separated string) and return the same list, sorted in alphabetical order. 
- Here is the [video]() of me test driving this Sinatra route 
- Code of the test can be found [here](https://github.com/forreya/web-applications/blob/main/web-app-practice/spec/integration/app_spec.rb) from **line 44 to 51**.
2. Test-drove Sinatra routes which interact with database-backed classes 
- [Spec integration file](https://github.com/forreya/web-applications/blob/main/music_library_database_app/spec/integration/application_spec.rb). These routes were developed for the previously mentioned [music library database web app](https://github.com/forreya/web-applications/tree/main/music_library_database_app).

#### 4. Using HTML forms to make the browser send GET and POST requests.

As previosuly mentioned, this aim was thoroughly practiced in both the [music library database web app](https://github.com/forreya/web-applications/tree/main/music_library_database_app) and the main [twitter clone](https://github.com/forreya/twitter-clone) project.



---
### Daily Journal/Notes

---
### End-of-Week Evaluation
*Were all the weekly aims achieved?*


*Were there any roadblocks/difficulties you had to face?*
