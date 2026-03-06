# Technical Specification

## 1. System Overview

**Project Name:** Movie Hall Management System

**Description:** A web-based application for managing movie theatre operations including movie scheduling, ticket booking, seat management, payment processing, and reporting.

**Architecture Pattern:** Microservices

### Key Design Decisions

- Use microservices architecture for scalability and maintainability
- Implement RESTful APIs for communication between services
- Use a database to store application data

## 2. Data Model

### Entity: User

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the user |
| name | String | User's full name |
| email | String | User's email address |
| password | String | User's password (hashed) |
| role | String | User's role (Admin or User) |

**Relationships:** Show, Booking

### Entity: Movie

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the movie |
| title | String | Movie title |
| description | String | Movie description |
| duration | Integer | Movie duration in minutes |
| rating | Float | Movie rating |

**Relationships:** Show

### Entity: Show

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the show |
| movie_id | UUID | Foreign key to the Movie entity |
| screen_id | UUID | Foreign key to the Screen entity |
| start_time | Timestamp | Show start time |
| end_time | Timestamp | Show end time |

**Relationships:** Movie, Screen, Booking

### Entity: Screen

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the screen |
| hall_id | UUID | Foreign key to the Hall entity |
| name | String | Screen name |
| layout | String | Seat layout in JSON format |

**Relationships:** Show

### Entity: Hall

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the hall |
| name | String | Hall name |
| capacity | Integer | Hall capacity |

**Relationships:** Screen

### Entity: Booking

| Field | Type | Description |
|-------|------|-------------|
| id | UUID | Unique identifier for the booking |
| user_id | UUID | Foreign key to the User entity |
| show_id | UUID | Foreign key to the Show entity |
| seat_ids | String | Comma-separated list of seat IDs |
| total_amount | Float | Total amount paid for the booking |
| status | String | Booking status (Confirmed, Cancelled, etc.) |

**Relationships:** User, Show

## 3. API Design

| Method | Path | Description |
|--------|------|-------------|
| POST | `/users/register` | Register a new user |
| POST | `/users/login` | User login |
| POST | `/users/logout` | User logout |
| GET | `/movies` | List all movies |
| GET | `/movies/{movie_id}` | Get movie details |
| POST | `/shows` | Add a new show |
| PUT | `/shows/{show_id}` | Update show details |
| DELETE | `/shows/{show_id}` | Delete a show |
| GET | `/shows/{show_id}/seats` | Get seat layout for a show |
| POST | `/bookings` | Book seats for a show |
| GET | `/bookings/{booking_id}` | Get booking details |
| PUT | `/bookings/{booking_id}` | Update booking details |
| DELETE | `/bookings/{booking_id}` | Cancel a booking |
| GET | `/admin/reports` | Get admin reports |

### POST `/users/register`

Register a new user

**Request Body:** User registration details

**Response Body:** User registration confirmation

### POST `/users/login`

User login

**Request Body:** User login credentials

**Response Body:** User login confirmation

### POST `/users/logout`

User logout

**Request Body:** User logout request

**Response Body:** User logout confirmation

### GET `/movies`

List all movies

**Response Body:** List of movies

### GET `/movies/{movie_id}`

Get movie details

**Response Body:** Movie details

### POST `/shows`

Add a new show

**Request Body:** Show details

**Response Body:** Show creation confirmation

### PUT `/shows/{show_id}`

Update show details

**Request Body:** Updated show details

**Response Body:** Show update confirmation

### DELETE `/shows/{show_id}`

Delete a show

**Response Body:** Show deletion confirmation

### GET `/shows/{show_id}/seats`

Get seat layout for a show

**Response Body:** Seat layout

### POST `/bookings`

Book seats for a show

**Request Body:** Seat booking details

**Response Body:** Booking confirmation

### GET `/bookings/{booking_id}`

Get booking details

**Response Body:** Booking details

### PUT `/bookings/{booking_id}`

Update booking details

**Request Body:** Updated booking details

**Response Body:** Booking update confirmation

### DELETE `/bookings/{booking_id}`

Cancel a booking

**Response Body:** Booking cancellation confirmation

### GET `/admin/reports`

Get admin reports

**Response Body:** Admin reports

## 4. Component Breakdown

### UserService

**Responsibility:** Handles user registration, login, and logout

**Depends on:** UserService

### MovieService

**Responsibility:** Manages movie listings and details

**Depends on:** UserService

### ShowService

**Responsibility:** Manages show scheduling and seat availability

**Depends on:** UserService, MovieService

### BookingService

**Responsibility:** Handles seat booking and payment processing

**Depends on:** UserService, ShowService

### AdminService

**Responsibility:** Manages admin operations and reports

**Depends on:** UserService, MovieService, ShowService, BookingService

## 5. Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js |
| Backend | Spring Boot |
| Database | PostgreSQL |
| Infrastructure | AWS |

## 6. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Security vulnerabilities in payment processing | Financial loss and reputation damage | Use a reputable payment gateway and perform regular security audits |
| Database performance issues | Slow response times and user frustration | Optimize database queries and use indexing |
| Concurrency issues | Data inconsistencies and user errors | Implement proper locking mechanisms and use transactions |

## 7. Open Questions

- What is the exact payment gateway to be used?
- How will user roles be managed and enforced?
