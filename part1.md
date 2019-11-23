# Part 1

## Part 1.1

```bash
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS                                              NAMES
23e2519b8409        postgres            "docker-entrypoint.s…"   45 seconds ago      Exited (0) 13 seconds ago                                                      cranky_brattain
c825b793fd35        jenkins             "/bin/tini -- /usr/l…"   6 minutes ago       Up 5 minutes                0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp   musing_sanderson
3e6e4126b974        nginx:latest        "nginx -g 'daemon of…"   19 minutes ago      Exited (0) 4 seconds ago                                                       happy_bell
```

## Part 1.2

```bash
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```

```bash
$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```

## Part 1.3

```bash
$ docker run -it devopsdockeruh/pull_exercise
Unable to find image 'devopsdockeruh/pull_exercise:latest' locally
latest: Pulling from devopsdockeruh/pull_exercise
8e402f1a9c57: Pull complete 
5e2195587d10: Pull complete 
6f595b2fc66d: Pull complete 
165f32bf4e94: Pull complete 
67c4f504c224: Pull complete 
Digest: sha256:7c0635934049afb9ca0481fb6a58b16100f990a0d62c8665b9cfb5c9ada8a99f
Status: Downloaded newer image for devopsdockeruh/pull_exercise:latest
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
```

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
