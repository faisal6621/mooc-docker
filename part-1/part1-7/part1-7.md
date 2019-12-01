## Part 1.7

[Dockerfile](./Dockerfile)  
[curler.sh](./curler.sh)

```bash
$ docker build -t curler .
Sending build context to Docker daemon  38.15MB
Step 1/6 : FROM ubuntu:latest
 ---> 775349758637
Step 2/6 : WORKDIR /mydir
 ---> Using cache
 ---> 268f11ec60f5
Step 3/6 : COPY ./curler.sh .
 ---> Using cache
 ---> 534de39791e3
Step 4/6 : RUN chmod a+x ./curler.sh
 ---> Using cache
 ---> b10299a8bc23
Step 5/6 : RUN apt-get update && apt-get install -y curl
 ---> Using cache
 ---> 496017f61ea1
Step 6/6 : CMD ["./curler.sh"]
 ---> Using cache
 ---> 4aaa30fb698c
Successfully built 4aaa30fb698c
Successfully tagged curler:latest
```

```bash
$ docker run -it curler
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```


Prev: [Part 1.6](../part1-6/part1-6.md)  
Next: [Part 1.8](../part1-8.md)
