## Part 1.12

Frontend [Dockerfile](./frontend/Dockerfile)  
Backend [Dockerfile](./backend/Dockerfile)

Commands used:

```bash
$ cd ./frontend
$ docker build -t frontend .
$ docker run -d -p 5050:5000 --name frontend frontend

$ cd ../backend
$ docker build -t backend .
$ docker run -d -v $(pwd)/logs/logs.txt:/myapp/logs.txt -p 8090:8000 --name backend backend
```


Prev: [Part 1.11](../part1-11/part1-11.md)  
Next: Part 1.13