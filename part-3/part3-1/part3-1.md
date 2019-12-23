## Part 3.1

Before:
```bash
$ docker history frontend
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
3c67c78780d5        2 minutes ago       /bin/sh -c #(nop)  EXPOSE 5000                  0B                  
f6888de961ed        2 minutes ago       /bin/sh -c #(nop)  CMD ["/bin/sh" "-c" "npm …   0B                  
a5820d892f8a        2 minutes ago       /bin/sh -c npm install                          155MB               
9e17d9817276        3 minutes ago       /bin/sh -c #(nop) COPY dir:b2f6cea9477b5615e…   571kB               
9554e481d5fb        3 minutes ago       /bin/sh -c apt install -y nodejs                87.2MB              
eaec8ac5f3bb        3 minutes ago       /bin/sh -c curl -sL https://deb.nodesource.c…   35.9MB              
203047c89993        4 minutes ago       /bin/sh -c apt-get update && apt-get install…   42MB                
729ae05330c7        4 minutes ago       /bin/sh -c #(nop) WORKDIR /myapp                0B                  
549b9b86cb8d        4 days ago          /bin/sh -c #(nop)  CMD ["/bin/bash"]            0B                  
<missing>           4 days ago          /bin/sh -c mkdir -p /run/systemd && echo 'do…   7B                  
<missing>           4 days ago          /bin/sh -c set -xe   && echo '#!/bin/sh' > /…   745B                
<missing>           4 days ago          /bin/sh -c [ -z "$(apt-get indextargets)" ]     987kB               
<missing>           4 days ago          /bin/sh -c #(nop) ADD file:53f100793e6c0adfc…   63.2MB

$ docker history backend
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
8f77f4de71e9        4 minutes ago       /bin/sh -c #(nop)  EXPOSE 8000                  0B                  
d61cc2155f8d        4 minutes ago       /bin/sh -c #(nop)  CMD ["/bin/sh" "-c" "npm …   0B                  
f109ea594841        4 minutes ago       /bin/sh -c npm install                          58.4MB              
b4b71316aae4        4 minutes ago       /bin/sh -c #(nop) COPY dir:c4da7e477e24b051e…   578kB               
9554e481d5fb        6 minutes ago       /bin/sh -c apt install -y nodejs                87.2MB              
eaec8ac5f3bb        6 minutes ago       /bin/sh -c curl -sL https://deb.nodesource.c…   35.9MB              
203047c89993        7 minutes ago       /bin/sh -c apt-get update && apt-get install…   42MB                
729ae05330c7        7 minutes ago       /bin/sh -c #(nop) WORKDIR /myapp                0B                  
549b9b86cb8d        4 days ago          /bin/sh -c #(nop)  CMD ["/bin/bash"]            0B                  
<missing>           4 days ago          /bin/sh -c mkdir -p /run/systemd && echo 'do…   7B                  
<missing>           4 days ago          /bin/sh -c set -xe   && echo '#!/bin/sh' > /…   745B                
<missing>           4 days ago          /bin/sh -c [ -z "$(apt-get indextargets)" ]     987kB               
<missing>           4 days ago          /bin/sh -c #(nop) ADD file:53f100793e6c0adfc…   63.2MB
```

After:
```bash
$ docker history frontend
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
f294b8165bbd        42 minutes ago      /bin/sh -c #(nop)  EXPOSE 5000                  0B                  
07f6bfa14b29        42 minutes ago      /bin/sh -c #(nop)  CMD ["/bin/sh" "-c" "npm …   0B                  
048c3f90ee5b        42 minutes ago      /bin/sh -c apt-get update && apt-get install…   286MB               
4c79720b32c6        43 minutes ago      /bin/sh -c #(nop) COPY dir:b2f6cea9477b5615e…   571kB               
729ae05330c7        58 minutes ago      /bin/sh -c #(nop) WORKDIR /myapp                0B                  
549b9b86cb8d        4 days ago          /bin/sh -c #(nop)  CMD ["/bin/bash"]            0B                  
<missing>           4 days ago          /bin/sh -c mkdir -p /run/systemd && echo 'do…   7B                  
<missing>           4 days ago          /bin/sh -c set -xe   && echo '#!/bin/sh' > /…   745B                
<missing>           4 days ago          /bin/sh -c [ -z "$(apt-get indextargets)" ]     987kB               
<missing>           4 days ago          /bin/sh -c #(nop) ADD file:53f100793e6c0adfc…   63.2MB

$ docker history backend
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
f17d3a4b5acb        25 minutes ago      /bin/sh -c #(nop)  EXPOSE 8000                  0B                  
ffddd465536e        25 minutes ago      /bin/sh -c #(nop)  CMD ["/bin/sh" "-c" "npm …   0B                  
b18a8b300db9        25 minutes ago      /bin/sh -c apt-get update && apt-get install…   190MB               
bff50fdfc143        26 minutes ago      /bin/sh -c #(nop) COPY dir:c4da7e477e24b051e…   578kB               
729ae05330c7        57 minutes ago      /bin/sh -c #(nop) WORKDIR /myapp                0B                  
549b9b86cb8d        4 days ago          /bin/sh -c #(nop)  CMD ["/bin/bash"]            0B                  
<missing>           4 days ago          /bin/sh -c mkdir -p /run/systemd && echo 'do…   7B                  
<missing>           4 days ago          /bin/sh -c set -xe   && echo '#!/bin/sh' > /…   745B                
<missing>           4 days ago          /bin/sh -c [ -z "$(apt-get indextargets)" ]     987kB               
<missing>           4 days ago          /bin/sh -c #(nop) ADD file:53f100793e6c0adfc…   63.2MB
```
