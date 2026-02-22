
### วิธีติดตั้ง VSFTP SERVER บน CentOS 7
------------
HTTP เซิร์ฟเวอร์โปรโตคอลการถ่ายโอนไฮเปอร์เท็กซ์ (Hypertext Transfer Protocol) หรือเว็บเซิร์ฟเวอร์คือบริการเครือข่ายที่ให้บริการเนื้อหาแก่ไคลเอนต์ผ่านทางเว็บ โดยทั่วไปหมายถึงเว็บเพจ แต่เอกสารอื่นๆ ก็สามารถให้บริการได้เช่นกัน
เว็บเซิร์ฟเวอร์ที่มีให้ใช้งานใน CenOS ได้แก่:เซิร์ฟเวอร์ Apache HTTP


#### 1. ตรวจสอบแพ็กเกจ  FTP server (package vsftpd)  

ใช้คำสั่งตรวจสอบ packet ftpd ว่า ติดตั้งแล้วยัง 

*#rpm -q vsftpd*  ⏪⏪⏪  ***ถ้ายัง ให้ติดตั้ง packet vsfpd***


#### 2\. ใช้คำสั่ง yum install ติดตั้งแพ็กเกจ  vsftpd 

*#yum install -y vsftpd*    ⏪⏪⏪  ***ติดตั้ง packet vsfpd***
 

#### 3\.ใช้คำสั่ง netstat ตรวจสอบสถานะการเชื่อมต่ออินเทอร์เน็ต 

*#netstat -tanp |grep 21*

หรือ 

*#netstat -tanp |grep ftp*

----

####  แก้ไขไฟล์ config vsftpd.conf   ⏪⏪⏪  *** /etc/vsftpd ***

กำหนดค่า vsftpd  แก้ไขการกำหนดค่า vsftpd ให้แก้ไขไฟล์กำหนดค่าสำหรับ vsftpd เปิดไฟล์ด้วยคำสั่งต่อไปนี้: 


ใช้คำสั่ง

*# namo /etc/vsftpd/vsftpd.conf  ⏪⏪⏪  *** /etc/vsftpd ***

#### ดำเนินการแก้ไขโดยเอาเครื่องหมาย # ออกจากด้านหน้าข้อความในบรรทัดที่ 101 กับ 103 ดังนี้ ####


#chroot_list_enables=YES **เป็น chroot_list_enables=YES  เอาเครื่องหมาย # ออกจากด้านหน้า**

#chroot_list_file=/etc/vsftpd/chroot_list **เป็น chroot_list_file=/etc/vsftpd/chroot_list  เอาเครื่องหมาย # ออกจากด้านหน้า**

เพื่อจำกัดสิทธิ์การ access ตามที่เราต้องการในที่นี้ทางเราจะกำจัดสิทธิ์การเข้าถึง directory ของ user ให้สามารถ access ตามที่เรากำหนดเท่านั้น 

**ใช้คำสั่ง netstat ตรวจสอบสถานะการเชื่อมต่ออินเทอร์เน็ต**

*#netstat -tanp |grep 21*

หรือ 

*#netstat -tanp |grep ftp*

----



#### ทดสอบใช้งาน FTP และ config vsftpd server ด้วย โปรแกรม WinSCP

โปรแกรม WinSCP [Program Winscp](https://winscp.net/eng/download.php "winsc") <<<<download 

Host : ใส่หมายเลข IP server ของท่าน

Username : ชื่อผู้ใช้

Password : รหัสผ่าน

Port : 21 แต่หากไม่สามารถใช้งานได้ โดยโปรโตคอล FTP อาจถูกบล็อกโดยไฟร์วอลล์ ISP ของท่าน ให้ลองเชื่อมต่อผ่าน SFTP (เช่น ใช้หมายเลข 22 เป็นต้น) 
ใช้คำสั่ง   

----


