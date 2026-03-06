# User Stories: E-Commerce Platform

**Total User Stories:** 9
**Estimated Effort:** 16 days

## Sprint Week 1: Sprint 1

### US1: User Registration
Users should be able to register using email and password.

**Acceptance Criteria:**
- Users can enter their email and password to register.
- Registration process should be secure and validate input.
- User registration should generate a unique user ID.

**Linked FRs:** FR-1

### US2: User Login
Users should be able to log in and log out securely.

**Acceptance Criteria:**
- Users can enter their email and password to log in.
- System should validate user credentials and generate a session token.
- Users can log out securely.

**Linked FRs:** FR-2

### US3: Password Reset via Email
System should support password reset via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- System should send a password reset link to the user's email.
- Users can reset their password using the link.

**Linked FRs:** FR-3

## Sprint Week 2: Sprint 2

### US4: OAuth Login
System should support OAuth login (Google, Facebook).

**Acceptance Criteria:**
- Users can log in using Google or Facebook credentials.
- OAuth login should be secure and validate user credentials.
- User session should be managed securely.

**Linked FRs:** FR-4

### US5: Product Management for Sellers
Sellers should be able to add, update, and delete products.

**Acceptance Criteria:**
- Sellers can add new products with details.
- Sellers can update product details.
- Sellers can delete products.
- Products should have name, description, price, images, stock quantity, and category.

**Linked FRs:** FR-6, FR-7, FR-8, FR-9

## Sprint Week 3: Sprint 3

### US6: Product Search & Browsing
Users should be able to browse products by category, search by keywords, filter by price, rating, and availability, and sort by price, popularity, and rating.

**Acceptance Criteria:**
- Users can browse products by category.
- Users can search products by keywords.
- Users can filter products by price, rating, and availability.
- Users can sort products by price, popularity, and rating.

**Linked FRs:** FR-11, FR-12, FR-13, FR-14

### US7: Shopping Cart Management
Users should be able to add, update, and remove items from the cart, and the cart should persist for logged-in users.

**Acceptance Criteria:**
- Users can add products to the cart.
- Users can update the quantity of items in the cart.
- Users can remove items from the cart.
- Cart should persist for logged-in users.

**Linked FRs:** FR-15, FR-16, FR-17, FR-18

## Sprint Week 4: Sprint 4

### US8: Checkout & Order Management
Users should be able to enter shipping address, calculate total cost, confirm order before payment, and view order history. Admin should be able to update order status and track order status.

**Acceptance Criteria:**
- Users can enter shipping address.
- System should calculate total cost (tax + shipping).
- Users can confirm order before payment.
- System should generate a unique order ID.
- Users can view order history.
- Admin can update order status (Processing, Shipped, Delivered).
- Users can track order status.

**Linked FRs:** FR-19, FR-20, FR-21, FR-22, FR-23, FR-28, FR-29

### US9: Payment Processing
System should integrate with payment gateway and support credit/debit cards, UPI, net banking. System should confirm payment before order processing and handle failed transactions gracefully.

**Acceptance Criteria:**
- System should integrate with payment gateway.
- Support credit/debit cards, UPI, net banking.
- System should confirm payment before order processing.
- System should handle failed transactions gracefully.

**Linked FRs:** FR-24, FR-25, FR-26, FR-27
