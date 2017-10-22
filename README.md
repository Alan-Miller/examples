
---
  
## cart
[github.com/Alan-Miller/cart](https://github.com/Alan-Miller/cart)

Small shop app lets user browse, view details, and place items in cart. 

<details>
<summary>Details</summary>

* Shop button makes axios request to outside API and stores response on Redux.
* Clicking a product makes axios request using product ID to get product details, storing response on Redux.
* Add To Cart button pushes product into array stored on Redux. The number of items in the cart is updated in the header (Cart button).
</details>
<br/>


Tech:
* React 
* Redux
* axios

---

## carousel  
[github.com/Alan-Miller/carousel](https://github.com/Alan-Miller/carousel)

Carousel with forward and back buttons and auto-forward.

<details>
<summary>Details</summary>

* setInterval changes photos automatically.
* Back and Forward buttons change photo manually and restarts automatic interval.
</details>
<br/>

Tech:
* React

---
  
## parallax
Three repos showing different forms of parallax.

* CSS: [github.com/Alan-Miller/Parallax-CSS](https://github.com/Alan-Miller/Parallax-CSS)

* background-attachment: [github.com/Alan-Miller/Parallax-Fixed-Image](https://github.com/Alan-Miller/Parallax-Fixed-Image)

* jQuery: [github.com/Alan-Miller/Parallax-scrollTop](https://github.com/Alan-Miller/Parallax-scrollTop)

<details>
<summary>Details</summary>

* Pure CSS parallax repo shows parallax using large layers.
* Fixed-image parallax is a pseudo-parallax effect made by simply setting a background image to be fixed in place so that the elements scroll but the images do not.
* jQuery scrollTop lets you move things on screen at different speeds, or perform other transforms like rotate or fade, based on the amount the user has scrolled from the top of the page.
</details>
<br/>

Tech:
* CSS (no JavaScript)
* jQuery in vanilla JavaScript environment (scrollTop repo)

---

## reducks
[githumb.com/Alan-Miller/reducks](https://githumb.com/Alan-Miller/reducks)

App lets user route to different components, making API and database request, and changing values on Redux.

Tech:
* React 
* Redux
* axios
* massive

---
  
## rpm (react-promise-middleware) list
[github.com/Alan-Miller/rpm](https://github.com/Alan-Miller/rpm)

List app lets user add and delete list items in a database, using Redux to store the values and react-promise-middleware to handle the promises.

<details>
<summary>Details</summary>

* Component fires Redux action with promise on payload. Promise resolves with teacher data from database.
* Form adds new teachers on Redux using react-promise-middleware to make axios requests.
* Clicking a teacher in the list deletes the teacher from the database.
</details>

<details>
<summary>Special instructions</summary>

* Make a teachers table with data. I recommend adding a teachers table to an existing database you already have. To create the table and insert some initial data into it, copy the SQL commands in the createTables.sql file or copy the lines below:
  ```sql
  create table teachers (
    id serial primary key,
    name varchar(40),
    subject varchar(40)
  );

  insert into teachers
  (name, subject)
  values
  ('Philby', 'Chemistry'),
  ('Barnaby', 'Chemistry'),
  ('Monaghan', 'History'),
  ('Grable', 'History'),
  ('Marx', 'Geometry'),
  ('Kim', 'Geometry'),
  ('Termagant', 'English'),
  ('Stiller', 'English');
  ```
* The .gitignore file ignores the config.js file, so make your own config.js file at the root of the project folder. Inside, export an object with a port value and a connection string like the one below:

  ``` js
  module.exports = {
    PORT: 3001, // pick a port number
    connection: 'yourConnectionStringHere' // connection string to your db
  }
  ```
</details>
<br/>

Tech:
* React 
* Redux
* react-promise-middleware
* axios