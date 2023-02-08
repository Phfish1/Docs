### Execute commands

>:! = Execute commands

:!ls
:!bin/bash

### Visual mode

Highlight text
>v = visual mode

### Writing files

>:wq = write and quit

---

Writes a new file with name "FILENAME"
>:w FILENAME

---

highlight text with "v"(visual mode) then:
>:'<,'>:w 'FILENAME'

creates a new File with the text highlighted

---

### Adding text EZ

**Retrieve** / paste the content of a file
>:r FILENAME

Retrieves the command output
>:r !ls


