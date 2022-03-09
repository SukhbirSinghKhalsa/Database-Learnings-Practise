# DATABASE

#------------------CONSTRAINTS

NOT NULL Constraint 	   -- <br>Ensures that a column cannot have Null value<br>

DEFAULT Constraint  	   -- <br>Provides a default value for a column where none is specified/ given or value not inserted<br>
			                      Eg: auto generate Pass@123 for all the user appering for assessment 	  <br><br>
UNIQUE Constraint   	   -- <br>Ensures that all the values in column are different<br>
	                      Eg: no repeatation of number, it could be your adhaar card, pan no, bank account no,<br>
			      skills, background, interests, problems, goals, vision 
<br><br>
CHECK Constraint    	   -- <br>Makes sure that all values in column satisfy certain given criteria
			                      Eg: no negative numbers, year must be greater then 2000, age greater then 18, age between 11 - 18
<br><br>
 PRIMARY KEY Constraint  -- <br>Used to Uniquely Identify a row in a table, cannot be NULL and must have all UNIQUE/
                            different values
<br><br>
FOREIGN KEY Constraint   -- <br>Used to ensure referential integrity of the data
<br><br>
#------------------END OF CONSTRAINTS
<br><br><br>


#-----------------LOGICAL OPERATORS

#AND OPERATOR<br>
SELECT col FROM table_name WHERE year-of-passing = 2022 AND stream ="Engineering";

#OR OPERATOR<br>
SELECT col FROM table_name WHERE year-of-passing = 2022 OR experience >= "1 year";

#NOT OPERATOR<br>
SELECT col FROM table_name WHERE NOT age < 18

#-----------------END OF LOGICAL OPERATORS
<br><br><br>


#CREATE NEW TABLE , DUPLICATE OF EXISTING TABLE <br>
CREATE TABLE table_name as SELECT * FROM old_table_name;
<br><br>

#IN OPERATOR<br>
SELECT col FROM table_name WHERE name = "sukhbir" or name = "sukhi" or name = "ssk"<br>
equivalent to<br>
SELECT col FROM table_name WHERE name IN ("sukhbir","sukhi","ssk");
<br><br>

#BETWEEN OPERATOR<br>
SELECT col FROM table_name WHERE salary >= 10000 AND salary <= 30000<br>
equivalent to<br>
SELECT col FROM table_name WHERE salary BETWEEN 10000 AND 30000<br>
<br><br>

#LIKE OPERATOR --- % = any string of any length(including zero length), _ = single character<br>
SELECT col FROM table_name WHERE name LIKE 'Sukh%' //starts with Sukh<br>
SELECT col FROM table_name WHERE name LIKE '%bir'  // ends with bir<br>
SELECT col FROM table_name WHERE name LIKE '_uk%ir' // 2nd & 3rd char = uk, and  2nd last & last char = ir<br>
SELECT col FROM table_name WHERE name LIKE '10_\%' // to check if % present use escape character '\%'<br>
<br><br>

#ORDER BY - default ASC, other option DESC<br>
SELECT col FROM table_name [WHERE condition] ORDER BY age<br>
SELECT col FROM table_name [WHERE condition] ORDER BY year ASC, score DESC<br>
SELECT col FROM table_name [WHERE condition] ORDER BY 2 DESC // 2 is column number<br>
<br><br>

#LIMIT -- limits result set upto desired number of row_count <br>
SELECT col FROM table_name [WHERE condition] LIMIT 5  //here we get 5 rows in our result set
<br><br>
