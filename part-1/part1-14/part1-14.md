## Part 1.14

Changes done in `Gemfile`, uncommented the code:

```
gem 'mini_racer', platforms: :ruby
```

Running the example:

```bash
$ docker build -t ruby-example .
$ docker run -d -p 3000:3000 --name ruby-example ruby-example
```


Prev: Part 1.13 - [Dockerfile](../part1-13/Dockerfile)  
