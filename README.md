# Experiment to create a .NET Web API using Docker scratch

Trying to get a .NET Web API down to the smallest possible container size
without depending on a base distribution for the final image.

## Work in progress

Able to build and run the app locally but not yet got it working in Docker

### On Mac Os (ARM)

```shell
dotnet publish ScratchApi/ScratchApi.csproj -c Release -o ./out --self-contained -r linux-arm64
./out/ScratchApi
```

```shell
docker build -f ScratchApi/Dockerfile.arm64 -t scratch .
```

### On Windows / WSL (x64)

```shell
dotnet publish ScratchApi/ScratchApi.csproj -c Release -o ./out --self-contained -r linux-arm64
./out/ScratchApi
```

```shell
docker build -f ScratchApi/Dockerfile.arm64 -t scratch .
```
