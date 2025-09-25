<img width="390" height="75" alt="image" src="https://github.com/user-attachments/assets/e3e6d7b0-d55c-4d81-843f-064866580547" />Question 3
3.1

USE insy6112_test;

CREATE TABLE Author (
    AuthorID INT AUTO_INCREMENT,
    AuthorName VARCHAR(250) NOT NULL,
    AuthorEmail VARCHAR(50) NOT NULL,
    PRIMARY KEY (AuthorID)
);

3.2

USE insy6112_test;

CREATE TABLE FictionBook (
    BookID INT AUTO_INCREMENT,
    BookTitle VARCHAR(250) NOT NULL,
    PublicationDate VARCHAR(50) NOT NULL,
    PRIMARY KEY (BookID),
    FOREIGN KEY (AuthorID) REFERENCES Author(AuthorID)
);

3.3

INSERT INTO Author (AuthorID, AuthorName, AuthorEmail) VALUES
(1, "Thabo Bless", "thabo@yahoo.com");

INSERT INTO FictionBook (BookID, BookTitle, AuthorID, PublicationDate) VALUES
(1, "Into The Darkness", 1, "2025-02-14");


