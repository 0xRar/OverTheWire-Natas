### *Challenge Name:* **`Natas7`**
### *Level:* **`Level 7`**


- Username: natas7
- Password: 7z3hEENjQtflzgnT29q7wAvMNfZdh0i9
- URL: http://natas6.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115260116-21f85f80-a13b-11eb-86ce-d8512fcbb57d.png)


First thing i did is take a look at the `source code` and im already thinking its `LFI(Local File Inclusion)`

we have 2 links right here and a hint:
```
<a href="index.php?page=home">Home</a>
<a href="index.php?page=about">About</a>

<!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->
```
when you click on one of the links you see this in the URL ofcourse `index.php?page=home`
i know its an LFI so i tried `index.php?page=/etc/natas_webpass/natas8` without going up(`../`)
and it worked we got our password.

![image](https://user-images.githubusercontent.com/33517160/115260629-9df2a780-a13b-11eb-8efd-4370ee2ef21c.png)


### natas8 password: **`DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe`**
