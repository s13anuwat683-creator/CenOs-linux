# แหล่งข้อมูล

[centos-7-x86_64-dvd-2009.iso](https://mirror.psu.ac.th/centos/7.9.2009/isos/x86_64/ "centos-7-x86_64-dvd-2009.iso") *<<click*

[Deployment, Configuration and Administration of Red Hat Enterprise Linux 6](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/6/html/deployment_guide/index "Deployment, Configuration and Administration of Red Hat Enterprise Linux 6") *<<click*

---

 # คำสั่ง Reboot บน Linux
 
***Restart Restart Command***

##### ทำการรีบูทเครื่องทันที
*#shutdown -r now*

##### ทำการรีบูทเครื่องในอีก 5 นาทีข้างหน้า
*#shutdown -r +5*

##### ทำการรีบูทเครื่องทันที
*#reboot*

หรือ

*#init 6*

 # คำสั่ง Shutdown  บน Linux

ปิดเครื่องทันที

#shutdown -h now

ปิดเครื่องในอีก 10 นาที

#shutdown -h +10

ปิดเครื่องในเวลา 18:00 น.

#shutdown -h 18:00

ปิดเครื่องทันที

#poweroff

ปิดเครื่องทันที

#init 0 


---

# คำสั่งntsysv

ntsysv เป็นโปรแกรมที่ช่วยให้เราเปิดปิดเซอร์วิสได้ง่าย ถ้ามีเครื่องหมายดอกจัน อยู่ด้านหน้าหมายความว่าในการบูทเครื่องเข้ามา เซอร์วิสนั้นจะทำงาน แต่ถ้าไม่มีเครื่องหมายดอกจันเปิดเครื่องมาใหม่เซอร์วิสนั้นไม่ทำงาน
การที่จะให้มีเครื่องหมายดอกจัน หรือให้เครื่องหมายดอกจันหายไปให้กดปุ่ม spacebar

[![ntsysv](https://access.redhat.com/webassets/avalon/d/Red_Hat_Enterprise_Linux-6-Deployment_Guide-en-US/images/fae44841ba01c8c7b2af15735b3495bb/controlling-access-to-services-ntsysv.png "ntsysv")](https://access.redhat.com/webassets/avalon/d/Red_Hat_Enterprise_Linux-6-Deployment_Guide-en-US/images/fae44841ba01c8c7b2af15735b3495bb/controlling-access-to-services-ntsysv.png "ntsysv")









