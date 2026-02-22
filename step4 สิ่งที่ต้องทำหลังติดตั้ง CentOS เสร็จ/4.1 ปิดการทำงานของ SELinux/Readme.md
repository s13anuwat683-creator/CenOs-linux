### ปิดการทำงานของ SELinux
------------
####Security-Enhanced Linux (SELinux) ปิดการทำงานของ SELinux 

โดยการแก้ไขไฟล์/etc/selinux/config  โดยการเปลี่ยนจาก SELINUX=enforcing เป็น SELINUX=disabled ดังตัวอย่างด้านล่างนี้


#### 1\. ให้พิมพ์ คำสั่ง 
*#cd /etc/selinux/config*    

*#nano config*     ⏪⏪⏪  เปิด / แก้ไข Script file config

#### 2\. เปิด / แก้ไข Script file config  ดังน้

SELINUX=disabled   <=== แก้ไข SELINUX=enforcing เป็น ***SELINUX=disabled***

#### 3\. หลังจากแก้ไขไฟล์เรียบร้อยแล้วให้รีสตาร์ทเครื่อง

*#init6*


#### 4 \. ตรวจสอบการทำงานของ SELINUX 

#getenforce 		⏪⏪⏪ แสดงสถานะ Disable

------------
