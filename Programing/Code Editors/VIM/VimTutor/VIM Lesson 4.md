File location, status, Line, %, collum
>CTRL-G = Show info

500G
>"num"G = Move to Line

>G = End of file

>gg = Start of file

### Search

/power

>/ = Search

>? = Search but reversed

**n** = Search down

**N** = Search up

>CTRL + O = Go back

>CTRL + I = Go forward

---

Debuging Search (Usefull in programing)
>% = search for matching: (, [, {

# Changing ( Old -> New )

>:s/old/new/g

:s = substitude / Find and replace

/old/new = Changes every "old" to "new"

/g = globaly in the line

```` VIM
thee plum is in thee flower
:s/thee/the/g

the plum is in the flower
````

---

###### Change / **Substitute** a lot:

- Changes everything. from LINE 100 - 200

>:#,#s/old/new/g
>
:100,200s/old/new/g

- Changes everything. On ENTIRE FILE

>:%s/old/new/g

Gives you a **prompt** to change:

>:%s/old/new/gc