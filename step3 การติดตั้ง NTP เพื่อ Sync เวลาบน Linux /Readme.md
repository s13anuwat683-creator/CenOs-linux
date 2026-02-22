### การติดตั้ง NTP เพื่อ Sync เวลาบน Linux เพื่อทำให้เวลาของเครื่องตรงมากที่สุด โดยสามารถติดตั้งง่ายๆ โดยใช้คำสั่งดังต่อไปนี้     
------------
#### เปิด โปรแแกรม Terminal (เพื่อใช้งาน คำสั่งแบบ command)

#### 1\. ให้พิมพ์ คำสั่ง 
#yum -y install ntp

#timedatectl set-timezone Asia/Bangkok# timedatectl

#service ntpd restart 

#systemctl enable ntpd.service

#### 2\.🏴สามารถตรวจสอบว่า เวลาถูกต้องหรือไม่ โดยใช้คำสั่ง 
#date           <=== ตรวจสอบว่าเวลาถูกต้องหรือไม่

------------
