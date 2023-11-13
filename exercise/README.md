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

Create a **`details.ejs`** file inside of your `views` directory.  Once created, add boilerplate.

Once this file is created, define a get route called `/details` that will render this template.  As a part of rendering the template, pass the `APP_USER` as a value in the locals object for the view template.  

Modify the template such that it will display the `username`, `isAdmin`, and `sales` values in the template.

### Exercise 3

Create an **`inventory.ejs`** file inside of your `views` directory.  Once created, add the following boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Inventory</title>
</head>
<body>
</body>
</html>
```

Once this file is created, define a get route called `/inventory` that will render this template.  As a part of rendering the template, pass the `APP_USER` as a value in the locals object for the view template.  

Within the template, write logic that will display the name and quantity of each item from the objects in the inventory array if the value for `isAdmin` is true.  As a part of this template, provide a message that displays on the page if the value for `isAdmin` is false.

### Exercise 4

Create an **`inventory-details.ejs`** file inside of your `views` directory.  Once created, add the following boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Inventory Details</title>
</head>
<body>
</body>
</html>
```

Once this file is created, define a get route called `/inventory/:id` that will render this template.  As a part of rendering the template, pass the `APP_USER` as a value in the locals object for the view template.  

Within the template, write logic that will display the details of one item in the inventory if the value in place of the `id` req.params maps to an id value in one of the inventory objects.  As a part of this template, provide a message that displays on the page if the id provided does not correspond with an object.