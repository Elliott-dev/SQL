# SQL
I was hired as a new data engineer at Microsoft. My first major task was a research project on employees of the corporation from the 1980s and 1990s. All that remain of the database of employees from that period are six CSV files.

I designed the tables to hold data in the CSVs, imported the CSVs into a SQL database, and answered questions about the data. In other words, I performed:

Data Engineering

Data Analysis

#### Data Modeling

Inspect the CSVs and sketch out an ERD of the tables. Feel free to use a tool like [http://www.quickdatabasediagrams.com](http://www.quickdatabasediagrams.com).

#### Data Engineering

* Used the information I had to create a table schema for each of the six CSV files. Specified data types, primary keys, foreign keys, and other constraints.

* Imported each CSV file into the corresponding SQL table. Note: I imported the data in the same order that the tables were created and accounted for the headers when importing to avoid errors.

#### Data Analysis

Once you have a complete database, do the following:

Once I got a complete database, I did the following:

1. Listed the following details of each employee: employee number, last name, first name, sex, and salary.

2. Listed first name, last name, and hire date for employees who were hired in 1986.

3. Listed the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.

4. Listed the department of each employee with the following information: employee number, last name, first name, and department name.

5. Listed first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."

6. Listed all employees in the Sales department, including their employee number, last name, first name, and department name.

7. Listed all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.

8. In descending order, listed the frequency count of employee last names, i.e., how many employees share each last name.

#### Part II

As I examined the data, you I overcame with a creeping suspicion that the dataset is fake. I surmised that my boss handed me spurious data in order to test the data engineering skills of a new employee. To confirm my hunch, I decide to take the following steps to generate a visualization of the data, with which I would confront my boss:

1. Imported the SQL database into Pandas. Connected to PostgreSQL like this:

 ```sql
   from sqlalchemy import create_engine
   engine = create_engine('postgresql://localhost:5432/<your_db_name>')
   connection = engine.connect()
   ```

2. Created a histogram to visualize the most common salary ranges for employees.

3. Created a bar chart of average salary by title.

#### References

Mockaroo, LLC. (2021). Realistic Data Generator. https://www.mockaroo.com/
