1. The first thing I did when opening the database was run the original query and inspect the result. Original Query: SELECT * FROM webfour.webfour where name = '$input'
![Basic Injection Original Query](https://github.com/user-attachments/assets/a1442763-bd11-4b73-a032-f57f484a4252)
2. After reviewing the query I remembered some basic SQL injection tricks I had learned throughout studying for the Sec+ and CySA+ and I attempted to replace the $input in the original query with an *
![image](https://github.com/user-attachments/assets/dd75ff9b-c206-42da-bd67-db3e1e298318)
3. This returned every instance in which name had a value including the flag user and the corresponding flag to complete the lab.
