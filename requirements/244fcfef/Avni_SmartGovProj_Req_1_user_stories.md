# User Stories: Library Management System

**Total User Stories:** 8
**Estimated Effort:** 32 days

## Sprint Week 1: User Management

### US1: Create User Account
As an administrator, I want to create a new user account with the necessary details.

**Acceptance Criteria:**
- The system creates a new user account with the provided details.
- The system assigns a unique user ID.
- The system sets the initial role to member.

**Linked FRs:** FR1

### US2: Update User Profile
As a user, I want to update my profile details.

**Acceptance Criteria:**
- The system allows the user to update their profile details.
- The system saves the updated profile details.
- The system sends a notification to the user confirming the update.

**Linked FRs:** FR4

## Sprint Week 2: Book Management

### US3: Deactivate Inactive Users
As an administrator, I want to deactivate user accounts that are inactive or expired.

**Acceptance Criteria:**
- The system identifies inactive or expired user accounts.
- The system deactivates the identified user accounts.
- The system sends a notification to the user about account deactivation.

**Linked FRs:** FR5

### US4: Add New Book
As a librarian, I want to add a new book to the library collection.

**Acceptance Criteria:**
- The system allows the librarian to add a new book with the necessary details.
- The system saves the new book details.
- The system updates the book count.

**Linked FRs:** FR6

## Sprint Week 3: Book Issue and Return

### US5: Update Book Record
As a librarian, I want to update an existing book record.

**Acceptance Criteria:**
- The system allows the librarian to update an existing book record.
- The system saves the updated book details.
- The system updates the book count if necessary.

**Linked FRs:** FR7

### US6: Issue Book to User
As a librarian, I want to issue a book to a registered user.

**Acceptance Criteria:**
- The system allows the librarian to issue a book to a user.
- The system records the issue date, due date, and return date.
- The system updates the book availability.

**Linked FRs:** FR14

## Sprint Week 4: Reservation Management

### US7: Return Book
As a librarian, I want to return a book and update its availability.

**Acceptance Criteria:**
- The system allows the librarian to return a book.
- The system updates the book availability.
- The system records the return date.

**Linked FRs:** FR17

### US8: Notify User for Book Availability
As a user, I want to be notified when a reserved book becomes available.

**Acceptance Criteria:**
- The system maintains a reservation queue.
- The system notifies the user when a reserved book becomes available.
- The system updates the reservation status.

**Linked FRs:** FR20
