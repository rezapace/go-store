# Postman API Requests for backend-golang

Below are the detailed Postman API requests for the backend-golang project, including the necessary data and explanations.

## 1. Create Order

**Request**

- **Method:** POST
- **URL:** `http://localhost:8080/orders`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`
- **Body (JSON):**
  ```json
  {
    "products": [
      {
        "product_id": "product-uuid-1",
        "quantity": 2
      },
      {
        "product_id": "product-uuid-2",
        "quantity": 1
      }
    ],
    "address": "123 Main St",
    "cart": true,
    "coin": false
  }
  ```

**Explanation**

This endpoint creates a new order for the user. The `products` array contains the product IDs and quantities. The `address` is the delivery address. The `cart` and `coin` fields are boolean values indicating whether to use the cart and coins, respectively.

## 2. Get Orders

**Request**

- **Method:** GET
- **URL:** `http://localhost:8080/orders`
- **Headers:**
  - `Authorization: Bearer <token>`
- **Query Parameters:**
  - `keyword`: (optional) Search keyword
  - `status`: (optional) Order status (e.g., dikemas, dikirim, diterima)

**Explanation**

This endpoint retrieves a list of orders based on the provided query parameters. The `keyword` can be used to search for orders, and the `status` can filter orders by their status.

## 3. Create Address

**Request**

- **Method:** POST
- **URL:** `http://localhost:8080/addresses`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`
- **Body (JSON):**
  ```json
  {
    "profile_id": 1,
    "address": "123 Main St",
    "city": "CityName",
    "province": "ProvinceName"
  }
  ```

**Explanation**

This endpoint creates a new address for the user's profile. The `profile_id` is the ID of the user's profile, and the `address`, `city`, and `province` fields provide the address details.

## 4. Get Products

**Request**

- **Method:** GET
- **URL:** `http://localhost:8080/products`
- **Headers:**
  - `Authorization: Bearer <token>`
- **Query Parameters:**
  - `status`: (optional) Product status (e.g., tersedia, habis)
  - `keyword`: (optional) Search keyword

**Explanation**

This endpoint retrieves a list of products based on the provided query parameters. The `status` can filter products by their availability, and the `keyword` can be used to search for products.

## 5. Add to Cart

**Request**

- **Method:** POST
- **URL:** `http://localhost:8080/cart`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`
- **Body (JSON):**
  ```json
  {
    "user_id": 1,
    "product_id": "product-uuid-1",
    "quantity": 2
  }
  ```

**Explanation**

This endpoint adds a product to the user's cart. The `user_id` is the ID of the user, the `product_id` is the ID of the product to be added, and the `quantity` is the number of units to add.

## 6. Get Cart

**Request**

- **Method:** GET
- **URL:** `http://localhost:8080/cart`
- **Headers:**
  - `Authorization: Bearer <token>`

**Explanation**

This endpoint retrieves the current cart items for the user. It returns the details of the products in the cart, including their quantities and other relevant information.

## 7. Update Cart Quantity

**Request**

- **Method:** PUT
- **URL:** `http://localhost:8080/cart/{id}`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`
- **Body (JSON):**
  ```json
  {
    "quantity": 3
  }
  ```

**Explanation**

This endpoint updates the quantity of a specific cart item. The `{id}` in the URL is the ID of the cart item to be updated, and the `quantity` field in the body specifies the new quantity.

## 8. Delete Cart Item

**Request**

- **Method:** DELETE
- **URL:** `http://localhost:8080/cart/{id}`
- **Headers:**
  - `Authorization: Bearer <token>`

**Explanation**

This endpoint deletes a specific item from the user's cart. The `{id}` in the URL is the ID of the cart item to be deleted.

## 9. Get Notifications

**Request**

- **Method:** GET
- **URL:** `http://localhost:8080/notifications`
- **Headers:**
  - `Authorization: Bearer <token>`

**Explanation**

This endpoint retrieves the notifications for the user. It returns a list of notifications, including their status (read/unread) and other details.

## 10. Update Notification Status

**Request**

- **Method:** PUT
- **URL:** `http://localhost:8080/notifications/{id}`
- **Headers:**
  - `Authorization: Bearer <token>`

**Explanation**

This endpoint updates the status of a specific notification to mark it as read. The `{id}` in the URL is the ID of the notification to be updated.

## 11. Delete Notification

**Request**

- **Method:** DELETE
- **URL:** `http://localhost:8080/notifications/{id}`
- **Headers:**
  - `Authorization: Bearer <token>`

**Explanation**

This endpoint deletes a specific notification.

# Clicked Code Block to apply Changes From

# Postman API Requests for backend-golang

Below are the detailed Postman API requests for the backend-golang project, including the necessary data and explanations.

## 1. Create Order

**Request**

- **Method:** POST
- **URL:** `http://localhost:8080/orders`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`
- **Body (JSON):**
  ```json
  {
    "products": [
      {
        "product_id": "product-uuid-1",
        "quantity": 2
      },
      {
        "product_id": "product-uuid-2",
        "quantity": 1
      }
    ],
    "address": "123 Main St",
    "cart": true,
    "coin": false
  }
  ```

**Explanation**

This endpoint creates a new order for the user. The `products` array contains the product IDs and quantities. The `address` is the delivery address. The `cart` and `coin` fields are boolean values indicating whether to use the cart and coins, respectively.
These requests cover the main functionalities of the backend-golang project. Adjust the URLs, headers, and body data as needed based on your specific implementation and environment.
