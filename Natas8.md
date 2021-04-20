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
it will encode it to hex i think than reverse the string i think?  PHP is not my strongest suit so im just guessing here but if we can reverse this algorithm 
change the encoding to decode i think that would work.

```
<?php
function decodeFunc($secret){
  return base64_decode(strrev(hex2bin($secret)));
  }

print decodeFunc("3d3d516343746d4d6d6c315669563362");
print "<br>";
?>
```

