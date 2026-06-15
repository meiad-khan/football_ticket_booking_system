# Football Ticket Booking System

## Project Overview

This project is a Database Management System (DBMS) assignment based on a Football Ticket Booking System. The system manages football fans, football matches, and ticket bookings. It demonstrates database design concepts, ERD modeling, table relationships, and SQL query implementation.

---

## Objectives

* Design an Entity Relationship Diagram (ERD)
* Implement relational database tables
* Apply Primary Keys and Foreign Keys
* Maintain Referential Integrity
* Write SQL queries using:

  * Filtering
  * Pattern Matching
  * Joins
  * Subqueries
  * Aggregation Functions
  * NULL Handling
  * Pagination

---

## Database Schema

### Users

Stores information about platform users and administrators.

| Column       | Description                    |
| ------------ | ------------------------------ |
| user_id (PK) | Unique user identifier         |
| full_name    | User's full name               |
| email        | User email address             |
| role         | Football Fan or Ticket Manager |
| phone_number | Contact number                 |

### Matches

Stores football match information.

| Column              | Description                                  |
| ------------------- | -------------------------------------------- |
| match_id (PK)       | Unique match identifier                      |
| fixture             | Teams participating in the match             |
| tournament_category | Competition name                             |
| base_ticket_price   | Standard ticket price                        |
| match_status        | Available, Selling Fast, Sold Out, Postponed |

### Bookings

Stores ticket purchase records.

| Column          | Description                             |
| --------------- | --------------------------------------- |
| booking_id (PK) | Unique booking identifier               |
| user_id (FK)    | References Users table                  |
| match_id (FK)   | References Matches table                |
| seat_number     | Allocated seat                          |
| payment_status  | Pending, Confirmed, Cancelled, Refunded |
| total_cost      | Final booking cost                      |

---

## Entity Relationship Diagram (ERD)

### Relationships

* One User → Many Bookings (1:M)
* One Match → Many Bookings (1:M)
* Each Booking links one User to one Match

### Foreign Keys

```sql
Bookings.user_id  → Users.user_id
Bookings.match_id → Matches.match_id
```

---

## SQL Concepts Demonstrated

### Query 1

Retrieve available Champions League matches.

### Query 2

Search users using LIKE and ILIKE.

### Query 3

Handle NULL payment status using COALESCE.

### Query 4

Retrieve booking details using INNER JOIN.

### Query 5

Display all users including those without bookings using LEFT JOIN.

### Query 6

Use a subquery to compare booking costs with the average booking cost.

### Query 7

Apply ORDER BY, LIMIT, and OFFSET for pagination.

---

## Sample Data

The database contains sample records for:

* 4 Users
* 5 Matches
* 5 Bookings

These records were provided as part of the assignment specification.

---

## Project Structure

```text
Football_Ticket_Booking_System/
│
├── QUERY.sql
├── README.md
```

---

## Technologies Used

* PostgreSQL
* SQL
* Beekeeper Studio
* Git & GitHub

---

## Author

**Md Meiad Khan**

Database Management System Assignment

---


This project was developed for academic learning purposes and demonstrates relational database design and SQL query implementation.
