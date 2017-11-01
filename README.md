
---
  
## animations
[github.com/Alan-Miller/animations](https://github.com/Alan-Miller/animations)

Simple HTML/CSS page showing two divs that have different animations and transitions. Comments in the CSS explain the use of transitions and animations. Simple JS file adds an onClick event to the divs to add a class to them.

Tech:
* CSS 

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
* CSS and inline styles

---
  
## cart
[github.com/Alan-Miller/cart](https://github.com/Alan-Miller/cart)

Small shop app lets user browse, view details, and place items in cart. 

<details>
<summary>Details</summary>

* Shop button makes axios request to outside API and stores response on Redux.
* Clicking a product makes axios request using product ID to get product details, storing response on Redux.
* Add To Cart button pushes product into array stored on Redux. The number of items in the cart is updated in the header (Cart button).
* Cart button routes to Cart component, which maps through cart items coming from Redux.
* Clicking the "x" on an item in the cart will delete the item from the Redux cart.
</details>
<br/>


Tech:
* React 
* Redux
* axios

---
  
## parallax
Three repos showing different forms of parallax.

* CSS: [github.com/Alan-Miller/Parallax-CSS](https://github.com/Alan-Miller/Parallax-CSS)

* background-attachment: [github.com/Alan-Miller/Parallax-Fixed-Image](https://github.com/Alan-Miller/Parallax-Fixed-Image)

* jQuery: [github.com/Alan-Miller/Parallax-scrollTop](https://github.com/Alan-Miller/Parallax-scrollTop)

<details>
<summary>Details</summary>

* Pure CSS parallax repo shows parallax using large layers.
* Fixed-image parallax is a pseudo-parallax effect made by simply setting the ```background-attachment``` property to ```fixed``` so the elements scroll but the images do not.
* jQuery scrollTop lets you move things on screen at different speeds, or perform other transforms like rotate or fade, based on the amount the user has scrolled from the top of the page.
</details>
<br/>

Tech:
* CSS (no JavaScript)
* jQuery in vanilla JavaScript environment (scrollTop repo)

---

## reducks
[github.com/Alan-Miller/reducks](https://github.com/Alan-Miller/reducks)

App lets user route to different components, making API and database requests and changing values on Redux.

<details>
<summary>Details</summary>

* The intial value of the pokemon property on Redux is an array of two pokemon: Pikachu and Squirtle.
* The Home component subscribes to the pokemon Redux value and renders it. It has a Change Pokemon button that uses the getPokemon Redux action creator to change the value to a different array of two pokemon: Butterfree and Wigglytuff.
* The Pokemon component makes an automatic call to the pokemon outside API and gets the names of all 800+ pokemon available. The promise is handled in the component's componentDidMount method, and the array is stored on Redux with the getPokemon action creator. Routing back to the Home component will show this new (large) array of pokemon is displayed in both components.
* The Database component makes an automatic call to a database to get a user name and id based on an auth ID. In this case, the app grabs a hard-coded auth ID from the component's state object, but in real life this ID might come from a successful authentication using auth0 and then storing that value in a variable that is then passed to the axios request that fetches the user name and id.
</details>

<details>
<summary>Special instructions</summary>

* Make a yoozers table with data. I recommend adding a yoozers table to an existing database you already have. To create the table and insert some initial data into it, copy the SQL commands in the create_tables.sql file or copy the lines below:
  ```sql
    create table yoozers (
      id serial primary key,
      auth_id text,
      name varchar(40)
    );

    insert into yoozers 
    (auth_id, name)
    values
    ('secret_authID_321', 'Nathaniel'),
    ('special_authID_789', 'Jill');
  ```
* The .gitignore file ignores the config.js file, so make your own config.js file at the root of the project folder. Inside, export an object with a port value and a connection string like the one below:

  ``` js
    module.exports = {
      port: 3001, // pick a port number
      connection: 'yourConnectionStringHere' // your connection string
    }
  ```
</details>
<br/>

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
* massive

---
  
## sass-workshop
[github.com/Alan-Miller/sass-workshop](https://github.com/Alan-Miller/sass-workshop)

Example of Sass. README file has detailed instructions for setting up Sass in a React app and using many of Sass's features.

Tech:
* React
* Sass

---
  
## stripe checkout
[github.com/Alan-Miller/stripe-checkout](https://github.com/Alan-Miller/stripe-checkout)

Example of Stripe Checkout (simple) in React. Based on [Joe Blank's repo](https://github.com/joeblank/react-stripe). Contains some extra notes in the comments taken from Joe's explanation of the process.

<details>
<summary>Details</summary>

* Pay With Card button opens form, which gets token back from Stripe. Token can be console logged.
* When the token arrives, a POST request is sent with the token id to the server to make a charge, and a response comes back (if it is an error, the charge failed).
* Summary of Stripe process:
  * User clicks button and completes form.
  * Stripe receives payment information securely.
  * Stripe sends back token to app.
  * Token contains email and other information.
  * Token is stripped of credit card information and send to app server via POST request.
</details>
<br/>

Tech:
* React
* Stripe Checkout

---
  
## stripe checkout (custom button)
[github.com/Alan-Miller/stripe-checkout-custom](https://github.com/Alan-Miller/stripe-checkout-custom)

Example of Stripe Checkout (with custom button) in React. Uses ```<script>``` tag instead of installing ```react-stripe-checkout```.

<details>
<summary>Details</summary>

* Repo uses ```<script src="https://checkout.stripe.com/checkout.js"></script>``` tag in index.html.
* Pay With Card button opens form, which gets token back from Stripe. Token can be console logged.
* When the token arrives, a POST request is sent with the token id to the server to make a charge, and a response comes back (if it is an error, the charge failed).
* Summary of Stripe process:
  * User clicks button and completes form.
  * Stripe receives payment information securely.
  * Stripe sends back token to app.
  * Token contains email and other information.
  * Token is stripped of credit card information and send to app server via POST request.
</details>
<br/>

Tech:
* React
* Stripe Checkout