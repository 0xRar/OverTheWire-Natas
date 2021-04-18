### *Challenge Name:* **`Natas3`**
### *Level:* **`Level 3`**

- Username: natas3
- Password: sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
- URL: http://natas3.natas.labs.overthewire.or

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115132800-270ac100-a00c-11eb-9ccc-2d7b7360748e.png)

this is the only thing in the source code
`<!-- No more information leaks!! Not even Google will find it this time... -->`

when i saw that i thought of `robots.txt` maybe there is something there


**What is robots.txt ?**

A robots.txt file tells search engine crawlers which pages or files the crawler can or can't request from your site.

in http://natas3.natas.labs.overthewire.org/robots.txt we found a Disallowed directory `/s3cr3t/`

in the directory `/s3cr3t` has a file `users.txt`

![image](https://user-images.githubusercontent.com/33517160/115133082-2541fd00-a00e-11eb-8269-a87409085a47.png)

in `users.txt` we find our natas4 password

### natas4 password: **`Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ`**
