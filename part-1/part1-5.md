## Part 1.5

```bash
$ docker run -it --name curl ubuntu:latest sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
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

In the other terminal while waiting for `Input website:`:
```bash
$ docker exec -it curl sh
# apt-get update

# apt-get install curl
```


Prev: [Part 1.4](./part1-4.md)  
Next: [Part 1.6](./part1-6/part1-6.md)
