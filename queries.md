1. Selezionare tutti gli studenti nati nel 1990. (160)

```sql
SELECT id, name, surname, date_of_birth
FROM university.students
WHERE students.date_of_birth LIKE "1990%";
```

2. Selezionare tutti i corsi che valgono più di 10 crediti. (479)

```sql
SELECT id, degree_id, name, cfu
FROM university.courses
WHERE cfu >10;
```

3. Selezionare tutti gli studenti che hanno più di 30 anni.

```sql
SELECT id, name, surname, date_of_birth
FROM university.students
WHERE students.date_of_birth < DATE_SUB(CURDATE(), INTERVAL 30 YEAR);
```

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea. (286)

```sql
SELECT id, degree_id, name, period, year
FROM university.courses
WHERE courses.period = "I semestre" AND courses.year = "1";
```

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020. (21)

6. Selezionare tutti i corsi di laurea magistrale. (38)

7. Da quanti dipartimenti è composta l'università? (12)

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
