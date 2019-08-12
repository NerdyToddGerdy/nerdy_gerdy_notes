On create, use:
  `-t -i`

`pkill -9 -f 'docker.*attach`
```
[berto@g6]$ docker run -d --name test python:3.6 /bin/bash -c 'while [ 1 ]; do sleep 30; done;'
b26e39632351192a9a1a00ea0c2f3e10729b6d3e22f8e0676d6519e15c08b518

[berto@g6]$ docker attach test
# here I typed ^P^Q and doesn't work
^P
# ctrl+c doesn't work either
^C
# can't background either
^Z

# go to another shell and run the `pkill` command above

# i'm back to my prompt
[berto@g6]$
```pkil