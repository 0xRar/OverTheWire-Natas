### *Challenge Name:* **`Natas6`**
### *Level:* **`Level 6`**


- Username: natas6
- Password: aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1
- URL: http://natas6.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115188708-fb600780-a0ed-11eb-962b-917ee832bda6.png)

so we have this input here but when we enter anything it wont show up as a query in the URL 
but taking look at the `source code` we have this:  `<a href="index-source.html">View sourcecode</a>`

so we can see the php source code of the input 

php source code:
```
<?

include "includes/secret.inc";

    if(array_key_exists("submit", $_POST)) {
        if($secret == $_POST['secret']) {
        print "Access granted. The password for natas7 is <censored>";
    } else {
        print "Wrong secret";
    }
    }
?>
```

after seeing the source code the first thing will come to your mind is `Local File Inclusion`
just because the code is using the `include function in php` but like i said nothing is showing in the url no
query what so ever so i tried `?secret=../../../../../../includes/secret.inc` but didin't work for me,

also in the source code we see that the `include function` is including a `secret.inc` under the directory `/includes/`
im guessing it has the password or some info?? so i tried accessing it normally http://natas6.natas.labs.overthewire.org/includes/secret.inc

![image](https://user-images.githubusercontent.com/33517160/115193831-56492d00-a0f5-11eb-8688-28ca574f8cb9.png)

and we found what the input password is : `FOEIUWGHFEEUHOFUOIU`


![image](https://user-images.githubusercontent.com/33517160/115194096-a6c08a80-a0f5-11eb-9ac3-fe727402a8cc.png)

and *BOOOOM!* we got out password for the next challenge.


### natas7 password: **`7z3hEENjQtflzgnT29q7wAvMNfZdh0i9`**
