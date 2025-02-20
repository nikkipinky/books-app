# Google Books CRUD Application

## Overview
This project is a web application that integrates with the [Google Books API](https://developers.google.com/books) to perform full CRUD (Create, Read, Update, Delete) operations. Users can search for books, add them to a personal collection, edit book details, and delete them as needed.

## Features
- **Search Books**: Fetch books from the Google Books API using keywords.
- **Add to Collection**: Save books to a personal database.
- **Update Book Details**: Edit book information in the collection.
- **Delete Books**: Remove books from the collection.

## Technologies Used
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **API Integration**: Google Books API

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/google-books-crud.git
   cd google-books-crud
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```env
     GOOGLE_BOOKS_API_KEY=your_api_key_here
     DATABASE_URL=your_database_url_here
     ```

4. Start the server:
   ```bash
   npm start
   ```

## API Endpoints

### 1. Search Books (Google Books API)
```http
GET /api/books/search?q=keyword
```
- **Description**: Fetch books from the Google Books API based on a search query.
- **Response**: List of books matching the query.

### 2. Add a Book
```http
POST /api/books
```
- **Request Body**:
  ```json
  {
    "title": "Book Title",
    "author": "Author Name",
    "description": "Book description",
    "thumbnail": "image_url_here"
  }
  ```
- **Response**: Added book details.

### 3. Get All Books
```http
GET /api/books
```
- **Description**: Retrieve all books from the personal collection.

### 4. Update a Book
```http
PUT /api/books/:id
```
- **Request Body**:
  ```json
  {
    "title": "Updated Title",
    "author": "Updated Author"
  }
  ```
- **Response**: Updated book details.

### 5. Delete a Book
```http
DELETE /api/books/:id
```
- **Description**: Remove a book from the collection.


