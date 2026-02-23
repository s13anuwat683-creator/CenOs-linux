### เปิดใช้งาน userdir ผู้ใช้สามารถสร้างเว็บไซต์ได้โดยใช้การตั้งค่านี้
------

#### คำสั่ง จัดการ user 

*#useradd < user >*        เพิ่มผู้ใช้รายใหม่เข้าไปในระบบ

*#passwduser < user >*	   กำหนดรหัสผ่าน ผู้ใช้รายใหม่เข้าไปในระบบ

#### คำสั่ง ลบผู้ใช้รายเดิม ออกจากระบบ 

*#userdel < user >*	 : ลบผู้ใช้รายเดิม ออกจากระบบ

-----
### ขั้นตอนที่ 1 Configure httpd

📚ใช้คำสั่ง เพื่อแก้ไข ไฟล์ script  userdir.conf  // แก้ไขครั้งเดียว

*# vi /etc/httpd/conf.d/userdir.conf*   หรือ 

*# nano /etc/httpd/conf.d/userdir.conf*   

#### แก้ไข userdir.conf ####

*# line 17: comment out*

*#UserDir disabled*

*# line 24: uncomment*

*UserDir public_html*

*# line 31 - 35*

< Directory "/home/*/public_html">
  
*AllowOverride All     # change*

*Options None     # change*

*Require method GET POST OPTIONS*

< /Directory >

----

#### ใช้คำสั่ง systemctl start เพื่อรันเซอร์วิส

*# systemctl restart httpd* 
