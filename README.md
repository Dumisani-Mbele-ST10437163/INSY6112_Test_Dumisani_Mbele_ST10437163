Question 3
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
