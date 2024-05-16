1. Contare quanti iscritti ci sono stati ogni anno || SELECT COUNT(*), YEAR(enrolment_date) FROM `students` GROUP BY YEAR(enrolment_date);
1. Contare gli insegnanti che hanno l'ufficio nello stesso edificio || SELECT COUNT(*) AS posti_totali, office_address FROM `teachers` GROUP BY office_address;
1. Calcolare la media dei voti di ogni appello d'esame || SELECT AVG(vote) AS media_voti FROM `exam_student`;
1. Contare quanti corsi di laurea ci sono per ogni dipartimento || SELECT COUNT(*) AS degrees_for_departement FROM `degrees` GROUP BY department_id;

#
1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia || SELECT * FROM `students` INNER JOIN degrees ON degrees.id = students.degree_id WHERE degrees.name = "Corso di Laurea in Economia";
1. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze || SELECT * FROM `degrees` INNER JOIN departments ON degrees.department_id = departments.id WHERE degrees.name = "Corsi di Laurea Magistrale" AND departments.name = "Dipartimento di Neuroscienze";
1. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) || SELECT * FROM `teachers` INNER JOIN course_teacher ON teachers.id = course_teacher.teacher_id INNER JOIN courses ON courses.id = course_teacher.teacher_id WHERE teachers.id = 44;
1. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome || SELECT * FROM `students` INNER JOIN degrees ON degrees.id = students.degree_id INNER JOIN departments ON departments.id = degrees.department_id ORDER BY students.surname;
1.  Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti || SELECT * FROM `degrees` INNER JOIN courses ON degrees.id = courses.degree_id INNER JOIN course_teacher ON course_teacher.course_id = courses.id INNER JOIN teachers ON course_teacher.teacher_id = teachers.id;
1. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica || SELECT * FROM `teachers` INNER JOIN course_teacher ON course_teacher.teacher_id = teachers.id INNER JOIN courses ON course_teacher.course_id = courses.id INNER JOIN degrees ON courses.degree_id = degrees.id INNER JOIN departments ON departments.id = degrees.department_id;
