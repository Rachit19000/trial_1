# User Stories: E-Commerce Platform

**Total User Stories:** 11
**Estimated Effort:** 28 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality allowing users to sign up with an email and password.

**Acceptance Criteria:**
- Users can enter their email and password to register.
- Email and password are stored securely.
- User receives a confirmation email upon successful registration.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement secure login and logout functionality for users.

**Acceptance Criteria:**
- Users can log in using their email and password.
- Users can log out securely.
- Session management is implemented to prevent unauthorized access.

**Linked FRs:** FR-2

### US3: System shall support password reset via email.
Implement password reset functionality allowing users to reset their password via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- A password reset link is sent to the user's email.
- Users can reset their password using the link.

**Linked FRs:** FR-3

## Sprint Week 2: Sprint 2

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login functionality for Google and Facebook.

**Acceptance Criteria:**
- Users can log in using their Google or Facebook account.
- OAuth tokens are securely stored.
- User profile is linked to the system.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
Implement password encryption to ensure stored passwords are secure.

**Acceptance Criteria:**
- Passwords are hashed and stored securely.
- Password hashing algorithm is strong and up-to-date.

**Linked FRs:** FR-5

### US6: Sellers shall be able to add new products.
Implement functionality for sellers to add new products to the platform.

**Acceptance Criteria:**
- Sellers can add new products with name, description, price, images, stock quantity, and category.
- Products are stored in the database.
- Products are visible to users.

**Linked FRs:** FR-6

## Sprint Week 3: Sprint 3

### US7: Sellers shall be able to update product details.
Implement functionality for sellers to update product details.

**Acceptance Criteria:**
- Sellers can update product details including name, description, price, images, stock quantity, and category.
- Updated product details are stored in the database.
- Updated products are visible to users.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement functionality for sellers to delete products from the platform.

**Acceptance Criteria:**
- Sellers can delete products.
- Deleted products are removed from the database.
- Deleted products are no longer visible to users.

**Linked FRs:** FR-8

### US9: Products shall contain name, description, price, images, stock quantity, category.
Ensure products have the required fields for display and management.

**Acceptance Criteria:**
- Products have a name, description, price, images, stock quantity, and category.
- Product details are displayed correctly.
- Product details are managed correctly.

**Linked FRs:** FR-9

## Sprint Week 4: Sprint 4

### US10: Admin shall approve seller products before publishing (optional).
Implement functionality for admin to approve seller products before they are published.

**Acceptance Criteria:**
- Admin can approve or reject seller products.
- Approved products are published.
- Rejected products are not published.

**Linked FRs:** FR-10

### US11: Users shall browse products by category.
Implement functionality for users to browse products by category.

**Acceptance Criteria:**
- Users can browse products by category.
- Products are displayed by category.
- Category filtering works correctly.

**Linked FRs:** FR-11
