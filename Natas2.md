### *Challenge Name:* **`Natas2`**
### *Level:* **`Level 2`**


- Username: natas2
- Password: ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi
- URL: http://natas2.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115132454-dfcf0100-a008-11eb-95af-bbd253b1a3e4.png)

We dont see anything on the source code but there is a `<img src="files/pixel.png">`

we can see the image called `pixel.jpg` is stored in a directory called `files`
lets try to access files and hope we get status code 200

![image](https://user-images.githubusercontent.com/33517160/115132605-56203300-a00a-11eb-8a26-09e196fed21f.png)

http://natas2.natas.labs.overthewire.org/files/

- we see that there is a txt file `users.txt`

contents of `users.txt`
```
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```

### natas3 password: **`sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14`**
