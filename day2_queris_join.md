1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia (68)

```sql
SELECT students.id, degrees.name
FROM university.students
INNER JOIN university.degrees ON students.degree_id = degrees.id
WHERE degrees.name = 'Corso di Laurea in Economia'
```

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze (1)

```sql
SELECT
	degrees.id AS degrees_id,
	degrees.name AS degrees_name,
    departments.id AS departments_id,
    departments.name AS departments_name
FROM university.degrees

INNER JOIN university.departments
ON degrees.department_id = departments.id

WHERE departments.name = "Dipartimento di Neuroscienze" AND degrees.name LIKE "%Magistrale%"
```

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) (11)

```sql
SELECT
	courses.name AS courses_name,
	course_teacher.*
FROM university.course_teacher

INNER JOIN university.courses
ON courses.id = course_id

WHERE teacher_id = "44"
```

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
   sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome (5000)

```sql
SELECT
	students.id AS students_id,
    students.surname,
    students.name,
    students.degree_id,
    degrees.name AS degree_name,
    degrees.level,
    degrees.department_id,
    departments.name AS department_name
FROM university.students

INNER JOIN university.degrees
ON students.degree_id = degrees.id

INNER JOIN university.departments
ON degrees.department_id = departments.id

ORDER BY students.surname ASC, students.name ASC
```

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti (1317)

```sql

```

6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

```sql

```

7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
   per ogni esame, stampando anche il voto massimo. Successivamente,
   filtrare i tentativi con voto minimo 18. (21880)

```sql

```
