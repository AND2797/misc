```bash
tac file | grep -m1 "string" | grep -E "string1|string2"
#find the first instance of string from reverse, look for string1 or string2

tac file | grep -m1 "string" | grep -oE ".{0,20}string{0,20}"
#same as above, but find string with a context of 20 chars before and after
```
