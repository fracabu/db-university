
-Selezionare tutti gli studenti che hanno più di 30 anni
SELECT *, YEAR (NOW()) , YEAR (`date_of_birth`) FROM `students` WHERE YEAR (NOW()) - YEAR (`date_of_birth`) >= 30 ORDER BY `date_of_birth`;


-Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
SELECT * FROM `exams` WHERE `hour`>= '14:00' AND `date` = '2020-06-22' ORDER BY `hour`;