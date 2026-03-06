# User Stories: E-Commerce Platform

**Total User Stories:** 8
**Estimated Effort:** 16 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality allowing users to sign up with an email and password.

**Acceptance Criteria:**
- Users can enter their email and password during registration.
- A unique user ID is generated upon successful registration.
- User data is stored securely with encrypted passwords.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement secure login and logout functionality for users.

**Acceptance Criteria:**
- Users can log in using their email and password.
- Users can log out securely, invalidating their session.
- Session management is handled securely.

**Linked FRs:** FR-2

## Sprint Week 2: Sprint 2

### US3: System shall support password reset via email.
Implement password reset functionality allowing users to reset their password via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- A password reset link is sent to the user's email.
- Users can reset their password using the link.

**Linked FRs:** FR-3

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login functionality allowing users to log in using Google or Facebook.

**Acceptance Criteria:**
- Users can log in using their Google or Facebook accounts.
- User data is securely stored upon successful OAuth login.
- OAuth login is integrated with the system.

**Linked FRs:** FR-4

## Sprint Week 3: Sprint 3

### US5: System shall encrypt stored passwords.
Implement password encryption for all stored user passwords.

**Acceptance Criteria:**
- All stored passwords are encrypted using a secure hashing algorithm.
- Password encryption is applied to all existing and new user accounts.
- Password decryption is not possible without the user's password.

**Linked FRs:** FR-5

### US6: Sellers shall be able to add new products.
Implement functionality for sellers to add new products to the platform.

**Acceptance Criteria:**
- Sellers can add new products with details such as name, description, price, images, stock quantity, and category.
- Products are stored in the database with all required fields.
- Products are visible to users after approval.

**Linked FRs:** FR-6

## Sprint Week 4: Sprint 4

### US7: Sellers shall be able to update product details.
Implement functionality for sellers to update product details.

**Acceptance Criteria:**
- Sellers can update product details such as name, description, price, images, stock quantity, and category.
- Product updates are reflected in the database.
- Updated products are visible to users.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement functionality for sellers to delete products from the platform.

**Acceptance Criteria:**
- Sellers can delete products from the platform.
- Deleted products are no longer visible to users.
- Product deletion is logged for auditing purposes.

**Linked FRs:** FR-8
