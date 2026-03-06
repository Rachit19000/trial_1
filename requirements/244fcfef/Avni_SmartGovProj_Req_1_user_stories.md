# User Stories: E-Commerce Platform

**Total User Stories:** 23
**Estimated Effort:** 32 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality with email and password.

**Acceptance Criteria:**
- Users can register with a valid email and password.
- Email and password are stored securely.
- User receives a confirmation email upon registration.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement secure login and logout functionality.

**Acceptance Criteria:**
- Users can log in with their registered email and password.
- Session is terminated upon logout.
- Secure cookies are used for session management.

**Linked FRs:** FR-2

### US3: System shall support password reset via email.
Implement password reset functionality via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- A password reset link is sent to the user's email.
- Users can reset their password using the link.

**Linked FRs:** FR-3

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login for Google and Facebook.

**Acceptance Criteria:**
- Users can log in using their Google or Facebook account.
- OAuth tokens are securely stored.
- User profile is linked to the account.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
Encrypt passwords before storing them in the database.

**Acceptance Criteria:**
- Passwords are hashed and salted before storage.
- Password hashing algorithm is secure.
- Password verification is implemented.

**Linked FRs:** FR-5

## Sprint Week 2: Sprint 2

### US6: Sellers shall be able to add new products.
Implement product addition functionality for sellers.

**Acceptance Criteria:**
- Sellers can add new products with all required details.
- Products are stored in the database.
- Products are visible in the product catalog.

**Linked FRs:** FR-6

### US7: Sellers shall be able to update product details.
Implement product update functionality for sellers.

**Acceptance Criteria:**
- Sellers can update product details.
- Updated product details are stored in the database.
- Updated products are reflected in the product catalog.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement product deletion functionality for sellers.

**Acceptance Criteria:**
- Sellers can delete products.
- Deleted products are removed from the database.
- Deleted products are no longer visible in the product catalog.

**Linked FRs:** FR-8

### US9: Products shall contain name, description, price, images, stock quantity, category.
Implement product details storage and retrieval.

**Acceptance Criteria:**
- Product details are stored in the database.
- Product details are retrieved and displayed correctly.
- Product details are updated and reflected in the product catalog.

**Linked FRs:** FR-9

### US10: Admin shall approve seller products before publishing (optional).
Implement product approval functionality for admins.

**Acceptance Criteria:**
- Admins can approve or reject seller products.
- Approved products are published in the product catalog.
- Rejected products are not visible in the product catalog.

**Linked FRs:** FR-10

## Sprint Week 3: Sprint 3

### US11: Users shall browse products by category.
Implement product browsing by category.

**Acceptance Criteria:**
- Users can browse products by category.
- Products are filtered and displayed by category.
- Category names are displayed correctly.

**Linked FRs:** FR-11

### US12: Users shall search products by keywords.
Implement product search by keywords.

**Acceptance Criteria:**
- Users can search for products by keywords.
- Search results are displayed.
- Search results are filtered by keyword.

**Linked FRs:** FR-12

### US13: Users shall filter by price, rating, availability.
Implement product filtering by price, rating, and availability.

**Acceptance Criteria:**
- Users can filter products by price, rating, and availability.
- Filtered products are displayed.
- Filter options are displayed correctly.

**Linked FRs:** FR-13

### US14: Users shall sort by price, popularity, rating.
Implement product sorting by price, popularity, and rating.

**Acceptance Criteria:**
- Users can sort products by price, popularity, and rating.
- Sorted products are displayed.
- Sort options are displayed correctly.

**Linked FRs:** FR-14

## Sprint Week 4: Sprint 4

### US15: Users shall add products to cart.
Implement product addition to cart.

**Acceptance Criteria:**
- Users can add products to their cart.
- Products are stored in the cart.
- Cart items are displayed to the user.

**Linked FRs:** FR-15

### US16: Users shall update quantity in cart.
Implement cart quantity update functionality.

**Acceptance Criteria:**
- Users can update the quantity of products in their cart.
- Updated quantities are stored.
- Cart items are displayed with updated quantities.

**Linked FRs:** FR-16

### US17: Users shall remove items from cart.
Implement cart item removal functionality.

**Acceptance Criteria:**
- Users can remove items from their cart.
- Removed items are deleted from the cart.
- Cart items are displayed without the removed item.

**Linked FRs:** FR-17

### US18: Cart shall persist for logged-in users.
Implement cart persistence for logged-in users.

**Acceptance Criteria:**
- Logged-in users can access their cart across sessions.
- Cart items are stored and retrieved based on user session.
- Cart items are displayed to the user.

**Linked FRs:** FR-18

### US19: Users shall enter shipping address.
Implement shipping address entry functionality.

**Acceptance Criteria:**
- Users can enter their shipping address.
- Shipping address is stored.
- Shipping address is displayed to the user.

**Linked FRs:** FR-19

### US20: System shall calculate total cost (tax + shipping).
Implement total cost calculation.

**Acceptance Criteria:**
- Total cost is calculated including tax and shipping.
- Total cost is displayed to the user.
- Cost calculation is accurate.

**Linked FRs:** FR-20

### US21: Users shall confirm order before payment.
Implement order confirmation functionality.

**Acceptance Criteria:**
- Users can confirm their order.
- Order confirmation is displayed to the user.
- Order is ready for payment.

**Linked FRs:** FR-21

### US22: System shall generate unique order ID.
Implement unique order ID generation.

**Acceptance Criteria:**
- Unique order ID is generated for each order.
- Order ID is displayed to the user.
- Order ID is stored in the database.

**Linked FRs:** FR-22

### US23: Users shall view order history.
Implement order history display functionality.

**Acceptance Criteria:**
- Users can view their order history.
- Order history is displayed to the user.
- Order history is stored in the database.

**Linked FRs:** FR-23
