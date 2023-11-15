# ![EJS Lab - Setup](./assets/tktkhero.png)

## Setup 
Open your Terminal application and navigate to your **`~/code/ga/labs`** directory:

```bash
cd ~/code/ga/labs
```

Make a new directory called **`ejs-lab`**, then enter this directory:

```bash
mkdir ejs-lab
cd ejs-lab
```

Then, create a **`server.js`** file and a **`views`** directory.  Your views directory will hold the various **`ejs`** files you will create during this lab:

```bash
touch server.js
mkdir views
```

Once you have created the **`server.js`** file, initialize this directory for npm and install the express package:

```bash
npm init
```
Hit the return key for every prompt you are given in the initialization process.

We next need to install both the `express` and `ejs` modules. We can install both modules in a single line:

```bash
npm install express ejs
```

Open this project in `VS Code`:
```bash
code .
```

Add the following code to your **`server.js`** file:

```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello There!');
});

app.listen(3000);
```

Start your server using `nodemon`:

```bash
nodemon server.js
```

Lastly, navigate to `localhost:3000` in your browser to be greeted with 'Hello There!' in the browser window