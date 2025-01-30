
# **First Module**

# Introduction to Web Development: Basics of HTTP/HTTPS

## What is Web Development?

Web development refers to the process of creating and maintaining websites and web applications. It involves various aspects such as:

- **Front-end development** (User Interface and Experience)
- **Back-end development** (Server-side logic and databases)
- **Full-stack development** (Both front-end and back-end)

One of the key components of web development is **communication between clients (browsers) and servers**, which is facilitated by the HTTP/HTTPS protocols.

---

## What is HTTP?

### **Definition:**

**HyperText Transfer Protocol (HTTP)** is a protocol used for transferring hypertext (HTML documents) between web clients and servers. It is the foundation of data communication on the World Wide Web.

### **How HTTP Works:**

1. A user enters a URL in their browser.
2. The browser sends an **HTTP request** to the web server.
3. The web server processes the request and sends back an **HTTP response**.
4. The browser receives the response and displays the web page.

### **Structure of an HTTP Request:**

An HTTP request consists of the following parts:

1. **Request Line** - Contains the request method (GET, POST, etc.), URL, and HTTP version.
2. **Headers** - Contains metadata such as browser type, accepted content type, etc.
3. **Body** (Optional) - Used for sending data in POST requests.

#### Example of an HTTP Request:

```
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html
```

### **Structure of an HTTP Response:**

An HTTP response consists of:

1. **Status Line** - Contains the HTTP version, status code, and status message.
2. **Headers** - Information about the server, content type, date, etc.
3. **Body** - Contains the actual requested resource (HTML, JSON, etc.).

#### Example of an HTTP Response:

```
HTTP/1.1 200 OK
Date: Mon, 30 Jan 2025 12:00:00 GMT
Server: Apache/2.4.41
Content-Type: text/html

<html>
<head><title>Example Page</title></head>
<body><h1>Welcome to Example.com</h1></body>
</html>
```

### **Common HTTP Methods:**

|Method|Description|
|---|---|
|GET|Retrieves data from the server|
|POST|Sends data to the server|
|PUT|Updates a resource on the server|
|DELETE|Deletes a resource from the server|

### **Common HTTP Status Codes:**

|Code|Meaning|
|---|---|
|200|OK (Success)|
|301|Moved Permanently (Redirect)|
|404|Not Found|
|500|Internal Server Error|

---

## What is HTTPS?

### **Definition:**

**HyperText Transfer Protocol Secure (HTTPS)** is a secure version of HTTP that encrypts data exchanged between the client and server using **SSL/TLS encryption**.

### **Key Differences Between HTTP and HTTPS:**

|Feature|HTTP|HTTPS|
|---|---|---|
|Security|Unencrypted, vulnerable to attacks|Encrypted, secure data transfer|
|Protocol|Uses TCP|Uses SSL/TLS over TCP|
|URL Prefix|`http://`|`https://`|
|Port|80|443|

### **How HTTPS Works:**

1. The browser requests a secure connection from the server.
2. The server responds with an **SSL certificate**.
3. The browser verifies the certificate with a Certificate Authority (CA).
4. A secure encrypted connection is established using **TLS encryption**.
5. Data transfer begins securely between the client and server.

### **Example of an HTTPS URL:**

```
https://www.securewebsite.com
```

### **Benefits of HTTPS:**

- **Data Encryption:** Prevents eavesdropping and data theft.
- **Authentication:** Ensures the website is legitimate.
- **Data Integrity:** Protects against data tampering.
- **SEO Ranking Boost:** Google prioritizes HTTPS websites.

---

## **Diagram: HTTP vs HTTPS Communication**

```plaintext
            HTTP Communication                 HTTPS Communication

User -----> Request (Plain Text) -----> Server  User -----> Encrypted Request -----> Server
      <----- Response (Plain Text) <-----        <----- Encrypted Response <-----
```

---

## **Conclusion:**

- **HTTP is the foundation of web communication** but lacks security.
- **HTTPS is the secure version of HTTP**, using SSL/TLS encryption to protect data.
- Modern web development **should always prefer HTTPS** for better security and trust.

### **Example of HTTP vs HTTPS in Real Life:**

|Website|URL|
|---|---|
|Insecure Site|`http://example.com`|
|Secure Site|`https://example.com`|

Web development relies on understanding how HTTP/HTTPS work to create secure and efficient web applications. Transitioning to HTTPS is crucial for security and trustworthiness in the modern web.

