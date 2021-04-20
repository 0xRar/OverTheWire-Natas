### *Challenge Name:* **`Natas8`**
### *Level:* **`Level 8`**


- Username: natas8
- Password: DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe
- URL: http://natas8.natas.labs.overthewire.org

# Solution:
![image](https://user-images.githubusercontent.com/33517160/115324951-78918800-a193-11eb-8e66-bc9771e43d19.png)

Its the same as `Natas6` but this time we have a function that encodes.

`source code`:
```

<?
$encodedSecret = "3d3d516343746d4d6d6c315669563362";

function encodeSecret($secret) {
    return bin2hex(strrev(base64_encode($secret)));
}

if(array_key_exists("submit", $_POST)) {
    if(encodeSecret($_POST['secret']) == $encodedSecret) {
    print "Access granted. The password for natas9 is <censored>";
    } else {
    print "Wrong secret";
    }
}
?>
```

we have a variable `$encodedSecret` that holds the Secret and a function `encodeSecret` that will encode the `$encodedSecret`
it will encode it to hex than reverse the string i think?  PHP is not my strongest suit so im just guessing here but if we can reverse this algorithm 
change the encoding to decode i think that would work.


```
<?php
function decodeSecret($secret){
  return base64_decode(strrev(hex2bin($secret)));
  }
  
print "secret pass: "; 
print decodeSecret("3d3d516343746d4d6d6c315669563362");
print "\n";
?>
```

after running this php script in our apache server i used `xampp` to run the php script all you have to do
is create file in (`/xampp/htdocs`) `filename.php` and paste the script in it than save it and run(`apache, MySQL`):

![image](https://user-images.githubusercontent.com/33517160/115344018-632d5580-a1b5-11eb-868f-61038283f85c.png)

all you have to do is access `localhost` or `127.0.0.1` via a web browser of your choice,
http://127.0.0.1:`port_number`/filename.php/

after getting the secret `oubWYf2kBq` lets enter it and get our password for the next
challenge.

### natas9 password: **`W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl`**
