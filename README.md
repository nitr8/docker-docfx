## Building documentation in docker with DocFX

## Usage

Start your container exposing port 8124
```
docker run --rm -it -p 8082:8082 whumphrey/docfx
```

Start your container exposing port 8124 and using your local documentation
```
docker run --rm -it -p 8082:8082 -v /Users/whumphrey/projects/docfx/_site2:/docs whumphrey/docfx
```

Start your container exposing port 8124 and using your local documentation rendered from `docs/`

```
docker run --rm -it -p 8082:8082 -v $PWD/docs:/docs whumphrey/docfx
```

Please see the sample docfx documentation project https://github.com/docascode/docfx-seed

## Quick setup

Go to [http://127.0.0.1:8082](http://127.0.0.1:8082) in your browser and enjoy your markdown in html.

### build
```
git clone https://github.com/nitr8/docker-docfx.git
docker build -t whumphrey/docfx .
docker run --rm -it -p 8082:8082 -v $PWD/docs:/docs whumphrey/docfx
```
