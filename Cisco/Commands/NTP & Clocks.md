### Show's

>\#show clock [detailed]
>\#show ntp {associate | status}

### Clock conf

> \#clock set 12:00:00 24 dec 2022 `( hh:mm:ss day month year)`
> \#calender set hh:mm:ss day month year `( Hardware-Clock)`

> \#clock update-calender `( Updates hardware clock based on software clock`
> \#clock read-calender

TIMEZONE:

>\(conf) clock timezone "name" "{-23 | 23}" `(NOR 1), for +1 UTC`

DST (Daylight Saving Time):

>(conf) clock summer-time "name" recurring "DST START" "DST END" 
>`(NOR), (Last Sunday March 02:00), (Last Sunday October 03:00)`

### **NTP** (Network Time Protocol)

>(conf) NTP server "ip" [key "num"]

>(conf) NTP update-calender

>(conf) NTP peer "ip" [key "num"]

NTP Master

>(conf) NTP master [stratum]
>(conf) NTP source "int"

NTP Authentication

>(conf) NTP authentication
>(conf) NTP authentication-key "key-num" MD5 "password" `(1, pass123)` 
>(conf) trusted-key 1