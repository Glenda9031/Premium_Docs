# How The Web Works

Before we jump in and start to write HTML and CSS, I want to talk about how the web works at a very high level. We won't get in to deep because the truth is, you don't need to know most of this to get started with HTML and CSS. You'll learn a lot along the way. However, it's good to just have a basic overview.

Let's start by just thinking about going to a website. You type a URL into your browser like https://traversymedia.com and it shows my website. URL stands for `Uniform Resource Locator` and it includes the protocol, which in this case is `https`, the domain name and then if you're looking for a specific page or resource, you would put that after the slash. Maybe something like "about.html". If you don't include a resource, it will just show the root or home page, which is typically named "index.html".

The machine that you're on and the browser that is making the request to this URL is called the **client**. The client is making what we call an HTTP request to the **server**. HTTP is a protocol and I'll talk more about that in a minute. So you have this client-server model and the server then sends back a response. This response is usually an HTML file. This file is then rendered by the browser and you see the website. The HTML file can also include links to CSS files, JavaScript file, images, etc. The browser then makes additional requests for these resources.

Your machine has an IP Address that identifies it on the internet. Actually, your public IP refers to your gateway or your router rather than the individual computer. Although each computer and device in your home has a local IP address as well, but that's beyond the scope of what we need to know here.

When you type in a URL with a domain name, that gets converted to the IP Address of the server. This is done through a **DNS** (Domain Name System) server. This is like a phone book for the internet. It's a system that maintains a directory of domain names and translates them to IP Addresses.

That's a very high level view of how the web works and what happens when you visit a webpage.

## HTTP Overview

Let's talk a bit more about **HTTP** (Hypertext Transfer Protocol). It's a communication protocol that you can think of as a language that allow browsers and other clients to talk to servers. When we make the request and get the response back, it's over this HTTP protocol. That's why website URLs start with HTTP or HTTPS. The S stands for secure and means that the data is encrypted. 

HTTP is stateless, which means each request-response cycle is independant from previous transactions. When you refresh a webpage, it is a completely different request than the last refresh and nothing carries over from it. Sometimes you may see something like a welcome message with your name. That name is stored in something called a session or through cookies on the server or client side. These mechanisms help maintain some level of statefulness within an otherwise stateless protocol. This is stuff you'll learn about much later.

When you make an HTTP request, you also get back a status code. When you start getting into server-side development or even client-side JavaScript, you'll need to know the important status codes. Right now, just know that 200 is a successful response. If you go to a URL that doesn't exist, that's a 404 status code. You've probably seen that before.

There are many different types of requests that can be made. The most common is a **GET** request. This is when you're just fetching data. There's also **POST** which is when you're sending data to the server. There's also **PUT** and **DELETE** which are used to update and delete data. This is not stuff that you need to worry about right now, but it's good to just have a basic understanding.

In the next lesson, we'll talk more about what HTML and CSS is as well as the roles that they play in web development.
