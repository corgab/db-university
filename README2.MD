1. Contare quanti iscritti ci sono stati ogni anno || SELECT COUNT(*), YEAR(enrolment_date) FROM `students` GROUP BY YEAR(enrolment_date);
1. Contare gli insegnanti che hanno l'ufficio nello stesso edificio || SELECT COUNT(*) AS posti_totali, office_address FROM `teachers` GROUP BY office_address;
1. Calcolare la media dei voti di ogni appello d'esame || SELECT AVG(vote) AS media_voti FROM `exam_student`;
1. Contare quanti corsi di laurea ci sono per ogni dipartimento || SELECT COUNT(*) AS degrees_for_departement FROM `degrees` GROUP BY department_id;

#
1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia || SELECT * FROM `students` INNER JOIN degrees ON degrees.id = students.degree_id WHERE degrees.name = "Corso di Laurea in Economia";
1. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze ||
1. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) ||
1. 
1. 
1. 
