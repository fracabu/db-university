ESERCZIO 2

1. Selezionare tutti gli studenti nati nel 1990 (160)
2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
3. Selezionare tutti gli studenti che hanno più di 30 anni
4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)
5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
6. Selezionare tutti i corsi di laurea magistrale (38)
7. Da quanti dipartimenti è composta l'università? 



2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
SELECT * FROM `courses` WHERE `cfu` > 10;

3. Selezionare tutti gli studenti che hanno più di 30 anni
SELECT *, YEAR (NOW()) , YEAR (`date_of_birth`) FROM `students` WHERE YEAR (NOW()) - YEAR (`date_of_birth`) >= 30 ORDER BY `date_of_birth`;


5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
SELECT * FROM `exams` WHERE `hour`>= '14:00' AND `date` = '2020-06-22' ORDER BY `hour`;