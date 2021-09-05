# tinyproxy-sample
use tinyproxy on docker-compose

# usage

- `localhost:8080/web` -> `web:8080/` (on container `web`)
- `localhost:8080/example` -> `example.com`

```bash
$ curl -i localhost:8080/web/names
HTTP/1.1 200 OK
Via: 1.1 cd7ca1234f47 (tinyproxy/1.11.0)
Content-Length: 18
Content-Type: application/json
Date: Sun, 05 Sep 2021 01:31:33 GMT

{"names":["Taro"]}

$ curl -i localhost:8080/example/
HTTP/1.0 200 OK
Via: 1.1 c9f985fbb8e5 (tinyproxy/1.11.0)
Accept-Ranges: bytes
Age: 423673
Cache-Control: max-age=604800
Content-Type: text/html; charset=UTF-8
Date: Sat, 04 Sep 2021 12:43:55 GMT
Etag: "3147526947"
Expires: Sat, 11 Sep 2021 12:43:55 GMT
Last-Modified: Thu, 17 Oct 2019 07:18:26 GMT
Server: ECS (sab/56F3)
Vary: Accept-Encoding
X-Cache: HIT
Content-Length: 1256

<!doctype html>
<html>
<head>
    <title>Example Domain</title>
...
```
