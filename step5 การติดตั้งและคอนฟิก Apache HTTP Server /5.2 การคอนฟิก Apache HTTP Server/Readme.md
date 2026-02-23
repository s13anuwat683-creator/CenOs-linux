#### ใน CentOS หรือ RedHat  จะใช้ชื่อแพ็กเกจ yum หรือชื่อเซอร์วิสของ Apache HTTP Server ว่า httpd
------------
#### ขั้นตอนที่ 1 ติดตั้ง เซอร์วิสของ Apache HTTP Server ว่า httpd 

#### 1.1\. ใช้คำสั่งตรวจสอบ packet http ว่า ติดตั้งแล้วยัง ให้พิมพ์ คำสั่ง 
*#rpm -q httpd*      ⏪⏪⏪  ***ถ้ายัง ให้ติดตั้ง packet http***

#### 1.2\. ใช้คำสั่ง systemctl start เพื่อรันเซอร์วิส

*#systemctl start httpd*

------------
#### ขั้นตอนที่ 2 เขียน Script html ที่ Directory  

#### ทดลอง เขียน Script html ที่ Directory  

*/var/www/html*    ⏪⏪⏪  ***ตำแหน่งที่อยู่ ไฟล์ ***

ใช้คำสั่ง   

*#nano /var/www/html/index.html*  		⏪⏪⏪  ***ชื่อไฟล์ ต้องตั้งชื่อ index.html*** 

เขียน Script ดังนี้ 

*< html>*

  .........................
  
  .........................
  
*< /html>*

------------

**[x] httpd.sevice  ⏪⏪⏪ เปิด บริการ httpd ทุกครั้งที่ เปิดเครื่อง**

หรือ ใช้คำสั่ง  

*#chkconfig httpd on*

------------

#### ขั้นตอนที่ 3 ทดสอบ 

#### 3.1\. ตรวจสอบ เปิด บริการ httpd  การตรวจสอบสถานะการให้บริการ

*# service httpd status*

**httpd (pid 19014) is running...** ⏪⏪⏪ เปิด บริการ httpd

#### 3.2\. ดูหมายเลข ip address

*# ip addr show*

#### 3.3\. ทดสอบ

- ทดสอบ การแสดงผล Web  ผ่าน  Browser   URL http:// (IP address server ) <==บนเครื่อง Server

-  ทดสอบ การแสดงผล Web  ผ่าน  Browser   URL http:// (IP address server ) <==บนเครื่อง Client   *ถ้าไม่แสดงผล บนเครื่อง Client ให้ปิดการทำงานของ Firewall บน CentOS  ดูวิธีการที่นี้* 

