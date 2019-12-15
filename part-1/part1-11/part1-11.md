## Part 1.11

[Dockerfile](./Dockerfile)

Commands used:

```bash
$ docker build -t backend .
$ docker run -d -v $(pwd)/logs/logs.txt:/myapp/logs.txt -p 8000:8000 --name backend backend
```


Prev: [Part 1.10](../part1-10/part1-10.md)  
Next: [Part 1.12](../part1-12/part1-12.md)
