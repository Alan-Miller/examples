
---

## carousel  
Carousel with forward and back buttons and auto-forward.

[github.com/Alan-Miller/carousel](https://github.com/Alan-Miller/carousel)

Tech:
* React

<details>
<summary>Details</summary>

* setInterval changes photos automatically.
* Back and Forward buttons change photo manually and restarts automatic interval.
</details>

---
  
## parallax
Three repos showing different forms of parallax.

> * CSS: [github.com/Alan-Miller/Parallax-CSS](https://github.com/Alan-Miller/Parallax-CSS)

> * background-attachment: [github.com/Alan-Miller/Parallax-Fixed-Image](https://github.com/Alan-Miller/Parallax-Fixed-Image)

> * jQuery: [github.com/Alan-Miller/Parallax-scrollTop](https://github.com/Alan-Miller/Parallax-scrollTop)

Tech:
* CSS (no JavaScript)
* jQuery in vanilla JavaScript environment (scrollTop repo)

---
  
## rpm (react-promise-middleware) list
List app lets user add and delete list items.

[github.com/Alan-Miller/rpm](https://github.com/Alan-Miller/rpm)

Tech:
* React with Redux
* react-promise-middleware
* axios

<details>
<summary>Details</summary>

* Component fires Redux action with promise on payload. Promise resolves with teacher data from database.
* Form adds new teachers on Redux using react-promise-middleware to make axios requests.
* Clicking a teacher in the list deletes the teacher from the database.
</details>

---
  
## shop with cart
Small shop app lets user browse, view details, and place items in cart. 

[github.com/Alan-Miller/cart](https://github.com/Alan-Miller/cart)

Tech:
* React with Redux
* axios

<details>
<summary>Details</summary>

* Shop button makes axios request to outside API and stores response on Redux.
* Clicking a product makes axios request using product ID to get product details, storing response on Redux.
* Add To Cart button pushes product into array stored on Redux. The number of items in the cart is updated in the header (Cart button).
</details>
