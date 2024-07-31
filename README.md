# RentalFlix ERD

## Overview
Welcome to the RentalFlix ERD documentation. This document outlines the Entity-Relationship Diagram (ERD) designed for a movie rental service, detailing the key entities and relationships necessary for efficiently managing the service.

## Entity-Relationship Explanation

### Entities and Relationships

- **Movie - MovieFormat**
  - **Relationship Type:** One-to-Many
  - **Description:** Each movie can be available in multiple formats (e.g., DVD, Blu-ray, digital).
  - **Key:** `Movie.MovieID → MovieFormat.MovieID`

- **Customer - Rental**
  - **Relationship Type:** One-to-Many
  - **Description:** A single customer can have multiple rentals, representing the movies they've rented over time.
  - **Key:** `Customer.CustomerID → Rental.CustomerID`

- **MovieFormat - Rental**
  - **Relationship Type:** Many-to-One
  - **Description:** Multiple rentals can correspond to the same movie format, indicating that different customers may rent the same format of a movie.
  - **Key:** `Rental.FormatID → MovieFormat.FormatID`

- **Movie - Reservation**
  - **Relationship Type:** One-to-Many
  - **Description:** One movie can have multiple reservations, allowing different customers to reserve the same movie.
  - **Key:** `Movie.MovieID → Reservation.MovieID`

- **Customer - Reservation**
  - **Relationship Type:** One-to-Many
  - **Description:** A customer can have multiple reservations, reflecting the movies they wish to rent in the future.
  - **Key:** `Customer.CustomerID → Reservation.CustomerID`

### Key Considerations
- The ERD is designed to accommodate multiple formats for each movie, allowing for flexibility in the rental options available to customers.
- The separation between rentals and reservations provides a clear distinction between movies that customers have rented and those they plan to rent.

## Diagram Overview
The ERD visually represents these relationships, showcasing how each entity is interconnected. This visualization aids in understanding the data flow and relationships within the system, ensuring efficient management of rentals, reservations, and customer interactions.

## Future Enhancements
- **Additional Entities:** Consider including entities such as `Payment`, `Staff`, and `Store` to further refine the management system.
- **Extended Relationships:** Implement many-to-many relationships where applicable, such as between `Movie` and `Actor` to showcase cast details.

## ER Diagram:
![erd](https://github.com/user-attachments/assets/82facf93-db93-4c96-9ffa-1e57dab27d5f)

