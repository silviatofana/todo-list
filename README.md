![](https://img.shields.io/badge/Microverse-blueviolet)

# Project Name 
 Set up project with webpack

> Description the project.
In this exercise you will build a simple yet powerful webpack boilerplate, which you can later use as a starting point in your projects. You will be working with the webpack official guides, which you know already from the previous lesson.


## Built With

- Major languages
- Frameworks
- Technologies used

## Live Demo (if available)

[Live Demo Link](https://silviatofana.github.io/webpack-exercise/)


## Getting Started

**This is an example of how you may give instructions on setting up your project locally.**
**Modify this file to match your project, remove sections that don't apply. For example: delete the testing section if the currect project doesn't require testing.**


To get a local copy up and running follow these simple example steps.

Instructions
Initialize a new project and install webpack
First set up a new GitHub repository for this exercise.
Follow the instructions from the getting started guide to set up the basics. Implement all the steps from Basic Setup to NPM Scripts.
Add HTML
You already know that all the distribution files will be placed in /dist directory. You also know that you should not create files manually in the /dist folder, as there's a risk they will be overwritten. Therefore, install the HtmlWebpackPlugin to automatically create the index.html file in the /dist directory.
Follow the instructions from the setting up HtmlWebpackPlugin guide. Be extra careful when updating the module.exports object in your webpack.config.js file, to not to make any nesting mistakes.
Now delete all the files from the /dist directory and run:
npm run build
Check your /dist folder. If it contains a new index.html file, it means you were successful.
HTML template
If you plan to write some HTML in your project, it's easiest to do it with a template. Create a /src/index.html in which you can write your markup. Add some basic page markup, like:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wbpack Exercise</title>
</head>
<body>
    <h1>Hello webpack!</h1>
</body>
</html>
Then modify webpack.config.js to point HtmlWebpackPlugin towards your template file:
plugins: [
  new HtmlWebpackPlugin({
-   title: 'Output Management',
+   template: './src/index.html',
  }),
],
You could remove the title property as well (as shown above), because you have set the page title in your /src/index.html.
Run npm run build to update the /dist/index.html.
View the /dist/index.html file in a code editor and notice how webpack inserted a <script> tag with correct path and minified the HTML for better performance.
Add CSS
The next step in building your webpack boilerplate is to add some style to it. Follow the steps in loading CSS guide.

In your style.css file add a generic rule, like:
body {
    background-color: bisque;
}
Next, execute npm run build and check if the HTML body style has changed.
Setup local dev server
Finally, it's time to improve your developer experience. When working on the project you will not want to run the build command from the terminal every time you make a change in the code. Therefore go ahead and install a webpack dev server, which will watch your source files, generate compiled distribution files and even refresh the browser every time you save changes in the source code.

Follow the using webpack-dev-server guide and set it up on your local machine. Again, be cautious with updating the module.exports object in your webpack.config.js.
Once these steps are complete, you should see your application working at: http://localhost:8080/. Every change you make in js or css files now should be reflected in a browser a few seconds later.



## Author

👤 **Silvia Tofana **

- GitHub: [@silviatofana](https://github.com/silviatofana)
- LinkedIn: [@silviatofana](www.linkedin.com/in/silvia-tofana-10b852186)
- Twitter: [@silviatofana](https://twitter.com/SilviaTofana)


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](https://github.com/silviatofana/webpack-exercise).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

## 📝 License

This project is [MIT](./MIT.md) licensed.
