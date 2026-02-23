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

-  ทดสอบ การแสดงผล Web  ผ่าน  Browser   URL http:// (IP address server ) <==บนเครื่อง Client   *ถ้าไม่แสดงผล บนเครื่อง Client ให้ปิดการทำงานของ Firewall บน CentOS  [ดูวิธีการที่นี้](https://github.com/s13anuwat683-creator/CenOs-linux/tree/83d237c3ac9e32fba00a519e5215f1fd01336003/step4%20%E0%B8%AA%E0%B8%B4%E0%B9%88%E0%B8%87%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%95%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%97%E0%B8%B3%E0%B8%AB%E0%B8%A5%E0%B8%B1%E0%B8%87%E0%B8%95%E0%B8%B4%E0%B8%94%E0%B8%95%E0%B8%B1%E0%B9%89%E0%B8%87%20CentOS%20%E0%B9%80%E0%B8%AA%E0%B8%A3%E0%B9%87%E0%B8%88 "ดูวิธีการที่นี้")

