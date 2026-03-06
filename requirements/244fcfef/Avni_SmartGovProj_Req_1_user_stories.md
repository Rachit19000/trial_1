# User Stories: E-Commerce Platform

**Total User Stories:** 10
**Estimated Effort:** 20 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
The system should allow users to create an account by providing an email and password.

**Acceptance Criteria:**
- Users can enter their email and password during registration.
- A confirmation email is sent to the user's email address.
- User registration is successful and a unique user ID is generated.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
The system should allow users to log in with their email and password and log out securely.

**Acceptance Criteria:**
- Users can log in using their email and password.
- Users can log out of their session.
- Session is terminated upon logout.

**Linked FRs:** FR-2

### US3: System shall support password reset via email.
The system should allow users to request a password reset via email.

**Acceptance Criteria:**
- Users can request a password reset by providing their email address.
- A password reset link is sent to the user's email address.
- Users can reset their password using the link.

**Linked FRs:** FR-3

## Sprint Week 2: Sprint 2

### US4: System shall support OAuth login (Google, Facebook).
The system should allow users to log in using OAuth providers like Google and Facebook.

**Acceptance Criteria:**
- Users can log in using Google or Facebook.
- User authentication is handled by OAuth providers.
- User is redirected to the system after successful authentication.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
The system should encrypt stored passwords to ensure data security.

**Acceptance Criteria:**
- Passwords are stored in an encrypted format.
- Encryption algorithm is secure and up-to-date.
- Decryption is not possible without the encryption key.

**Linked FRs:** FR-5

### US6: Sellers shall be able to add new products.
Sellers should be able to add new products to the catalog.

**Acceptance Criteria:**
- Sellers can add new products with details like name, description, price, images, stock quantity, and category.
- Products are stored in the database.
- Products are visible to users.

**Linked FRs:** FR-6

## Sprint Week 3: Sprint 3

### US7: Sellers shall be able to update product details.
Sellers should be able to update product details.

**Acceptance Criteria:**
- Sellers can update product details like name, description, price, images, stock quantity, and category.
- Updates are reflected in the database.
- Updates are visible to users.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Sellers should be able to delete products from the catalog.

**Acceptance Criteria:**
- Sellers can delete products.
- Products are removed from the database.
- Products are no longer visible to users.

**Linked FRs:** FR-8

### US9: Products shall contain name, description, price, images, stock quantity, category.
Products should have the specified details.

**Acceptance Criteria:**
- Products have a name, description, price, images, stock quantity, and category.
- Details are stored in the database.
- Details are visible to users.

**Linked FRs:** FR-9

## Sprint Week 4: Sprint 4

### US10: Admin shall approve seller products before publishing (optional).
Admin should be able to approve or reject products listed by sellers.

**Acceptance Criteria:**
- Admin can view products listed by sellers.
- Admin can approve or reject products.
- Approved products are visible to users.
- Rejected products are not visible to users.

**Linked FRs:** FR-10
