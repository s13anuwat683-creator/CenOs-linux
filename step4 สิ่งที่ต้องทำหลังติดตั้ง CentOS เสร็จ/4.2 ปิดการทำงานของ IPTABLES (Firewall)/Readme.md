### ปิดการทำงานของ IPTABLES (Firewall)
------------
#### CentOS 7แล้วไม่ได้ทำการติดตั้ง iptables สามารถดำเนินการติดตั้ง iptables ดังนี้

####  ติดตั้ง iptables  คำสั่ง 
*#yum install iptables-services -y*    


#### (1) หยุดการทำงานของ Firewall ด้วยคำสั่ง

*#service iptables stop*    

#### ปิดการทำงานเมื่อบูทเครื่องมาใหม่

*#chkconfig iptables off*    

**** เรื่องของการรักษาความปลอดภัยในการเริ่มคอนฟิก ให้ปิดไปก่อน เพราะจะสร้างปัญหาให้กับลีนุกซ์มือใหม่ เป็นอย่างมาก คอนฟิกเสร็จแล้วค่อยมาจัดการเรื่องการรักษาความปลอดภัยทีหลัง


#### (2) หยุดการทำงานของ Firewall ด้วยคำสั่ง
  
*#systemctl stop firewalld*

*#systemctl disable firewalld*

#systemctl mask --now firewalld*

#### ตรวจสอบว่า Firewall ถูกปิดไปหรือยัง 

*#systemctl status firewalld*   ⏪⏪⏪ 

 

------------
