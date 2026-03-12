1. Contare quanti iscritti ci sono stati ogni anno.

```sql
SELECT COUNT(id), YEAR(enrolment_date) AS enrolment_year
FROM university.students
GROUP BY enrolment_year;
```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio.

```sql
SELECT COUNT(id), office_address
FROM university.teachers
GROUP BY office_address;
```

3. Calcolare la media dei voti di ogni appello d'esame.

```sql
SELECT
    exams.id,
    AVG(exam_student.vote) AS average_vote
FROM university.exams
INNER JOIN exam_student ON exams.id = exam_student.exam_id
GROUP BY exams.id;
```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento.

```sql

```
