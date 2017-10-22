# mini tech examples

## shop with cart
#### Small shop app lets user browse, view details, and place items in cart. 

Tech:
> * React with Redux
> * axios

<details>
<summary>Details</summary>

> * Shop button makes axios request to outside API and stores response on Redux.
> * Clicking a product makes axios request using product ID to get product details, storing response on Redux.
> * Add To Cart button pushes product into array stored on Redux. The number of items in the cart is updated in the header (Cart button).
</details>
