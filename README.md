# DATABASE

#------------------CONSTRAINTS

NOT NULL Constraint 	   -- Ensures that a column cannot have Null value<br><br>

DEFAULT Constraint  	   -- Provides a default value for a column where none is specified/ given or value not inserted
			                      Eg: auto generate Pass@123 for all the user appering for assessment
<br>
UNIQUE Constraint   	   -- Ensures that all the values in column are different
	                      Eg: no repeatation of number, it could be your adhaar card, pan no, bank account no,
			      skills, background, interests, problems, goals, vision 
<br>
CHECK Constraint    	   -- Makes sure that all values in column satisfy certain given criteria
			                      Eg: no negative numbers, year must be greater then 2000, age greater then 18, age between 11 - 18
<br>
 PRIMARY KEY Constraint  -- Used to Uniquely Identify a row in a table, cannot be NULL and must have all UNIQUE/
                            different values
<br>
FOREIGN KEY Constraint   -- Used to ensure referential integrity of the data
<br>
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

#IN OPERATOR
SELECT col FROM table_name WHERE name = "sukhbir" or name = "sukhi" or name = "ssk"
equivalent to
SELECT col FROM table_name WHERE name IN ("sukhbir","sukhi","ssk");
<br><br>

#BETWEEN OPERATOR
SELECT col FROM table_name WHERE salary >= 10000 AND salary <= 30000
equivalent to
SELECT col FROM table_name WHERE salary BETWEEN 10000 AND 30000
<br><br>

#LIKE OPERATOR --- % = any string of any length(including zero length), _ = single character
SELECT col FROM table_name WHERE name LIKE 'Sukh%' //starts with Sukh
SELECT col FROM table_name WHERE name LIKE '%bir'  // ends with bir
SELECT col FROM table_name WHERE name LIKE '_uk%ir' // 2nd & 3rd char = uk, and  2nd last & last char = ir
SELECT col FROM table_name WHERE name LIKE '10_\%' // to check if % present use escape character '\%'
<br><br>

#ORDER BY - default ASC, other option DESC
SELECT col FROM table_name [WHERE condition] ORDER BY age
SELECT col FROM table_name [WHERE condition] ORDER BY year ASC, score DESC
SELECT col FROM table_name [WHERE condition] ORDER BY 2 DESC // 2 is column number
<br><br>

#LIMIT -- limits result set upto desired number of row_count 
SELECT col FROM table_name [WHERE condition] LIMIT 5  //here we get 5 rows in our result set
<br><br>
