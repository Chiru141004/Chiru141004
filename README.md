import mysql.connector

connection = mysql.connector.connect(

host='localhost',

database='electronics',

user='root',

password='xxxyyyyzzz' )

mySql_insert_query = """

INSERT INTO Laptop (Id, Name, Price, Purchase_date)

VALUES (15, 'Lenovo ThinkPad P71', 6459, '2019-08-14')

"""

cursor = connection.cursor()

cursor.execute(mySql_insert_query)

connection.commit()

print("Record inserted successfully into Laptop table")

connection.close()
