# Dulingo--BSAD-384

# ER Model

![ER model](ERModel.png)

# Relational Model 

![Relational model](RelationalSchema.png)

# Source Code

* [Create Script (DDL)](createtable)
* [Populate Script (DML)](Populate)

## Sample Queries

 
### Query 1

Which languages are users learning?

```
 SELECT U.Fname, U.Lname, L.LanguageName
FROM Users AS U
JOIN Learns AS LR ON U.UserID = LR.UserID
JOIN Language AS L ON LR.LanguageID = LR.LanguageID;
```

### Query 2

What are the names and levels of all courses?

```
SELECT C.Name AS CourseName, C.Level
FROM Course AS C;
 ```

### Query 3

What are the full names of users and their signup dates?

```
SELECT 
U.Fname + ' ' + U.Lname AS FullName,  -- Derived field: FullName
U.SignUpDate
FROM Users AS U;
 ```

### Query 4

What is the total number of users?

```
SELECT 
SELECT COUNT(U.UserID) AS NumberOfUsers
FROM Users AS U;
 ```

### Query 5

What are the names of the lessons and their corresponding courses?

```
SELECT L.LessonName, C.Name AS CourseName
FROM Lessons AS L
JOIN Course AS C ON L.CourseID = C.CourseID;
 ```
