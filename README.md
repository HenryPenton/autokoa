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


## Using a run file
