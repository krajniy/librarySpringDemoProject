# Task description:
The local library wants to switch to digital accounting of books. 
We need to implement a web application for them. 
Librarians should be able to register readers, lend books to them, and release books 
(after the reader returns the book to the library).

## Entities
Person (fields: full name (UNIQUE), year of birth) </br>
Book (fields: title, author, year) </br>
Relationship between entities: One to Many.
A person can have many books. A book can only belong to one person. </br>

There are two tables in the database - Person and Book. 
Automatic id generation is configured for all tables

## Required functionality
1) Pages for adding, changing and deleting a person.
2) Pages for adding, editing and deleting a book
3) A page with a list of all people (people are clickable - when clicked,
   go to person's page).
4) A page with a list of all books (books are clickable - when clicked,
   go to the page of the book).
5) The person's page, which shows the values of his fields and the list of books that he
   took. If the person did not take any books, instead of the list should be the text "Man hasn't picked up a single book yet."
6) A page of a book, which shows the values of the fields of this book and the name of the person,
   who took this book. If this book has not been taken by anyone, the text "This the book is free" is shown
7) On the page of the book, if the book is taken by a person, next to his name there should be a button
   "Release book". This button is pressed by the librarian when the reader
   returns this book back to the library. After pressing this button the book again
   becomes loose and disappears from the list of the person's books.
8) On the page of the book, if the book is free, there should be a drop-down list (select)
   with all people and the "Assign book" button. This button is pressed by the librarian
   when the reader wants to take this book home. After pressing this button, the book
   must begin to belong to the selected person and must appear in his list
   books.
9) All fields are be validated - with @Valid and Spring Validator if so
   required

