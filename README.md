# Pewlett-Hackard-Analysis


## SQL Project



## Overview of Project
 
 
 
 **On this project, we collaborated with Pewlett Hackard, a very Terenure and well-known company that is now implementing retiring packages for their employees. They have decided that they will be using SQL for their segmentation processes. On this project, we will be assisting Bobby, an analyst from the human resources department interested in finding out what employees will be retiring in a near future and what positions will be vacant to find new potential candidates for the available roles. Pewlett Hackard was used to all their data analysis with VBA and excel; however, taking into consideration the enormous amounts of data handled in the company moving to SQL is the best decision..**



### Purpose
 
 
 
 **The purpose of this work is to report findings on the data analyzed and help Bobby Pewlett Hackard’s analyst create a summary report of all the employees about to retire and ultimately understand the number of positions required to be filled in a short time. Bobby is excited to get started on this new project. PH has fallen a bit behind in the database department, so it will be a huge achievement to organize the company. To help Bobby prepare for his analysis, he will need to download his tools: PostgreSQL and pgAdmin. He will use Postgres to create a database and pgAdmin to work with the data he'll be importing. These tools are packaged together in a single download, so let us get started with the setup! The main assignment is to find out what employees could participate in the mentorship program and write a report summarizing our analysis.**


## Analysis 
     

## Results
   
   
  <img width="167" alt="unique_t_" src="https://user-images.githubusercontent.com/81654454/124396070-81dfba80-dcd5-11eb-9f87-459ab1375902.PNG">















<img width="217" alt="mentor_eligibility" src="https://user-images.githubusercontent.com/81654454/124396101-acca0e80-dcd5-11eb-8634-3d2ccf97528a.PNG">

    
   
-	**The first step was creating the unique titles table and joining the employees and titles tables, then filtered them by birth and the dates that the employees were hired. It is essential to ensure that there are no duplicates in our data and ordered them by data engaged; we conclude that about 90,398 employees are retiring as per the above criterion.**




-	 **Then, we formatted the mentorship eligibility table by joining the employees. There were about 1,549 employees eligible for the mentorship program; all eligible employees were constituted by 402 Engineers, 392 Senior staff, 290 senior Engineers, 77 technique leaders, and 56 assistants.**


 
 ### Summary

What are the advantages and recommendations that could contribute to the operations?


-	**The advantage of using the silver tsunami approach is that we should be aware that we are looking for 13,505 employees while preparing all the data. The number represents the number of people currently working on the company since it was funded, and the birth date is between a range from 1962 to 1965 that are eligible to retire. The idea is to offers this employee the mentorship program implemented by the corporate section of the company, so the company keeps this retiring employee mentoring new hires employees.**



-	**Then we use this code to see if there are many mentors in different departments, so the employees leaving table was created.**


**SELECT DISTINCT ON (emp_no) e.emp_no, d.dept_name, e.first_name, e.last_name, e.birth_date, de.from_date, de.to_date, t.title**

**INTO employees_leaving_by_dept**

**FROM employees as e**

**JOIN dept_emp as de**


**ON (e.emp_no = de.emp_no)**

**JOIN titles as t**

**ON (e.emp_no = t.emp_no)**

**LEFT JOIN departments as d**


**ON (de.dept_no = d.dept_no)**

**WHERE (de.to_date = '9999-01-01') AND (e.birth_date BETWEEN '1962-01-01' AND '1965-12-31')**
	
  **AND (de.from_date BETWEEN '1985-01-01' AND '1988-12-31')**

**ORDER BY e.emp_no**















**Finally, it all comes to how many employees are willing to be part of the mentorship program to give a hand to the company with the new hires. We know that there are an estimated number of 13,000 employees retiring and 13,000 new employees, so we recommend that there should be at least 3000 mentors distributed in all departments. It is imperative to point out that for this mentorship program to be successful, there should be a 25% of all retiring employees to become a mentor and help the company with the mentorship of new hires to have a higher success rate in their new roles distributed equally in all departments.** 


