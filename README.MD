1. SELECT * FROM `students` WHERE date_of_birth LIKE '1990%'; 
1. SELECT * FROM `courses` WHERE cfu > "10";
1. SELECT * FROM `students` WHERE TIMESTAMPDIFF(YEAR,date_of_birth, CURRENT_DATE()) > 30
1. SELECT * FROM `courses` WHERE period LIKE "I %" AND year LIKE "1";
1. SELECT * FROM `exams` WHERE date = "2020-06-20" AND TIME(hour) > "14:00";
1. SELECT * FROM `degrees` WHERE name LIKE "%magistrale%";
1.
1.