<h1>
  <span class="headline">EJS Lab</span>
  <span class="subhead">Setup</span>
</h1>

## Setup

Open your Terminal application and navigate to your `~/code/ga/labs` directory:

```bash
cd ~/code/ga/labs
```

Make a new repository on [GitHub](https://github.com/) named ejs-lab.

Clone a copy of your remote repo locally by using the `git clone` command:

```bash
git clone https://github.com/<your-username>/ejs-lab.git
```

> 📚 Note: In the link above, where it says `<your-username>`, you should see the username from your GitHub account.

Next, `cd` into your new cloned directory, `ejs-lab`:

```bash
cd ejs-lab
```

Then, create a **`server.js`** file and a **`views`** directory. Your views directory will hold the various **`ejs`** files you will create during this lab:

```bash
touch server.js
mkdir views
```

Once you have created the **`server.js`** file, initialize this directory for npm and install the express package:

```bash
npm init -y
```

Next, install both the `express` and `ejs` modules. We can install both modules in a single line:

```bash
npm install express ejs
```

Open the project's folder in your code editor:

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
