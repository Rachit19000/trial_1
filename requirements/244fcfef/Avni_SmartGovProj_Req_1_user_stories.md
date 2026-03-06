# User Stories: E-Commerce Platform

**Total User Stories:** 24
**Estimated Effort:** 30 days

## Sprint Week 1: Sprint 1

### US1: As a user, I want to register using email and password so that I can create an account.
The user should be able to provide an email and password to register.

**Acceptance Criteria:**
- User can enter email and password
- User receives a confirmation message
- User is redirected to the dashboard

**Linked FRs:** FR-1

### US2: As a user, I want to log in securely so that I can access my account.
The user should be able to provide email and password to log in.

**Acceptance Criteria:**
- User can enter email and password
- User receives a confirmation message
- User is redirected to the dashboard

**Linked FRs:** FR-2

### US3: As a user, I want to log out securely so that I can end my session.
The user should be able to log out of their account.

**Acceptance Criteria:**
- User can click logout button
- User is redirected to the login page
- User is logged out

**Linked FRs:** FR-2

### US4: As a user, I want to reset my password via email so that I can regain access to my account.
The user should be able to request a password reset via email.

**Acceptance Criteria:**
- User can enter email
- System sends password reset email
- User can reset password

**Linked FRs:** FR-3

### US5: As a user, I want to authenticate using OAuth so that I can easily log in.
The user should be able to log in using Google or Facebook.

**Acceptance Criteria:**
- User can click OAuth button
- User is redirected to OAuth provider
- User is redirected back to the platform with authentication

**Linked FRs:** FR-4

### US6: As a seller, I want to add new products so that I can list them for sale.
The seller should be able to add new products.

**Acceptance Criteria:**
- Seller can enter product details
- Product is added to the catalog
- Product is visible to users

**Linked FRs:** FR-6

## Sprint Week 2: Sprint 2

### US7: As a seller, I want to update product details so that I can keep my listings accurate.
The seller should be able to update product details.

**Acceptance Criteria:**
- Seller can edit product details
- Product details are updated
- Product is visible to users

**Linked FRs:** FR-7

### US8: As a seller, I want to delete products so that I can remove outdated listings.
The seller should be able to delete products.

**Acceptance Criteria:**
- Seller can select product to delete
- Product is removed from the catalog
- Product is no longer visible to users

**Linked FRs:** FR-8

### US9: As a user, I want to browse products by category so that I can find what I am looking for.
The user should be able to browse products by category.

**Acceptance Criteria:**
- User can select category
- Products in selected category are displayed
- Products are sorted by relevance

**Linked FRs:** FR-11

### US10: As a user, I want to search for products by keywords so that I can find specific items.
The user should be able to search for products by keywords.

**Acceptance Criteria:**
- User can enter search term
- Search results are displayed
- Results are sorted by relevance

**Linked FRs:** FR-12

### US11: As a user, I want to filter products by price, rating, and availability so that I can narrow down my search.
The user should be able to filter products by price, rating, and availability.

**Acceptance Criteria:**
- User can select filters
- Filtered products are displayed
- Filters are applied correctly

**Linked FRs:** FR-13

### US12: As a user, I want to sort products by price, popularity, and rating so that I can prioritize my search.
The user should be able to sort products by price, popularity, and rating.

**Acceptance Criteria:**
- User can select sort option
- Products are sorted as selected
- Sort order is applied correctly

**Linked FRs:** FR-14

## Sprint Week 3: Sprint 3

### US13: As a user, I want to add products to my cart so that I can purchase them later.
The user should be able to add products to their cart.

**Acceptance Criteria:**
- User can select product
- Product is added to cart
- Product is visible in cart

**Linked FRs:** FR-15

### US14: As a user, I want to update the quantity of items in my cart so that I can adjust my order.
The user should be able to update the quantity of items in their cart.

**Acceptance Criteria:**
- User can select quantity
- Quantity is updated
- Total cost is recalculated

**Linked FRs:** FR-16

### US15: As a user, I want to remove items from my cart so that I can adjust my order.
The user should be able to remove items from their cart.

**Acceptance Criteria:**
- User can select item to remove
- Item is removed from cart
- Total cost is recalculated

**Linked FRs:** FR-17

### US16: As a user, I want my cart to persist for logged-in users so that I can continue shopping.
The cart should persist for logged-in users.

**Acceptance Criteria:**
- User logs in
- Cart is restored
- Cart items are visible

**Linked FRs:** FR-18

### US17: As a user, I want to enter my shipping address during checkout so that I can complete my purchase.
The user should be able to enter their shipping address during checkout.

**Acceptance Criteria:**
- User can enter address
- Address is saved
- Address is displayed on confirmation page

**Linked FRs:** FR-19

### US18: As a user, I want the system to calculate the total cost of my order including tax and shipping so that I can see the final amount.
The system should calculate the total cost of the order.

**Acceptance Criteria:**
- System calculates total cost
- Total cost is displayed
- Tax and shipping are included

**Linked FRs:** FR-20

## Sprint Week 4: Sprint 4

### US19: As a user, I want to confirm my order before payment so that I can review my purchase.
The user should be able to confirm their order before payment.

**Acceptance Criteria:**
- User can review order
- User can confirm order
- Order is saved

**Linked FRs:** FR-21

### US20: As a user, I want the system to generate a unique order ID so that I can track my purchase.
The system should generate a unique order ID.

**Acceptance Criteria:**
- System generates unique ID
- ID is displayed
- ID is saved

**Linked FRs:** FR-22

### US21: As a user, I want to view my order history so that I can track my purchases.
The user should be able to view their order history.

**Acceptance Criteria:**
- User can view orders
- Orders are displayed
- Orders are sorted by date

**Linked FRs:** FR-23

### US22: As a user, I want to integrate with a payment gateway so that I can securely process payments.
The system should integrate with a payment gateway.

**Acceptance Criteria:**
- System integrates with payment gateway
- Payment is processed
- Order is confirmed

**Linked FRs:** FR-24

### US23: As a user, I want to support multiple payment methods including credit/debit cards, UPI, and net banking so that I can choose my preferred method.
The system should support multiple payment methods.

**Acceptance Criteria:**
- System supports multiple payment methods
- Payment method is selected
- Payment is processed

**Linked FRs:** FR-25

### US24: As a user, I want the system to handle failed transactions gracefully so that I can retry payment.
The system should handle failed transactions.

**Acceptance Criteria:**
- System handles failed transactions
- User is notified
- Transaction is retried

**Linked FRs:** FR-27
