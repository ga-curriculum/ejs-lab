# ![EJS Lab - Exercise](./assets/tktkhero.png)

## Introduction

This lab provides an opportunity to practice defining routes that respond to requests by rendering data in templates.

## A quick note before you dive in

Don't hesitate to collaborate with your classmates when working through labs.

If you get stuck during the lab, we recommend revisiting the lesson materials first. They're designed to provide you with the information and examples that will help you complete the exercises.

## Lab exercises

First, copy and paste the following data to be used in the lab above your defined route in **`server.js`**:

```javascript
const APP_USER = {
  username: 'Bob Loblaw',
  isAdmin: true,
  sales: 5000,
  inventory: [
    { 
      id: 1,
      name: 'A best selling book',
      qty: 500,
      rating: 5 
    },
    { 
      id: 2,
      name: 'Trendy water bottle',
      qty: 1500,
      rating: 5 
    },
    { 
      id: 3,
      name: 'Used VCR',
      qty: 40,
      rating: 5 
    },
    { 
      id: 4,
      name: 'Dog collar',
      qty: 10,
      rating: 5 
    }
  ]
}
```
### Exercise 1

Create an **`index.ejs`** file inside of your `views` directory.  Once created, add the following boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Index</title>
</head>
<body>
  <h1>Hello there!</h1>
</body>
</html>
```

Now that you have this template created, modify the existing route in **`server.js`** such that the template is now _rendered_ from the response.

### Exercise 2



