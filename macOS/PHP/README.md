Install [apple/container](https://github.com/apple/container)

```bash
brew install container
```

Set up DNS

```bash
$ sudo container system dns create test
$ container system property set dns.domain test
```

Set up container

```bash
$ container system start
$ container build --tag chancearthur --file _init/apple-container/Containerfile .
```

Start container

```bash
$ container system start
$ container run --name chancearthur --detach --rm -p 8080:8000 --mount type=bind,source=$PWD,target=/var/www/html chancearthur
```

Stop container

```bash
$ container stop chancearthur
```