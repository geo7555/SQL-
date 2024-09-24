1) 
SELECT AVG(grade) AS average_grade
FROM Enrollments;
![1](https://github.com/user-attachments/assets/62b60b57-346d-42f1-aac8-38b5cd016d49)

2). 
SELECT s.name AS student_name, c.course_name
FROM Enrollments e
JOIN Students s ON e.student_id = s.student_id
JOIN Courses c ON e.course_id = c.course_id;
![image](https://github.com/user-attachments/assets/8b399d6e-c66b-4337-9faa-bdc39b201240)

3)
SELECT grade_level, COUNT(*) AS student_count
FROM Students
GROUP BY grade_level;
![image](https://github.com/user-attachments/assets/3b46bb34-c355-4c19-a4dc-4a79c3e10e39)

4)
SELECT c.course_name, MAX(e.grade) AS max_grade
FROM Enrollments e
JOIN Courses c ON e.course_id = c.course_id
GROUP BY c.course_name;
![image](https://github.com/user-attachments/assets/e7b83b8e-f78c-4a1a-916f-1b33a6630f73)

5)
SELECT AVG(e.grade) AS average_grade_level_3
FROM Enrollments e
JOIN Students s ON e.student_id = s.student_id
WHERE s.grade_level = 3;
![image](https://github.com/user-attachments/assets/07b4a95f-8870-43ad-9ceb-7fa0d9af0fa1)

6)
SELECT s.name AS student_name, c.course_name, c.credits
FROM Enrollments e
JOIN Students s ON e.student_id = s.student_id
JOIN Courses c ON e.course_id = c.course_id;
![image](https://github.com/user-attachments/assets/d4d4e9ff-c23b-44c1-8cfe-ad0e1e14c2dd)

7)
SELECT c.course_name, AVG(e.grade) AS average_grade
FROM Enrollments e
JOIN Courses c ON e.course_id = c.course_id
GROUP BY c.course_name
HAVING AVG(e.grade) > 3.0;
![image](https://github.com/user-attachments/assets/4da304b2-81f5-4f4a-aeff-095b7fc7ffdd)

8)
SELECT DISTINCT s.name AS student_name
FROM Students s
WHERE s.student_id NOT IN (
    SELECT e.student_id
    FROM Enrollments e
    WHERE e.grade = 4.0
);
![image](https://github.com/user-attachments/assets/3c090169-9e72-4f17-80c2-d42895851d9a)

9)
SELECT s.name AS student_name
FROM Students s
JOIN Enrollments e ON s.student_id = e.student_id
GROUP BY s.student_id, s.name
HAVING AVG(e.grade) > (SELECT AVG(grade) FROM Enrollments);
![image](https://github.com/user-attachments/assets/30e72c51-4860-4db4-8222-f90d0dc3621f)

10)
SELECT s.name AS student_name, COUNT(e.course_id) AS total_courses, AVG(e.grade) AS average_grade
FROM Students s
JOIN Enrollments e ON s.student_id = e.student_id
GROUP BY s.student_id, s.name;
![image](https://github.com/user-attachments/assets/1154d3d0-778f-49e8-a7c0-723f8251f96d)





