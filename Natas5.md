### *Challenge Name:* **`Natas5`**
### *Level:* **`Level 5`**


- Username: natas5
- Password: iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
- URL: http://natas5.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115174378-d3fb4180-a0d1-11eb-84cc-49267a169598.png)

hmmmm, since we can't login and there is nothing on in the `source code`
i'm thinking of `broken authentication & session management attacks`
so first thing im gonna do is check for any cookies with a `
cookie editor browser extention` on Firefox
or chrome. 

![image](https://user-images.githubusercontent.com/33517160/115178203-7965e380-a0d9-11eb-8bbe-3c470c29465d.png)

only cookie here is a `loggedin` = `value`:`0` this is how the 
website keeps track of loggedin users is by this cookie lets increase the value to `1`
and see what we get:

![image](https://user-images.githubusercontent.com/33517160/115178560-3c4e2100-a0da-11eb-8c4a-607f97fe0c60.png)

and that was successful....we got our password



### natas6 password: **`aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1`**
