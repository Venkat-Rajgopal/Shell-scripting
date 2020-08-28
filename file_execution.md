# File execution through bash

Say i have a python file `pyscript.py` that needs to be run through bash. 

The script below simply prints arguments in reverse. 

```python
import sys
for arg in reversed(sys.argv[1:]):
    print(arg)
```
Of course by doing `python pyscript.py a b c d` we can run this script. But here we need to spicify the interpreter. 

By simply adding the line on the top we can run the script without specifing the interpreter in Bash. 

```python
#!/usr/local/bin/env python
```

Now we can run this as, 
```bash
$ ./pyscript.py a b c

c
b
a
```
