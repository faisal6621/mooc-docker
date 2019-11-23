## Part 1.4

```bash
$ docker run -d devopsdockeruh/exec_bash_exercise
466f45fce918a6274a3b45d7efe0b6289328491a8d4f46fc578e2ec813535025

$ docker ps -a
CONTAINER ID        IMAGE                               COMMAND             CREATED             STATUS                      PORTS               NAMES
466f45fce918        devopsdockeruh/exec_bash_exercise   "node index"        27 seconds ago      Up 26 seconds                                   hardcore_murdock

$ docker exec -it hardcore_murdock sh
# tail -f logs.txt
Sat, 23 Nov 2019 02:49:07 GMT
Sat, 23 Nov 2019 02:49:10 GMT
Secret message is:
"Docker is easy"
Sat, 23 Nov 2019 02:49:16 GMT
Sat, 23 Nov 2019 02:49:19 GMT
Sat, 23 Nov 2019 02:49:22 GMT
Sat, 23 Nov 2019 02:49:25 GMT
Secret message is:
"Docker is easy"
Sat, 23 Nov 2019 02:49:31 GMT
Sat, 23 Nov 2019 02:49:34 GMT
Sat, 23 Nov 2019 02:49:37 GMT
Sat, 23 Nov 2019 02:49:40 GMT
Secret message is:
"Docker is easy"
```


Prev: [Part 1.3](./part1-3.md)  
Next: [Part 1.5](./part1-5.md)
