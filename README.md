# xcgo
CGO Cross Compiler

## Support Target
* Linux x86_64 | armhf | aarch64 | mips64el
* Windows x86_64

## Usage 
linux x86_64
```
cd project_dir
docker run --rm -v $(pwd):/workdir illuspas/xcgo go build -v
```

linux x86_64 with proxy 
```
cd project_dir
docker run --rm -v $(pwd):/workdir -e HTTPS_PROXY=http://192.168.0.11:8118 illuspas/xcgo go build -v
```

windows x86_64
```
cd project_dir
docker run --rm -v $(pwd):/workdir -e CGO_ENABLED=1 -e GOOS=windows -e GOARCH=amd64 -e CC=x86_64-w64-mingw32-gcc illuspas/xcgo go build -v
```

# TODO
Add darwin-x86_64