---

## **Further Reading:**

- HTTP/HTTPS protocols: [Mozilla Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- SSL/TLS Encryption: [SSL.com](https://www.ssl.com/)

---

# Overview of Web Servers

## **What is a Web Server?**

A **web server** is a software and hardware system that processes requests over the internet or an intranet and delivers web pages or other web content to users. It serves web pages using the **HyperText Transfer Protocol (HTTP) or HyperText Transfer Protocol Secure (HTTPS).**

### **Functions of a Web Server:**

1. **Handling Client Requests:** Receives and processes requests from web browsers.
2. **Serving Web Pages:** Delivers HTML documents, images, videos, and other resources.
3. **Executing Scripts:** Runs server-side scripts like PHP, Python, or Node.js.
4. **Security Management:** Uses SSL/TLS for encrypted connections.
5. **Logging & Monitoring:** Tracks server activity and errors.

---

## **Types of Web Servers**

### **1. Static Web Server**

A static web server consists of a **computer with an HTTP server (software)** that serves **static content** like HTML, CSS, and images.

- Example: **NGINX serving static files**
- Pros: Fast, easy to set up
- Cons: Cannot process dynamic content

### **2. Dynamic Web Server**

A dynamic web server includes additional software like application servers and databases that generate content on-the-fly.

- Example: **Apache with PHP & MySQL**
- Pros: Can handle dynamic content like user logins, data retrieval
- Cons: Requires more processing power

---

## **Popular Web Servers**

|Server Name|Developed By|Usage|
|---|---|---|
|Apache HTTP Server|Apache Software Foundation|Most widely used open-source server|
|Nginx|Igor Sysoev|High-performance, lightweight server|
|Microsoft IIS|Microsoft|Windows-based web server|
|LiteSpeed|LiteSpeed Technologies|Optimized for speed and security|
|Caddy|Matt Holt|Secure, automatic HTTPS|

---

## **How a Web Server Works**

1. **Client Request:** A user types a URL in a browser (e.g., `https://example.com`).
2. **DNS Resolution:** The domain name translates into an IP address.
3. **Connection Establishment:** The browser connects to the web server via HTTP/HTTPS.
4. **Request Handling:** The server processes the request.
5. **Response Sending:** The server sends an HTML page or other content.
6. **Rendering in Browser:** The browser displays the webpage.

---

## **Key Components of a Web Server**

### **1. Hardware**

- **Physical server**: A powerful computer that stores website files.
- **Network connection**: Enables communication over the internet.
- **Storage**: Hard drives or SSDs for storing web content.

### **2. Software**

- **HTTP Server**: Software like Apache, Nginx.
- **Database Server**: MySQL, PostgreSQL, MongoDB.
- **Application Server**: PHP, Python, Node.js.

---

## **Web Server Architectures**

### **1. Single-Threaded Web Server**

- Handles one request at a time.
- Example: Basic Python `http.server` module.
- Suitable for small applications.

### **2. Multi-Threaded Web Server**

- Handles multiple requests simultaneously.
- Example: Apache HTTP Server with multi-threading.
- Suitable for medium to large applications.

### **3. Event-Driven Web Server**

- Uses non-blocking architecture to handle multiple requests efficiently.
- Example: Nginx, Node.js.
- Suitable for high-performance applications.

---

## **Security Features of Web Servers**

1. **SSL/TLS Encryption:** Uses HTTPS for secure communication.
2. **Firewalls:** Protect against unauthorized access.
3. **Access Control:** Restricts certain IPs or users.
4. **DDoS Protection:** Prevents denial-of-service attacks.
5. **Logging & Monitoring:** Helps detect security threats.

---

## **Web Server Performance Optimization**

- **Caching:** Stores frequently requested pages in memory.
- **Load Balancing:** Distributes traffic across multiple servers.
- **Compression:** Uses Gzip or Brotli to reduce file sizes.
- **CDN (Content Delivery Network):** Speeds up content delivery.
- **Database Optimization:** Reduces query load on the server.

---

## **Web Server vs Application Server**

|Feature|Web Server|Application Server|
|---|---|---|
|Handles|HTTP requests|Business logic|
|Serves|Static content|Dynamic content|
|Example|Nginx, Apache|Tomcat, Node.js|

---

## **Conclusion**

A web server is a crucial component of web development, enabling users to access websites and applications. Choosing the right web server depends on factors like performance, security, and scalability.

For modern applications, **Nginx and Apache** remain top choices, while **LiteSpeed and Caddy** offer security and performance advantages.

### **Further Reading**

- [Apache HTTP Server Documentation](https://httpd.apache.org/docs/)
- [NGINX Official Site](https://www.nginx.com/)
- [Microsoft IIS Documentation](https://docs.microsoft.com/en-us/iis/)


---

# HTML, CSS, and JavaScript - Detailed Notes

## **Introduction to Web Technologies**

Web development consists of three core technologies:

1. **HTML (HyperText Markup Language)** – The structure of web pages.
2. **CSS (Cascading Style Sheets)** – The styling and layout of web pages.
3. **JavaScript (JS)** – The behavior and interactivity of web pages.

---

# **1. HTML (HyperText Markup Language)**

### **What is HTML?**

HTML is a markup language used to create the structure of web pages. It consists of elements enclosed in tags.

### **Basic Structure of an HTML Document**

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

### **Common HTML Tags**

|Tag|Description|
|---|---|
|`<h1>` - `<h6>`|Headings (h1 is the largest, h6 is the smallest)|
|`<p>`|Paragraph|
|`<a href="url">`|Anchor (link)|
|`<img src="image.jpg">`|Image|
|`<ul>`, `<ol>`, `<li>`|Lists (unordered, ordered, list item)|
|`<table>`|Creates a table|
|`<form>`|Creates an input form|

### **HTML Forms Example**

```html
<form action="submit.php" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <input type="submit" value="Submit">
</form>
```

### **HTML5 Features**

- **Semantic elements** (`<header>`, `<footer>`, `<article>`, `<section>`)
- **Audio and video support** (`<audio>`, `<video>`)
- **Canvas for graphics** (`<canvas>`)

---

# **2. CSS (Cascading Style Sheets)**

### **What is CSS?**

CSS is used to style and layout web pages. It allows developers to apply colors, fonts, spacing, and animations.

### **Types of CSS**

1. **Inline CSS:** Applied directly to an HTML element.
2. **Internal CSS:** Defined inside a `<style>` tag in the HTML `<head>`.
3. **External CSS:** Written in a separate `.css` file and linked to the HTML file.

### **CSS Selectors**

|Selector|Description|
|---|---|
|`*`|Selects all elements|
|`p`|Selects all `<p>` elements|
|`.classname`|Selects all elements with a class|
|`#idname`|Selects a specific element with an ID|

### **Example of CSS Styling**

```css
body {
    background-color: lightblue;
    font-family: Arial, sans-serif;
}

h1 {
    color: darkblue;
    text-align: center;
}

p {
    font-size: 16px;
    line-height: 1.5;
}
```

### **CSS Box Model**

1. **Content:** The actual content inside the box.
2. **Padding:** Space between content and the border.
3. **Border:** The outline around the element.
4. **Margin:** Space outside the border separating elements.

```css
div {
    width: 200px;
    height: 100px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```

### **CSS Flexbox & Grid**

- **Flexbox:** Used for designing one-dimensional layouts.
- **Grid:** Used for designing two-dimensional layouts.

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

---

# **3. JavaScript (JS)**

### **What is JavaScript?**

JavaScript is a programming language used to make web pages interactive.

### **Basic JavaScript Example**

```html
<button onclick="showMessage()">Click Me</button>
<script>
    function showMessage() {
        alert("Hello, JavaScript!");
    }
</script>
```

### **JavaScript Variables & Data Types**

```js
let name = "John"; // String
const age = 25; // Number
let isActive = true; // Boolean
```

### **JavaScript Functions**

```js
function greet(user) {
    return "Hello, " + user + "!";
}
console.log(greet("Alice"));
```

### **JavaScript Events**

|Event|Description|
|---|---|
|`onclick`|Fires when an element is clicked|
|`onmouseover`|Fires when the mouse is over an element|
|`onload`|Fires when a page is fully loaded|

```html
<button id="btn">Click Me</button>
<script>
    document.getElementById("btn").addEventListener("click", function() {
        alert("Button clicked!");
    });
</script>
```

### **DOM Manipulation**

JavaScript can manipulate HTML elements dynamically.

```js
document.getElementById("title").innerHTML = "New Title";
```

### **JavaScript ES6 Features**

- **Arrow Functions:**

```js
const add = (a, b) => a + b;
console.log(add(3, 4));
```

- **Template Literals:**

```js
let name = "John";
console.log(`Hello, ${name}!`);
```

- **Destructuring:**

```js
let person = { name: "Alice", age: 30 };
let { name, age } = person;
console.log(name, age);
```

---

# **Conclusion**

- **HTML provides structure.**
- **CSS adds design and styling.**
- **JavaScript makes pages interactive.**

### **Further Reading**

- [HTML Tutorial](https://www.w3schools.com/html/)
- [CSS Guide](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

---

# Introduction to Python Web Frameworks

## **What is a Web Framework?**

A web framework is a software tool that provides a structured way to develop web applications. It simplifies the process of handling HTTP requests, database interactions, templating, and security features.

## **Why Use a Web Framework?**

- Reduces development time by providing built-in functions.
- Improves security by preventing common vulnerabilities (e.g., SQL injection, XSS attacks).
- Encourages code reusability and maintainability.
- Offers scalability and performance optimization features.

---

## **Types of Python Web Frameworks**

Python web frameworks are classified into three types:

### **1. Full-Stack Frameworks**

These frameworks provide everything needed for web application development, including ORM (Object Relational Mapping), authentication, and templating engines.

- **Examples:**
    - Django
    - Web2py
    - TurboGears

### **2. Microframeworks**

Microframeworks offer minimal functionalities, allowing developers to add only what is needed.

- **Examples:**
    - Flask
    - Bottle
    - CherryPy

### **3. Asynchronous Frameworks**

These frameworks are designed to handle a large number of concurrent connections efficiently.

- **Examples:**
    - FastAPI
    - Tornado
    - Sanic

---

## **Popular Python Web Frameworks**

### **1. Django (Full-Stack Framework)**

#### **Overview:**

- Django is a high-level framework that follows the **MTV (Model-Template-View)** pattern.
- It is designed to help developers build applications quickly and securely.

#### **Key Features:**

- Built-in authentication system
- ORM for database interactions
- Admin panel for easy management
- Security features (CSRF protection, SQL injection prevention)
- Scalability and performance optimization

#### **Example: Creating a Django Project**

```sh
pip install django
django-admin startproject myproject
cd myproject
python manage.py runserver
```

#### **Basic Django View Example**

```python
from django.http import HttpResponse

def home(request):
    return HttpResponse("Hello, Django!")
```

---

### **2. Flask (Microframework)**

#### **Overview:**

- Flask is a lightweight and flexible microframework.
- It follows the **WSGI (Web Server Gateway Interface)** standard.

#### **Key Features:**

- Minimalistic with an extensible design
- Jinja2 templating engine
- Integrated development server and debugger
- Support for RESTful APIs

#### **Example: Creating a Flask App**

```sh
pip install flask
```

#### **Basic Flask Application**

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, Flask!"

if __name__ == '__main__':
    app.run(debug=True)
```

---

### **3. FastAPI (Asynchronous Framework)**

#### **Overview:**

- FastAPI is a modern, high-performance web framework for building APIs.
- It is based on **ASGI (Asynchronous Server Gateway Interface)** and Python type hints.

#### **Key Features:**

- Automatic API documentation with Swagger and ReDoc
- Asynchronous support using `async/await`
- Fast execution speed
- Dependency injection system

#### **Example: Creating a FastAPI App**

```sh
pip install fastapi uvicorn
```

#### **Basic FastAPI Application**

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI!"}

if __name__ == "__main__":
    import uvicorn
    uvicorn.run(app, host="127.0.0.1", port=8000)
```

---

## **Comparison of Python Web Frameworks**

|Feature|Django|Flask|FastAPI|
|---|---|---|---|
|Type|Full-Stack|Micro|Asynchronous|
|Performance|Moderate|High|Very High|
|Learning Curve|Moderate|Easy|Moderate|
|Built-in ORM|Yes|No|No|
|Ideal Use Cases|Large applications|Small projects, APIs|High-performance APIs|

---

## **Conclusion**

- **Django** is best for full-fledged applications requiring built-in features.
- **Flask** is ideal for small projects where flexibility is needed.
- **FastAPI** is the best choice for high-performance, asynchronous APIs.

### **Further Reading**

- [Django Documentation](https://docs.djangoproject.com/)
- [Flask Documentation](https://flask.palletsprojects.com/)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)