# User Stories: E-Commerce Platform

**Total User Stories:** 12
**Estimated Effort:** 32 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality allowing users to sign up with an email and password.

**Acceptance Criteria:**
- Users can enter their email and password during registration.
- A confirmation email is sent to the user's email address.
- A unique user ID is generated upon successful registration.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement secure login and logout functionality for users.

**Acceptance Criteria:**
- Users can log in using their email and password.
- Users can log out of their account.
- Session management is handled securely.

**Linked FRs:** FR-2

### US3: System shall support password reset via email.
Implement password reset functionality allowing users to reset their password via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- A password reset link is sent to the user's email address.
- Users can reset their password using the provided link.

**Linked FRs:** FR-3

## Sprint Week 2: Sprint 2

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login functionality for Google and Facebook.

**Acceptance Criteria:**
- Users can log in using their Google or Facebook accounts.
- OAuth tokens are securely stored.
- User profiles are linked to their OAuth accounts.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
Implement password encryption to ensure stored passwords are secure.

**Acceptance Criteria:**
- Passwords are hashed and stored securely.
- Password hashing algorithm is up to date.
- Password verification is performed securely.

**Linked FRs:** FR-5

### US6: Sellers shall be able to add new products.
Implement functionality for sellers to add new products to the catalog.

**Acceptance Criteria:**
- Sellers can add new products with required details.
- Products are stored in the database.
- Products are visible in the product catalog.

**Linked FRs:** FR-6

## Sprint Week 3: Sprint 3

### US7: Sellers shall be able to update product details.
Implement functionality for sellers to update existing products.

**Acceptance Criteria:**
- Sellers can update product details.
- Product updates are reflected in the catalog.
- Product updates are stored in the database.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement functionality for sellers to delete products from the catalog.

**Acceptance Criteria:**
- Sellers can delete products.
- Deleted products are removed from the catalog.
- Deleted products are marked as inactive in the database.

**Linked FRs:** FR-8

### US9: Products shall contain name, description, price, images, stock quantity, category.
Implement product details management for sellers.

**Acceptance Criteria:**
- Products have a name, description, price, images, stock quantity, and category.
- Product details are stored in the database.
- Product details are displayed in the product catalog.

**Linked FRs:** FR-9

## Sprint Week 4: Sprint 4

### US10: Admin shall approve seller products before publishing (optional).
Implement product approval functionality for admin.

**Acceptance Criteria:**
- Admin can approve or reject seller products.
- Approved products are published in the catalog.
- Rejected products are not visible in the catalog.

**Linked FRs:** FR-10

### US11: Users shall browse products by category.
Implement category-based product browsing functionality.

**Acceptance Criteria:**
- Users can browse products by category.
- Products are categorized and displayed accordingly.
- Category filters are applied to the product list.

**Linked FRs:** FR-11

### US12: Users shall search products by keywords.
Implement keyword-based product search functionality.

**Acceptance Criteria:**
- Users can search for products using keywords.
- Search results are displayed based on keyword matches.
- Search results are ranked based on relevance.

**Linked FRs:** FR-12
