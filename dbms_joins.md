joins - these are used to join the rows of two or more tbles based on the related columns.

types:
1. inner join - returns only the rows that have the matching values in both tables
Ex:
select students.name, courses.course_name
from students
inner join courses
on students.course_id = courses.id;
(this only shows the studnets, who enrolled in the courses .)

2. left join or left outer join - returns all rows from the left table, and matched rows from the right table. if no match, NULL appears for the right table columns.
Ex:
select studentsname, courses.course_name
from students
left join courses
on students.course_id = courses.id;
( all students ae shown. if  a student not enrolled in any course, course_name will be NULL.)

3. right join or right outer join - returns all rows from the right table and matched rows from the left table. if no match, NULL appears for the left table columns.
Ex: 
select students.name, courses.course_name
from students
right join courses
on students.course_id = courses.id;
(all the course are shown. if no student is enrolled to a course, then NULL is shown at student name.)

4. full outer join - returns all the rows, whenthere is a match either on the left or right table. unmatched rows will have NULL on th emissing side.
Ex:
select students.name, course.course_name
from students
full outer join courses
on students.course_id = courses.id;
(shows all students and all courses. if a student is not enrolled in any course, course name is shown as NULL a course is not enrolled by any student, then student name is shown as NULL
