# program-59
import mysql.connector

conn = mysql.connector.connect(
    host='localhost',
    user='root',
    passwd='',
    database='db1'
)

cursor = conn.cursor()

# Insert record
cursor.execute("INSERT INTO books VALUES (101, 'Python')")
conn.commit()
print("Record inserted successfully")

# Fetch records
cursor.execute("SELECT * FROM books")
result = cursor.fetchall()

print(result)

# Close connection
cursor.close()
conn.close()
output
Record inserted successfully
[(101, 'Python')]
