### เปิด โปรแแกรม Terminal (เพื่อใช้งาน คำสั่งแบบ command)

#### 1\.   ให้ ดู Shell ว่าอยู่ใน user ใด?
   $ >> user
   # >> root 

#### 2\. คำส่ั่ง whoami << ดูสถาณะ

#### 3\. เปลี่ยนสถาณะเป็น root

   $su 

   password < ใส่ password ของ root ที่กำหนดไว้ 

      # <--mode root แล้ว

#### 4\. ทดสอบการเชื่อมต่อ internet

      # ping 8.8.8.8 <--- ทดสอบการเชื่อมต่อ internet , ออกจาก ping ctl-z

#### 5\. Update CentOS7
   #yum update <== CentOS7 หยุดการสนับสนุน online ต้องแก้ไข  

   #cd /  <== dir root
   #ls    <== check 
   
#### 6\. แก้ไข 

   #cd /etc/yum.repos.d  <== dir yum.repos.d

   #rm \*  <== delete all file ทั้งหมดใน Directory /yum.repos.d

   #vi CentOS-Base.repo   <== ใช้ โปรแกรท vi หรือ โปรแกรม nanoเขียน sqript ใหม่
   ##### หรือ 
   #nano CentOS-Base.repo   <== หรือ โปรแกรม nanoเขียน sqript ใหม่

#### 7\. นำไฟล์ มาแก้ไข ในไฟล์  CentOS-Base.repo
  
