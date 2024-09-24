1) 
SELECT AVG(grade) AS average_grade
FROM Enrollments;

2). 
SELECT s.name AS student_name, c.course_name
FROM Enrollments e
JOIN Students s ON e.student_id = s.student_id
JOIN Courses c ON e.course_id = c.course_id;

3)
SELECT grade_level, COUNT(*) AS student_count
FROM Students
GROUP BY grade_level;

4)
SELECT c.course_name, MAX(e.grade) AS max_grade
FROM Enrollments e
JOIN Courses c ON e.course_id = c.course_id
GROUP BY c.course_name;

5)
SELECT AVG(e.grade) AS average_grade_level_3
FROM Enrollments e
JOIN Students s ON e.student_id = s.student_id
WHERE s.grade_level = 3;

6)
