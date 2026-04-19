

# Not-for-sell - A Library Management Website

A **peer-to-peer book borrowing platform** where anyone can lend their personal books to others. Unlike traditional libraries, books are **not for sale** — owners lend them for reading and earn a small amount in return.

**Project Tagline**: "Borrow books from real people, not just libraries."

## Use Cases

- **Book Owners**: Add their books to the platform so others can borrow them. They earn a small fee when someone borrows their book.
- **Readers**: Browse available books, take a book manually from the owner after seeing details on the website, and return it later.
- **Billing System**: Each borrowing transaction generates a **bill number** for tracking.
- **Foundation Fund**: A small amount (e.g., 10 TK) from each transaction goes to a foundation fund.

## Main Features

- **Add New Books** — Owners can add book details (name, author, category, status) along with their own info.
- **Browse & Search Books** — Search by book name, author, or category. Filter available books.
- **Take Book** — Readers register a borrowing request with their details. Generates a bill number and updates book status to "Not Available".
- **Return Book** — Two types of return:
  - Return to Owner (get owner contact info)
  - Return to Website (update records, mark as returned, handle foundation payment)
- **Know Bill Number** — In case users forget their bill number.
- **Foundation Management** — Track total fund collected and view users who didn't return books on time or owners who haven't received payment.
- **Remove Books** — Owners can remove their books from the listing.

## Technology Stack

- **Backend**: PHP (MySQLi)
- **Database**: MySQL (`not_for_sell` database)
- **Frontend**: HTML, CSS, Bootstrap (basic styling), JavaScript (minimal)
- **Architecture**: Simple procedural PHP with separate pages for each functionality

## Database Tables

- `book_details` — Stores book information and links to owner
- `owner_details` — Book owner information and status
- `customer_details` — Reader/borrower information
- `bill_details` — Transaction records with bill number, dates, and fund contribution

## How It Works (Flow)

1. Owner adds a book → Book status becomes "Available"
2. Reader searches and takes the book → Status changes to "Not Available", bill is generated
3. Reader returns the book → Status updates to "Available", owner gets notified via contact info
4. Small fee goes to a foundation fund for community support

## Screenshots

(The project includes several images: `1.png`, `2.png`, `4.png`, `5.png`, `7.png`, `images.jpg` showing the UI — homepage, book list, forms, etc.)

## Note

This is a **academic project** demonstrating a simple library management system with a peer-to-peer twist. It focuses on basic CRUD operations, search functionality, and transaction tracking using PHP and MySQL.

**Important**: The system relies on **manual hand-over** of physical books between owner and reader. The website only manages information and billing.
