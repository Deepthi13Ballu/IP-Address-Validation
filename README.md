# IP-Address-Validation
import re
n=int(input())
for i in range(n):
    string=input()
    regex_string1="^(25[0-5]\.|2[0-4][0-9]\.|[01]?[0-9]?[0-9]\.){1,3}(25[0-5]|2[0-4][0-9]|[01]?[0-9]?[0-9])$"
    regex_string2="^(?:[a-f0-9]{1,4}:){7}[a-f0-9]{1,4}$"
    res1=bool(re.search(regex_string1,string))
    res2=bool(re.search(regex_string2,string))
    if(res1==True):
        print("IPv4")
    elif(res2==True):
        print("IPv6")
    else:
        print("Neither")
