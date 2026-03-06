# User Stories: E-Commerce Platform

**Total User Stories:** 20
**Estimated Effort:** 20 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality allowing users to create an account with email and password.

**Acceptance Criteria:**
- User can enter email and password during registration.
- User receives a confirmation email after registration.
- User can log in with the registered email and password.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement secure login and logout functionality for users.

**Acceptance Criteria:**
- User can log in using email and password.
- User can log out securely.
- User is redirected to login page after logout.

**Linked FRs:** FR-2

### US3: System shall support password reset via email.
Implement password reset functionality allowing users to request a password reset via email.

**Acceptance Criteria:**
- User can request password reset via email.
- User receives a password reset link via email.
- User can reset password using the link.

**Linked FRs:** FR-3

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login functionality allowing users to log in using Google or Facebook.

**Acceptance Criteria:**
- User can log in using Google or Facebook.
- User is redirected to the application after successful OAuth login.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
Implement password encryption for storing user passwords securely.

**Acceptance Criteria:**
- User passwords are stored in encrypted format.
- Password encryption is applied before storing in the database.

**Linked FRs:** FR-5

## Sprint Week 2: Sprint 2

### US6: Sellers shall be able to add new products.
Implement functionality for sellers to add new products to the catalog.

**Acceptance Criteria:**
- Seller can add a new product with name, description, price, images, stock quantity, and category.
- Product is saved in the database.
- Product is visible in the product catalog.

**Linked FRs:** FR-6

### US7: Sellers shall be able to update product details.
Implement functionality for sellers to update product details.

**Acceptance Criteria:**
- Seller can update product name, description, price, images, stock quantity, and category.
- Product details are updated in the database.
- Product details are reflected in the product catalog.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement functionality for sellers to delete products from the catalog.

**Acceptance Criteria:**
- Seller can delete a product.
- Product is removed from the database.
- Product is no longer visible in the product catalog.

**Linked FRs:** FR-8

### US9: Products shall contain name, description, price, images, stock quantity, category.
Implement product details storage and retrieval functionality.

**Acceptance Criteria:**
- Product name, description, price, images, stock quantity, and category are stored in the database.
- Product details are retrieved and displayed in the product catalog.

**Linked FRs:** FR-9

### US10: Admin shall approve seller products before publishing (optional).
Implement product approval functionality for admin.

**Acceptance Criteria:**
- Admin can approve or reject seller products.
- Approved products are visible in the product catalog.
- Rejected products are not visible in the product catalog.

**Linked FRs:** FR-10

## Sprint Week 3: Sprint 3

### US11: Users shall browse products by category.
Implement functionality for users to browse products by category.

**Acceptance Criteria:**
- User can browse products by category.
- Products are filtered and displayed based on the selected category.

**Linked FRs:** FR-11

### US12: Users shall search products by keywords.
Implement functionality for users to search products by keywords.

**Acceptance Criteria:**
- User can search products by keywords.
- Products matching the search query are displayed.

**Linked FRs:** FR-12

### US13: Users shall filter by price, rating, availability.
Implement functionality for users to filter products by price, rating, and availability.

**Acceptance Criteria:**
- User can filter products by price, rating, and availability.
- Filtered products are displayed.

**Linked FRs:** FR-13

### US14: Users shall sort by price, popularity, rating.
Implement functionality for users to sort products by price, popularity, and rating.

**Acceptance Criteria:**
- User can sort products by price, popularity, and rating.
- Products are displayed in the selected order.

**Linked FRs:** FR-14

### US15: Users shall add products to cart.
Implement functionality for users to add products to cart.

**Acceptance Criteria:**
- User can add a product to the cart.
- Product is added to the cart.
- Product is displayed in the cart.

**Linked FRs:** FR-15

## Sprint Week 4: Sprint 4

### US16: Users shall update quantity in cart.
Implement functionality for users to update the quantity of products in cart.

**Acceptance Criteria:**
- User can update the quantity of a product in the cart.
- Updated quantity is reflected in the cart.
- Total cost of the cart is recalculated.

**Linked FRs:** FR-16

### US17: Users shall remove items from cart.
Implement functionality for users to remove items from cart.

**Acceptance Criteria:**
- User can remove a product from the cart.
- Product is removed from the cart.
- Total cost of the cart is recalculated.

**Linked FRs:** FR-17

### US18: Cart shall persist for logged-in users.
Implement functionality for cart persistence for logged-in users.

**Acceptance Criteria:**
- Cart persists for logged-in users.
- Cart items are retained across sessions.

**Linked FRs:** FR-18

### US19: Users shall enter shipping address.
Implement functionality for users to enter shipping address during checkout.

**Acceptance Criteria:**
- User can enter shipping address.
- Shipping address is saved for the order.

**Linked FRs:** FR-19

### US20: System shall calculate total cost (tax + shipping).
Implement functionality for system to calculate total cost including tax and shipping.

**Acceptance Criteria:**
- Total cost is calculated including tax and shipping.
- Total cost is displayed to the user.

**Linked FRs:** FR-20
