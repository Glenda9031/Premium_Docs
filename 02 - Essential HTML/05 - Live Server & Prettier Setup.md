# Live Server & Prettier Setup

In the last lesson, we created an HTML document and opened it in the browser. In this lesson, we're going to set up a local server to run our files.

Running files directly from our local file system by double-clicking on them works fine for simple HTML files, but it has limitations, especially when our web pages start to interact with other files or resources, such as CSS stylesheets, JavaScript files, or images.

To overcome these limitations and simulate a more realistic web server environment, we're going to use a VS Code Extension called Live Server. This extension will create a local server that will serve our files and update the browser automatically when we make changes to our files.

I realize that some of you may not be using VS Code and can not use the Live Server extension. If that's the case, there are other solutions available:

- **Python** - You can use Python's built-in HTTP server to serve your files. Open a terminal, navigate to the directory where your files are located, and run the following command: `python -m http.server`. This will start a server on port 8000. You can then open your browser and navigate to `http://localhost:8000` to view your files.
- **http-server** - A simple zero-configuration command-line HTTP server. You would need to install [Node.js](https://nodejs.org) to use this solution and then install the `http-server` package globally by running the following command: `npm install -g http-server`. You can then navigate to the directory where your files are located and run the command `http-server` to start the server.
- **XAMPP** - A free and open-source cross-platform web server solution stack package developed by Apache Friends, consisting mainly of the Apache HTTP Server, MariaDB database, and interpreters for scripts written in the PHP and Perl programming languages. You can download XAMPP from [here](https://www.apachefriends.org/index.html).

## Live Server Setup

Let's start by installing the Live Server extension. Open VS Code and navigate to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window or by pressing `Ctrl+Shift+X`.

In the Extensions view, search for `Live Server` in the search bar. Click on the Install button to install the extension.

Once it is installed, you will see a `Go Live` button in the status bar at the bottom of the window. You can click that or right-click on your HTML file and select `Open with Live Server` to start the server. Your browser will open the URL `http://localhost:5500` with your HTML file.

Go ahead and add a few exclamation marks to the "Hello World!!!!" and save and you should see the changes reflected in the browser immediately.

You now have a nice little development server running your files. This will make it easier to work with your HTML, CSS, and JavaScript files as you build your projects. To stop the server, click the same button or right-click on the HTML file and select `Stop Live Server`.

## Prettier

Prettier is a code formatter extension for VS Code and it is extremely useful with JavaScript, but it can also be useful with HTML & CSS. It will format code automatically. It's been a long time since I didn't have Prettier enabled, so I couldn't tell you if VS Code does this stuff automatically. So I figured I would just show you how to set it up.

Just like with Live Server, go to the exensions icon and search for Prettier and install it. There isn't much configuration that you'll need. One thing I would just be sure to do is go to the settings by clicking on the gear icon in the bottom left or hitting command+comma and then searching for "format on save" and then make sure that's checked. That will make it so that it formats and indents when you save your file. That way you will never have your code unformatted.