```bash
tac file | grep -m1 "string" | grep -E "string1|string2"
#find the first instance of string from reverse, look for string1 or string2

tac file | grep -m1 "string" | grep -oE ".{0,20}string1{0,20}"
#same as above, but find string1 with a context of 20 chars before and after

tac file | grep -m6 "string1" | grep -oE ".{0,20}string2.{0,20}|.{0,500}string1.{0,20}"
#grep for string1 if exists grep for string2 and string1 and output with context
```
