# AutoKoa

A simple site server


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

## Using a run file
