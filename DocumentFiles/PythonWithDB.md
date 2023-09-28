Python can support a number of databases such as SQLite and MySQL. When working with databases, Python can use operations to manipulate data. For example, the delete operation can be executed:

import sqlite3
data = sqlite3.connect(data file)
data.execute(“DELETE from COMPANY where ID = 2;”)

There are other operations as well like update and select, which can directly make changes to databases.

Source: 
https://www.tutorialspoint.com/python_network_programming/python_databases_and_sql.htm#:~:text=Python%20supports%20various%20databases%20like,DML)%20and%20Data%20Query%20Statements.