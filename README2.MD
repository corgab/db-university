1. Contare quanti iscritti ci sono stati ogni anno || SELECT COUNT(*), YEAR(enrolment_date) FROM `students` GROUP BY YEAR(enrolment_date);
1. Contare gli insegnanti che hanno l'ufficio nello stesso edificio || SELECT COUNT(*) AS posti_totali, office_address FROM `teachers` GROUP BY office_address;
1. Calcolare la media dei voti di ogni appello d'esame || SELECT AVG(vote) AS media_voti FROM `exam_student`;

1. 
1. 
1. 
1. 
1. 
1. 
1. 
