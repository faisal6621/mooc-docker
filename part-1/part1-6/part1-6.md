## Part 1.6

[Dockerfile](./Dockerfile)

```bash
$ docker build -t docker-clock .
Sending build context to Docker daemon  38.15MB
Step 1/2 : FROM devopsdockeruh/overwrite_cmd_exercise
 ---> 3d2b622b1849
Step 2/2 : CMD ["--clock","10"]
 ---> Running in 8a5ecda103ad
Removing intermediate container 8a5ecda103ad
 ---> 15bc525c2251
Successfully built 15bc525c2251
Successfully tagged docker-clock:latest
```

```bash
$ docker run docker-clock
11
12
13
14
15
```


Prev: [Part 1.5](../part1-5.md)  
Next: [Part 1.7](../part1-7/part1-7.md)
