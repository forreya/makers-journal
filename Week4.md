# Week 4

### Weekly Aims:
1. Learn to explain the basics of how the HTTP protocol works. **✓**
2. Learn to send GET and POST HTTP requests with parameters using a graphical interface. **✓**
3. Learn to test-drive Sinatra routes which interact with database-backed classes. **✓**
4. Use HTML forms to make the browser send GET and POST requests. **✓**
5. Learn to use Discovery debugging for a web application. **✓**
6. Learn to deploy an application using Render. **✘**

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
- Here is the [video](https://github.com/forreya/makers-portfolio/blob/main/videos/test-driving-web-route.mp4) of me test driving this Sinatra route 
- Code of the test can be found [here](https://github.com/forreya/web-applications/blob/main/web-app-practice/spec/integration/app_spec.rb) from **line 44 to 51**.
2. Test-drove Sinatra routes which interact with database-backed classes 
- [Spec integration file](https://github.com/forreya/web-applications/blob/main/music_library_database_app/spec/integration/application_spec.rb). These routes were developed for the previously mentioned [music library database web app](https://github.com/forreya/web-applications/tree/main/music_library_database_app).

#### 4. Using HTML forms to make the browser send GET and POST requests.

As previosuly mentioned, this aim was thoroughly practiced in both the [music library database web app](https://github.com/forreya/web-applications/tree/main/music_library_database_app) and the main [twitter clone](https://github.com/forreya/twitter-clone) project.

#### 5. Using Discovery debugging for web applications.

_What discovery debugging is:_

Discovery debugging is a software debugging technique that involves exploring a system or application to gain a deeper understanding of its behavior and identify the root cause of a problem. The goal of discovery debugging is to gain a better understanding of how the system works, as opposed to simply fixing a specific issue.

I used discovery debugging to debug and fix the errors in all the programs listed in [this repository](https://github.com/forreya/web-applications/tree/main/projects_to_debug).

**It took a really long time to find the problems in the code sometimes which really frustrated me at times but eventually I realized that following this methology helped improve my debugguging efficiency:**
1. Gathering information: I started by collecting information about the system, including logs, error messages, and any relevant documentation. This information helped me get a better understanding of the problem and was vital in identifying potential causes.

2. Studying the code: Looking at the section of the code that is relevant to the problem, and trying to understand how it works helped me identify any potential issues and determine what parts of the code might be contributing to the problem.

3. Experimenting: Conducting experiments to see how different parts of the system were interacting and affecting each other by changing parts of the code, turning features on and off, and seeing how the system behaved in different scenarios.

4. Collaborating: Working with other members of my cohort to gain a more comprehensive understanding of the system sometimes helped me identify problems that I would not have thought of on my own.

5. Repeating steps as necessary.

---
### Daily Journal/Notes

#### Random Notes:
I have a prior experience with HTTP and the `curl` command-line tool, which means that the concept is not new to me. However, despite my familiarity with these technologies, I was still able to learn many new programming methods and techniques that I had not encountered previously, demonstrating that there is always room for growth and learning, even in areas where one already has some experience. The ability to continuously learn and expand one's knowledge is a valuable skill in the field of programming, something I will continually strive to do.

#### Day 3:
Today I finished all the challenges and exercises from the [web-applications](https://github.com/makersacademy/web-applications) module, so I begun working on my `twitter clone` project.

While working on my `twitter clone` project, I encountered a useful data type in PostgreSQL, called **timestamptz**. Some info:
- `timestamptz` represents a timestamp with time zone. 
- The data type stores a date and time value, along with the information about the time zone offset. This allows for proper handling of time-sensitive data that needs to take into account the geographical location of the user.
- The time zone information is stored as an offset from the UTC time, which is the reference time for all time zones. The offset is stored as the number of seconds ahead or behind the UTC time.

For example, the following statement creates a table with a column of type `timestamptz`:

```sql
CREATE TABLE events (
  id serial primary key,
  name text,
  event_time timestamptz
);
```

To insert a value into a `timestamptz` column, the 'timestamptz' value should be in the format of YYYY-MM-DD HH:MM:SS+TZ, where TZ is the time zone offset from UTC. For example:

```sql
INSERT INTO events (name, event_time)
VALUES ('Event 1', '2022-06-01 12:30:00 PST');
```

When you retrieve data from a `timestamptz` column, PostgreSQL will automatically adjust the timestamp value to the time zone of the client, so that the value will be displayed correctly for the user.

---
### End-of-Week Evaluation
*Were all the weekly aims achieved?*

The final aim was not achieved as I haven't finished my MVP of the `twitter clone` project yet. However, once I do complete all the features and code I intend to deploy the application so it runs remotely. 

*Were there any roadblocks/difficulties you had to face?*

Yes. Firstly, learning to build solid security within my apps was tough for me as I had a limited understanding of these security threats and how to protect my applications against them. I also struggled at first with ERB as its syntax was difficult to understand- from learning to embed Ruby code within HTML to learning how to pass variables and data between the controller and the view. These initial roadblocks eventually became learning curves as I slowly got familiar with concepts and programming ideas.