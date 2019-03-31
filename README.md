# AutoKoa

A simple site server with EJS support

## Installing

Install autokoa:

```javascript
npm install --save @henrypenton/autokoa
```

## Setting up a simple HTML server

Create an index.js file and copy in the following:

```javascript
const auto = require("@henrypenton/autokoa");
const app = auto(__dirname);

app.listen(3000);
```

Replacing 3000 with whatever port number you'd like to listen on.

Make two folders named views and public in your root directory, next to index.js.

Place any HTML files inside views and any images, scripts or stylesheets inside public.

index.html will be displayed on accessing ```localhost:3000```

Any subsequent pages such as testpage.html will be available under its name minus its identifier i.e. /testpage.

## Using a run file

Want to use EJS to do some behind the scenes magic?

Add a file in your root directory called run.js and give it the following structure:

```javascript
let pageData = "";

run = async (name, ctx) => {
  switch (name) {
    case 'index':
      pageData = {
        title: 'index'
      }
      break;
    case '/examplepage':
      pageData = {
        title: somethingIGenerated
      }
      break;
  }


  return new Promise(resolve => {
    resolve(pageData);
  });
}

module.exports = run;
```

Inside here you could fetch any data you like and feed it back to the page.

I used the page title on my homepage with:

```javascript
<%= title %>
```
In the html title field.
