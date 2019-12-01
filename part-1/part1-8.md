## Part 1.8

```bash
$ docker run -v $(pwd)/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
(node:1) ExperimentalWarning: The fs.promises API is experimental
Wrote to file /usr/app/logs.txt
Wrote to file /usr/app/logs.txt
Wrote to file /usr/app/logs.txt
```

```bash
$ cat logs.txt 
Sun, 01 Dec 2019 17:08:35 GMT
Sun, 01 Dec 2019 17:08:38 GMT
Sun, 01 Dec 2019 17:08:41 GMT
```


Prev: [Part 1.7](./part1-7/part1-7.md)  

