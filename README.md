# SQL-Database
A relational database containing of 10 tables. 

The list of 10 tables was created for data to be added into the database.

-- Creating tables...
CREATE TABLE IF NOT EXISTS ADDRESS
(
    ADDRESS_ID       VARCHAR(20) PRIMARY KEY
  , STREET           VARCHAR(250)
  , CITY             VARCHAR(100)
  , STATE            VARCHAR(100)
  , COUNTRY          VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS SCHOOL
(
    SCHOOL_ID         VARCHAR(20) PRIMARY KEY
  , SCHOOL_NAME       VARCHAR(100) NOT NULL
  , EDUCATION_BOARD   VARCHAR(80)
  , ADDRESS_ID        VARCHAR(20)
  , CONSTRAINT FK_SCHOOL_ADDR FOREIGN KEY(ADDRESS_ID) REFERENCES ADDRESS(ADDRESS_ID)
);

## Constraints were added to each table for easy data specifications. 
