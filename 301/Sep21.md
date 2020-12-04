## EJS

> EJS is a templating language for generating HTML using Javascript. It's simple to add to your server. Just add it to your package list with your preferred package manager (`npm install --save ejs` for npm). Then get your express server running.

```
const express = require('express');
const path = require('path');

const app = express();

app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');

app.get('/', (req, res) => response.render('index'));

app.listen(PORT, () => console.log('server listening on PORT: ${PORT}));
```

> The app.set section is telling express to look for views in the 'views' folder and to use EJS as the templating engine. When the .render() method is called, it takes the name of the file with the template as an argument. In this case, 'index' refers to a file named 'index.ejs' in the views directory.

> The .render() method can also take a second argument: an object of local variables. This allows filling the template's content dynamically. The notation for this in the .ejs file is something like: `<h1>Hello <%= name %></h1>` paired with the object `{name: 'Bob'}`.

npm init -y 
npm i <pakages that are needed like express and cors and such>
