# User Stories: E-Commerce Platform

**Total User Stories:** 10
**Estimated Effort:** 20 days

## Sprint Week 1: Sprint 1

### US1: Users shall be able to register using email and password.
Implement user registration functionality allowing users to create an account with email and password.

**Acceptance Criteria:**
- Users can enter their email and password to register.
- User registration form includes fields for email and password.
- Registration process is secure and stores hashed passwords.

**Linked FRs:** FR-1

### US2: Users shall be able to log in and log out securely.
Implement user login and logout functionality with secure authentication.

**Acceptance Criteria:**
- Users can log in using their email and password.
- Users can log out securely.
- Login and logout process is secure and uses secure tokens.

**Linked FRs:** FR-2

## Sprint Week 2: Sprint 2

### US3: System shall support password reset via email.
Implement password reset functionality allowing users to request a password reset via email.

**Acceptance Criteria:**
- Users can request a password reset via email.
- Email contains a secure link to reset the password.
- Password reset process is secure and uses secure tokens.

**Linked FRs:** FR-3

### US4: System shall support OAuth login (Google, Facebook).
Implement OAuth login functionality allowing users to log in using Google or Facebook accounts.

**Acceptance Criteria:**
- Users can log in using Google or Facebook accounts.
- OAuth login process is secure and uses secure tokens.
- OAuth login integrates with Google and Facebook APIs.

**Linked FRs:** FR-4

### US5: System shall encrypt stored passwords.
Implement password encryption to ensure stored passwords are secure.

**Acceptance Criteria:**
- Passwords are stored in an encrypted format.
- Encryption algorithm is secure and up-to-date.
- Decryption is not possible without the correct key.

**Linked FRs:** FR-5

## Sprint Week 3: Sprint 3

### US6: Sellers shall be able to add new products.
Implement product addition functionality allowing sellers to add new products.

**Acceptance Criteria:**
- Sellers can add new products.
- Product addition form includes fields for name, description, price, images, stock quantity, and category.
- Product addition is secure and validated.

**Linked FRs:** FR-6

### US7: Sellers shall be able to update product details.
Implement product update functionality allowing sellers to modify existing products.

**Acceptance Criteria:**
- Sellers can update product details.
- Product update form includes fields for name, description, price, images, stock quantity, and category.
- Product update is secure and validated.

**Linked FRs:** FR-7

### US8: Sellers shall be able to delete products.
Implement product deletion functionality allowing sellers to remove products.

**Acceptance Criteria:**
- Sellers can delete products.
- Product deletion is secure and validated.
- Product deletion is irreversible.

**Linked FRs:** FR-8

## Sprint Week 4: Sprint 4

### US9: Products shall contain name, description, price, images, stock quantity, category.
Implement product details functionality ensuring products have the required fields.

**Acceptance Criteria:**
- Products have a name, description, price, images, stock quantity, and category.
- Product details are displayed correctly.
- Product details are validated before saving.

**Linked FRs:** FR-9

### US10: Admin shall approve seller products before publishing (optional).
Implement product approval functionality allowing admins to approve or reject products.

**Acceptance Criteria:**
- Admins can approve or reject products.
- Product approval process is secure and validated.
- Approved products are published.
- Rejected products are not published.

**Linked FRs:** FR-10
